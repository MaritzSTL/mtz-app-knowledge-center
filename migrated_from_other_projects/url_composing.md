# TL;DR Image Url from Endpoint

To generate absolute image uri's from the api, we need to:

## Hit the endpoint
https://d-adesa-api.salesnext.com/api/rest/promotions/172/tile?dev=admin

* Grab BACKGROUND_PATH and BACKGROUND_FILENAME
* BACKGROUND_PATH -> `promotool|images|tile|background|17212552`
* BACKGROUND_FILENAME -> `WF-BOS-IMAGE-900x410-V7.jpg`

## Compose the new URL

We need to hit the `filesystem`. To do that, we append `filesystem` after `/api/rest/` (example below):

[ hostname + '/filesystem/' + (**escaped** BACKGROUND_PATH) + '/' + BACKGROUND_FILENAME ]

You can see above the path has a lot of `|`'s in it. '|'s escape character is `%7C`

```
['https://d-adesa-api.salesnext.com/api/rest/' + '/filesystem/' + 'promotool%7Cimages%7Ctile%7Cbackground%7C17212552%0A' + '/' + 'WF-BOS-IMAGE-900x410-V7.jpg' ]
```

## Add a valid JWT

However, filesystem doesn't allow you to get the images without a valid JWT token (indicating this is a user with a valid, live session). The `?dev=admin` approach doesn't work here. To get a JWT, you have to log in to the appropriate environment. We can pass that in as a query param, so `?jwt=`

Example JWT: `eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsImFjdGl2aXR5VGltZW91dCI6dHJ1ZSwiaWF0IjoxNTA5NTYzMDcyLCJpc3MiOiJhZGVzYS1hcGkiLCJleHAiOjE1MDk1OTkwNzJ9.H2KORHkrNAveaFR9CRatLfid5wZmr9rWIBatwn-z4Tc`

To get a valid JWT, you have to sign in.

## Finished URL:

So, to get the finished url for `https://d-adesa-api.salesnext.com/api/rest/promotions/172/tile?dev=admin`, we put it all together:

`https://d-adesa-api.salesnext.com/api/rest/filesystem/promotool%7Cimages%7Ctile%7Cbackground%7C17212552%0A/WF-BOS-IMAGE-900x410-V7.jpg?jwt=eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsImFjdGl2aXR5VGltZW91dCI6dHJ1ZSwiaWF0IjoxNTA5NTYzMDcyLCJpc3MiOiJhZGVzYS1hcGkiLCJleHAiOjE1MDk1OTkwNzJ9.H2KORHkrNAveaFR9CRatLfid5wZmr9rWIBatwn-z4Tc`

The database is decoupled from the filesystem, so even though the API might return it, there's no guarantee that it actually exists.

## Appendix

* Why the `foo.salesnext.com` and `foo-api.salesnext.com`?

> Mostly lack of NGINX config reasons.  We have a 2 server setup, so if you call `/api/rest` it will route to the server that hosts the UI, how the browser is designed, so for you guys: `https://d-adesa.salesnext.com/api/rest` that won't do anything because the API isn't on that server, normally we'd use an NGINX config to do that but since we can't get them to update it, our interceptor is designed to do that for you before it sends the request.

The api is hosted on `foo-api.salesnext.com`, and the ui is hosted on `foo.salesnext.com`

This means, requests with `/api/rest` need to hit a host with `-api` in it. This is what the ajax interceptor does.

All other requests can hit the url as usual.

* Why pass back an escaped string?

No idea, but `@jagan` said `@bob` would know.

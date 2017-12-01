# Building Customizable Components

It would be sweet if we could set a couple app-wide styles on a per-client basis, and have all the components in the app respond to those styles. We'd need a way to set styles in some global place, then have those apply down inside the shadow-dom of all the components.

So, the question is, what do we set? How do they apply?

Polymer provides a mechanism for this called called [custom properties](https://www.polymer-project.org/2.0/docs/devguide/custom-css-properties). They look like this:

```
--paper-checkbox-checked-color: var(--paper-red-500);
```

If you have the two dashes at the start, it means that whatever you put there can pierce through the shadow dom membrane and get from parent app's styles into the specific web component's styles.

So, tl;dr, things with `--` are "Custom properties"

The only sensible way I can think of to tackle this is:

1. Figure out the whole set of what all these custom properties are and where they come from (us or a library?)
2. For a given component, be able to select which ones we need
3. Actually apply those. So that's what this is walking through.

You can see what all these are in your console:
![in the console](https://i.imgur.com/ajIFtun.png)

## 1. What are all the potential variables?

Went through and grabbed all the variables that are injected through the shadow-dom in `mtz-promo-builder` and `mtz-app-contests`. Here's that list:

### What we use
```
var(--mtz-promo-card--border-color, #E0E0E0)
var(--mtz-promo-card__sales--color, #1565C0)
var(--mtz-promo-card__earnings--color, #1565C0)
var(--mtz-promo-item--selected--border-color, #1976D2)
var(--mtz-promo-search__input--focus-color, var(--default-primary-color))
var(--mtz-promo-search__button--color, #FFF)
var(--mtz-promo-search__button--background-color, var(--default-primary-color))
var(--app-secondary-color)
var(--app-gray-color)
var(--app-font-size-sm)
var(--app-primary-color)
var(--app-white-color)
var(--app-black-color)
var(--ci-profile-card-text, var(--app-black-color))
var(--ci-profile-card-headers, var(--app-primary-color))
var(--app-font-size-lg)
var(--app-font-size-base)
var(--ci-profile-card__icon-color, var(--app-primary-color))
var(--ci-profile-card__icon-size)
var(--ci-profile-card-size, 100px)
var(--app-font-size-h5)
var(--app-tertiary-color)
var(--icon-size)
var(--circle-size)
var(--app-font-size-h2)
var(--app-font-size-h6)
var(--app-font-size-h1)
var(--app-font-size-h3)
var(--app-font-size-h4)
var(--success-color)
var(--failure-color)
var(--app-success-color)
```
### What do we set? What's set Elsewhere?
A bunch of these are set by default:
* [paper elements](https://github.com/PolymerElements/paper-styles/blob/master/default-theme.html), * [paper elements colors](https://github.com/PolymerElements/paper-styles/blob/master/color.html)

## 2. For an given component, how do I select the ones I need to support?

## 3. How do I actually syntactically inject these?

## Note:

Sounds like there's another approach to this coming out with selectors that pierce the shadow dom boundary, but I'm not sure where to find more info around this. check with `@stramel`


Authors:
Chris Zempel (`@Chris Zempel`) & Shawn Barnes (`@shawnb`)

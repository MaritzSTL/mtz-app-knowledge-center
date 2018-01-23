## Writing a chapter template

When determining your chapter, start with:
1. Students will be able to... what?
2. Why would they want to learn this at all? Find the motivation
3. Where are they starting from? Begin with information they already know.
4. Build information incrementally on itself, until you arrive at
5. Them being able to do what they couldn't, before.
6. Add some exercise they can perform to apply what they just learned, and verify they know it
7. What here could you NOT cover? What could you do later?

This is to clarify it for you. Get your facts straight. Next, arrange it like this:

* **Introduction**: Entice them with the expertise they're going to gain - in whatever fashion makes sense, outline what they're learning, and why it's in their best interest to learn it
* **Supporting Fact 1**:
* **Supporting Fact 2**:
* **Supporting Fact 3**:
* (Maybe more who knows its ok)
* **Conclusion**:
* **Exercise**:

## Example Chapter Template: Custom Elements (Ch 4)

1. Students will be able to... what?
* have an awareness of the underlying custom elements apis
* understand how the browser will identify and parse specific markup
* dispel any fear of crazy wizardry. this is just plain old javascript


2. Why would they want to learn this at all?
* this is the future. this is the spec everything will eventually run off of, so learning it will effectively increase their market value as dev
* begin to get an understanding of the behavior polymer adds for us, by having to do something manually
* getting comfortable digging into browser internals is fun
* be able to understand what's actually going on when an element is imported.

3. Supporting facts:
* What does the browser do when it sees _any_ element?
* What about a custom one?
* CustomElementRegistry interface
* Adding a new custom element
* Actually importing it onto the page
* Seeing it work

4. Conclusion:
Custom elements api is not magic, nor is the browser. It's html, and js, all the way down!
This is the bedrock that polymer happens on. Polymer does a lot of lifting and convenience-method-making for us

5. Exercise:
We'll add a page to the knowledge center, /smorgasbord. They have to add a custom element to the custom-element smorgasbord. Every person who onboards will add their own.

6. What I'm NOT covering:
Prototypical inheritance in JS, how that affects autonomous vs customized built-in elements.

## Other things noted for later:
Additional tasks which need to be done:
* Analytics embedded into app (online, offline)
* Authentication

Additional chapters which need to be written:
* linting/code format standards
* appropriate testing
* device responsiveness
* i18n
* customizability (is responsive to app-level defaults, so for ex, you can set app colors on per-client basis)
* actual code (events up, properties down)
* reuse considerations
* service workers

# Material Design Components in Elm

Port of Google's
[Material Design Lite](https://www.getmdl.io/)
CSS/JS implementation of the
[Material Design Specification](https://www.google.com/design/spec/material-design/introduction.html).

MDL is implemented primarily through CSS, with a little bit of Javascript
adding and removing CSS classes in response to DOM events. This port
re-implements the CSS parts in Elm, but relies on the CSS of MDL verbatim.

*CAUTION* This is an early and incomplete prototype. Use at your own risk.


### Get Started

Build the demo:

    > elm-make Demo.elm

This will construct a file `index.html`; open that in your browser.

The library has a tiny native component (for measuring geometry of rendered
  elements, a necessity for re-implementing MDL ripple-animations), and so
  cannot be in the elm-package library. If you wish to use the library, I
  know no better way than to copy `Material.elm` and `Material/*` to your
  own project. 


### Contribute

Please do! The easiest place to start is to add more CSS-only components. These require no porting of Javascript, just putting together css-classes as instructed by the [MDL Component Documentation](https://www.getmdl.io/components/index.html). Take a look at

 - [Badges](https://www.getmdl.io/components/index.html#badges-section)
 - [Cards](https://www.getmdl.io/components/index.html#cards-section)
 - [Dialogs](https://www.getmdl.io/components/index.html#dialog-section)
 - [Footers](https://www.getmdl.io/components/index.html#layout-section/footer)
 - [Lists](https://www.getmdl.io/components/index.html#lists-section)
 - [Shadows](https://github.com/google/material-design-lite/tree/v1.1.2/src/shadow)

The remaining components, use Javascript
in various ways. Toggles seem to use Javascript exclusively to insert ripple-animations and __might__ be easy to implement using the `Ripple.elm`
component:

 - [Toggles](https://www.getmdl.io/components/index.html#toggles-section)

The rest I haven't looked at; they may or may not be straightforward to port
to Elm.

 - [Tables](https://www.getmdl.io/components/index.html#tables-section)
 - [Spinners](https://www.getmdl.io/components/index.html#loading-section)
 - [Sliders](https://www.getmdl.io/components/index.html#sliders-section)
 - [Menus](https://www.getmdl.io/components/index.html#menus-section)
 - [Snackbars](https://www.getmdl.io/components/index.html#snackbar-section)
 - [Tooltips](https://www.getmdl.io/components/index.html#tooltips-section)

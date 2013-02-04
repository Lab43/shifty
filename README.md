Shift Grid System
=================

A responsive grid system that works by adding/removing columns, rather than by making columns narrower.


## To Do:

* For stripes, it would be nice to not have to include a .stripes class. In Kickcorps (and probably other real-world projects) it's easiest to turn stripes on and off by just changing the sass variable, and not have to also add/remove a class in the html. However, there should still be the option to require a class. This is useful if you want to toggle stripes off and on with javascript. Hmmm... maybe the stripes show unless you add a class to remove them. Is this the best of both worlds?


## Bugs:

* If $startFluid is false, at4-hide gets immediately overrided by at4-show. In otherwords, there is no reason to ever hide the first breakpoint if $startFluid isn't true.
* If there is a breakpoint at 1 column, it won't use the correct stripe color. It will use the normal stripe color, not the breakpoint color. (why would anyone have a breakpoint at 1?)


## Documentation Notes:

<<<<<<< HEAD
The documentation still needs to be written. Here are some notes to help me remember what needs to be covered.

* using with sass vs using precompiled examples
* variables
* wrapper classes (.conainer, .grid)
* .span*
* .offset*
* how breakpoints work
  * $startFluid
  * .at*-span*, at*-span*
  * at() breakpoint mixin
    * using in conjunction with at() mixin
    * be careful about css bloat
  * if you set a span wider than the current document, it will be treated as full width until a wider breakpoint is reached. This is very helpful.
* layout modes
  * fluid
    * .break, .unbreak
    * .at*-break, .at*-unbreak
  * inline-block
    * Avoiding gaps between inline-block element: [Fighting the Space Between Inline Block Elements](http://css-tricks.com/fighting-the-space-between-inline-block-elements/)
* stripes
* nesting
  * nesting works, but it doesn't prevent you from having spans or offsets that are too wide.
  * breakpoints are only aware of the document width, not the width of spans.
* advice for css
  * avoid class names with 'span' in them
  * width must be preserved, so use box-sizing: border-box to prevent padding and borders from making spans wider


## Features to add

* span groups
  * example: span3-group would make all of it's direct children span3.
  * In other words, .span3-group > * is equivalent to .span3
=======
The documentation still needs to be written. Here are some notes to help me remember what everything does.

* Avoiding gaps between inline-block element: [Fighting the Space Between Inline Block Elements](http://css-tricks.com/fighting-the-space-between-inline-block-elements/)
>>>>>>> 170d2c9fb2e5dafa232c4f669926a42c127ce194


## Acknowledgements:

* Many ideas borrowed from [Twitter Bootstrap](http://twitter.github.com/bootstrap/), including class names and grid dimensions.
* T[Sass/Compass version of Normalize.css](https://github.com/JohnAlbin/normalize.css-with-sass-or-compass) by [John Albin Wilkins](https://github.com/JohnAlbin) is used in the documentation website.

Shift Grid System
=================

A responsive grid system that works by adding/removing columns, rather than by making columns narrower.


## To Do:

* more attractive striping
* documentation
* consider producing a less version. This will be more versatile and will make in-browser compiling possible.
  * or, at least document the sass features being used that don't have a simple less equivalent


## Bugs:

* If $startFluid is false, at4-hide gets immediately overrided by at4-show. In otherwords, there is no reason to ever hide the first breakpoint if $startFluid isn't true.
* If there is a breakpoint at 1 column, it won't use the correct stripe color. It will use the normal stripe color, not the breakpoint color. (why would anyone have a breakpoint at 1?)


## Documentation Notes:

The documentation still needs to be written. Here are some notes to help me remember what needs to be covered.

* using with sass vs using precompiled examples
* variables
* wrapper classes (.conainer, .grid)
* .span*
* .offset*
* .group*
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
  * avoid class conflicts
    * span and group are most likely to cause problems
    * change class shifty class names if need be
  * width must be preserved, so use box-sizing: border-box to prevent padding and borders from making spans wider



## Acknowledgements:

* Many ideas borrowed from [Twitter Bootstrap](http://twitter.github.com/bootstrap/), including class names and grid dimensions.

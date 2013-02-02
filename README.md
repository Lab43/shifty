shifty
======

Shift Grid System

## To Do:

* For stripes, it would be nice to not have to include a .stripes class. In Kickcorps (and probably other real-world project) it's easiest to turn stripes on and off by just changing the sass variable, and not have to also add/remove a class in the html. However, there should still be the option to require a class. This is useful if you want to toggle stripes off and on with javascript. Hmmm... maybe the stripes show unless you add a class to remove them. Is this the best of both worlds?


## Bugs:

* If $startFluid is false, at4-hide gets immediately overrided by at4-show. In otherwords, there is no reason to ever hide the first breakpoint if $startFluid isn't true.
* If there is a breakpoint at 1 column, it won't use the correct stripe color. It will use the normal stripe color, not the breakpoint color. (why would anyone have a breakpoint at 1?)


## Acknowledgements:

* Many ideas borrowed from [Twitter Bootstrap](http://twitter.github.com/bootstrap/), including class names and grid dimensions.
* The [Sass/Compass version of Normalize.css](https://github.com/JohnAlbin/normalize.css-with-sass-or-compass) by [John Albin Wilkins](https://github.com/JohnAlbin) is used in the documentation website.
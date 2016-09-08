# CSS4 Grid: True Layout Finally Arrives
## Jen Kramer
Slides: (slideshare.net/jen4web)[http://www.slideshare.net/jen4web]

-

### Actual problems
Explain why CSS flow doesn't work and its tidius, float

-

### Flexbox
Explain Flexbox
  and a little bit of history
    2009 display: box;
    2011 display: flexbox;
    2014 display: flex;

  and why is awesome

-

### Grid
Grid specification in development
0 browser support
Flexbox is designed for elements or collections
and Grid is thinked for major Layout.

https://drafts.csswg.org/css-grid/

Still buggy on the browser, you could enable it with some flags.

-


```css

.gridable-element {
  display: grid;
    /* That apply the grid into the DOMElement */
  grid-column: 1 / 6;
    /*
      Here comes the magic:
        grid-column allows to spread the space of this element into the horitzontal
        flow.

        Like this:

            +---------------------------------------+
            |                                       |
            |  +---+ +---+ +---+ +---+ +---+ +---+  |
            |  |   | |   | |   | |   | |   | |   |  |
            |  +---+ +---+ +---+ +---+ +---+ +---+  |
            |                                       |
            +---------------------------------------+

          so grid-column will be a notation like X / Y
          being X / Y a precentatge of space on the hole thing
    */

  grid-row: 1 / 2;
    /*
        Sort of the same idea as column, but vertically, something like:

            +------------------+
            |                  |
            | +--------------+ |
            | |              | |
            | |              | |
            | |              | |
            | +--------------+ |
            |                  |
            | +--------------+ |
            | |              | |
            | |              | |
            | |              | |
            | +--------------+ |
            |                  |
            +------------------+
     */

  grid-grap: 10px;
    /* That allows the inner-space between the elements
        Note: In px is the only that actually works, percents breaks so hard.
    */
}

Ref: https://github.com/jen4web/css4grid

-

"So we stoped using tables and we've 15 years fighting with responsive layouts just to define a new spec for making divs behave like tables again"
- Smart Quote

-

Recomemended Resources:

CSS Tricks
Grid by Example: https://gridbyexample.com
W3C Spec: https://www.w3.org/TR/css-grid-1
W3C Editor's Draft Updated Sept 8:
W3C Spec: https://drafts.csswg.org/css-grid

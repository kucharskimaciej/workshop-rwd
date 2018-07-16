# Units in CSS

## Relative units

Most frequently used in CSS, work well for both print and screen.

- `%` - percentage, calculated based on a property (usually the same) of parent
- `em` - relative to the font size of the element (or inherited)
- `rem` - relative to font size of the root element

## Viewport units

The viewport percentage units are relative to the *initial containing block* -- usually the browser window.

- `vw` - 1% of viewport (window) width
- `vh` - 1% of viewport (window) height
- `vmin` - 1% of viewport (window) width **or** height, whichever is **smaller**
- `vmax` - 1% of viewport (window) width **or** height, whichever is **bigger**

## Units in print

When styling the website for print, you should still use relative units, but viewport units are tricky.
On the other hand, you can use absolute units (aside from `px`):

- `cm`, `mm`, `in` - centimeter, millimeter, inch

## Further reading

- [CSS Values and Units Module Level 3](https://www.w3.org/TR/css3-values/#font-relative-lengths)
- [7 CSS Units You Might Not Know About](https://webdesign.tutsplus.com/articles/7-css-units-you-might-not-know-about--cms-22573)
- [Building Resizeable Components with Relative CSS Units | CSS-Tricks](https://css-tricks.com/building-resizeable-components-relative-css-units/)
- [CSS Units Best Practices · GitHub](https://gist.github.com/basham/2175a16ab7c60ce8e001)
- [Taking the “Erm..” Out of Ems](https://webdesign.tutsplus.com/articles/taking-the-erm-out-of-ems--webdesign-12321)
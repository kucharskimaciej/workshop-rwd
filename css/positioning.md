# Positioning elements

## Static

This is the default for all elements. Element will be positioned according to its display property*:
- `display: block` elements will each have own line in the document,
- `display: inline` or `display: inline-block` will be positioned in a single line (with line breaks where appropriate)

*Assuming the element is not floated or a child of `display: flex` parent*

## Relative
```css
.example {
    position: relative;
}
```

Relatively positioned element behaves exactly the same as a statically positioned one,
but it's position can be offset using `top`, `right`, `bottom` and `left` properties:

```css
.box {
    position: relative;
    top: 10px;
    left: 30px;
}
```

## Absolute

```css
.example {
    position: absolute;
}
```

Absolutely positioned element is removed from the document flow: it no longer takes up space on the site.
Like relatively positioned elements it can be offset using `top`, `right`, `bottom` and `left`.

### Positioning context

By default the `position: absolute` element is offset relative to the document body:
it starts at position `0, 0` - the top left corner of the website.
However, if its parent or an ancestor element is positioned relatively,
the absolutely positioned element will be offset relatively to that ancestor:

[](codepen://maciej-kucharski/pQvmXg)

## Fixed

```css
.example {
    position: fixed;
}
```

Behaves the same as `position: absolute`,
but it's positioning context is **always** the browser window, and it cannot be changed.

## Read more

- [CSS Positioning: A Comprehensive Look - Treehouse Blog](http://blog.teamtreehouse.com/css-positioning)
- [CSS - position](http://learnlayout.com/position.html)
- [position | CSS-Tricks](https://css-tricks.com/almanac/properties/p/position/)
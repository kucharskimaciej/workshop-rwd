# Floats

Float is a positioning property, originally intended for describing the flow of text around an image:

[](codepen://maciej-kucharski/bQNQYp)

While now replaced by `flexbox`, the `float`s were used to create a majority of layouts for the past 10 years.

## Normal document flow

For the purpose of explaining the flow: elements are either **block-level** or **inline-level**.
In normal flow, block-level elements are displayed vertically, and inline-level elements are displayed side-by-side.

## Floating elements

A floated element is taken out of a normal flow and moves left or right until it touches the edge of its container or another floated element:

[](codepen://maciej-kucharski/aQzXbd)

## Clearing floats

Clearing floats is a way to force a floated element to move below any other floated elements:

[](codepen://maciej-kucharski/RqNOmg)

## Container collapse

While floated elements are somewhat in the document flow, they don't count towards the container height.
This is especially important when the container only has floated children.

```scss
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

[](codepen://maciej-kucharski/aQvbGq)

## Read more

- [Floats Tutorial | HTML & CSS Is Hard](https://internetingishard.com/html-and-css/floats/)
- [All About Floats | CSS-Tricks](https://css-tricks.com/all-about-floats/)
- [The Clearfix: Force an Element To Self-Clear its Children | CSS-Tricks](https://css-tricks.com/snippets/css/clear-fix/)

# Flexbox

Flexbox is the modern alternative to `floats` when in comes to building layouts.
It gives us complete control on how the elements are positioned, aligned,
what size they are, and how they behave when the page is resized.

## Flex container

```html
<nav class="menu">
    <a class="menu__item">Element 1</a>
    <a class="menu__item">Element 2</a>
    <a class="menu__item">Element 3</a>
</div>

<style>
    .menu {
        display: flex;
    }
</style>
```

The flex container is an element that defines the *flex context* - how the elements inside are positioned, the spacing around them and their orientation.

## Flex items orientation

Flex items can be organized in rows and columns, with option to reverse them, using the `flex-direction` prop:

- `row` (default),
- `row-reverse`
- `column`
- `column-reverse`

```scss
.menu {
  display: flex;
  flex-direction: column;
}
```


## Main axis alignment

Main axis is the main direction of flex items:
- left-to-right for `flex-direction: row`,
- right-to-left for `flex-direction: row-reverse`,
- top-to-bottom for `flex-direction: column`,
- bottom-to-top for `flex-direction: column-reverse`,


Valid values:
- `flex-start` (default),
- `flex-end`,
- `center`,
- `space-around`,
- `space-between`


```scss
.menu {
  display: flex;
  justify-content: center;
}
```

[](codepen://maciej-kucharski/jQWPPz)

## Cross axis alignment

Cross axis alignment of elements can be defined used the `align-items` property -
works the same as the `justify-content`, but in the perpendicular direction.

- `flex-start` (default),
- `flex-end`,
- `center`,
- `baseline`,
- `stretch`

[](codepen://maciej-kucharski/MzKwbZ)

## Tasks

[](codepen://t-i-m-i/wQWOXX)
[](codepen://t-i-m-i/qQNvVZ)
[](codepen://t-i-m-i/yQJwKr)

## Read more

- [Flexbox Froggy - A game for learning CSS flexbox](https://flexboxfroggy.com/)
- [A guide to flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Cheatsheet](https://yoksel.github.io/flex-cheatsheet/)
- [Flexbox Tutorial | HTML & CSS Is Hard](https://internetingishard.com/html-and-css/flexbox/)
- [Cross Axis - MDN Web Docs Glossary: Definitions of Web-related terms | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Cross_Axis)

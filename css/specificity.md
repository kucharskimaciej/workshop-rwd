# Selector specificity

Specificity is a way the browser decides which properties to use for styling when more than one selector applies to the given element .

```html
<h1 id="title" class="page-title" style="font-size: 16px;">Hello!</h1>
```

```css
#title {
    font-size: 24px;
}

.page-title {
    font-weight: 300;
}

h1 {
    font-weight: 700;
}
```

## How to calculate specificity

Specificity can be written as set of four numbers representing respectively:

- inline styles applied to the element (1 or 0)
- number of id attributes in the selector
- number of (pseudo-)classes in the selector
- number of tags (including pseudoelements) in the selector

Examples:

- `#main` - has specificity of `0, 1, 0, 0`
- `.sidebar` - has specificity of `0, 0, 1, 0`
- `a:hover` - has specificity of `0, 0, 1, 1`

The numbers are then compared in order and the higher one wins.

## Overriding styles

Styles can be overridden by either creating a more specific selector:

```scss
article p { /* specificity 0, 0, 0, 2 */
    font-size: 12px;
    font-weight: normal;
}

article p.featured { /* specificity 0, 0, 1, 2 */
  font-size: 14px;
  font-weight: bold;
}
```
or using the `!important` keyword (bad practice):

```css
/* specificity 0, 1, 3, 2 */
#page.page--main.page--default article p.featured {
    font-size: 18px;
}

p { /* specificity 0, 0, 0, 1 */
    font-size: 12px !important;
}
```
## Tasks

[](codepen://t-i-m-i/dQXdEo)
## Further reading

- [Cascade and inheritance - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)
- [CSS Specificity explained | pawelgrzybek.com](https://pawelgrzybek.com/css-specificity-explained/)
# Inheritance of properties

Inheritance in CSS defines what styles are applied to the element
when no value is specified for a property on an element.

## Inherited properties

If no value is set for inherited property take the value from its ancestors.

```html
<article>
    <header>
        <h2>Title</h2>
    </header>

    <p>Lorem ipsum...</p>
</article>
```

```css
article {
    color: red;
}
```

Examples of inherited properties:

- `font-family`
- `word-spacing`
- `list-style`

## Non-inherited properties

If no value set for non-inherited property, it is displayed with an *initial value*.
```css
header {
    border-bottom: 1px solid black;
}
```

## Further reading

- [Inheritance - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/inheritance)
- [Full property table](https://www.w3.org/TR/CSS21/propidx.html)
- [inherit - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/inherit)
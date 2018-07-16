# Syntax and selectors in CSS


## Basic syntax

```css
h1 {
    color: red;
    border: 1px solid black;
}
```

`h1` is a selector, `color` is a property with `red` as its value. 
Similarly `border` is a property, but it's a short-hand - shortcut to writing multiple properties. 
`1px solid black` are the values of abbreviated properties.

## Basic selectors

```css
#title {}

.page-wrapper {}

p {}
```
Each selector will apply to all elements that match:

- `#title` selects elements based on their `id` attribute: `<h2 id="title">`.
- `.page-wrapper` selects elements based on the `class` attribute: `<div class="page-wrapper">`.
- `p` is an element (tag) selector: `<p>`

## Combining selectors

```css
p.featured {}
```

Matches all paragraphs (`p`) that have the `featured` class:
```html
<p class="featured">Lorem ipsum</p>
```

-----

```css
.sidebar a {}
```

Matches all links (`a`) that are inside of an element with the `sidebar` class:

```html
<aside class="sidebar">
    <a href="/">Home</a>
    <nav>
        <a href="/about">About</a>
    </nav>
</aside>
```

## Attribute selectors

Elements can also be select based on a presence or value of an attribute:

```css
a[title] {}

input[type="text"] {}

a[href^="#"] {}

a[href^="http" i] {}
```

- `a[title]` selects all links that have a title attribute (even if it's empty).
- `input[type="text"]` selects text inputs 
- `a[href^="#"]` selects the links that start with `#` character (i.e. internal links)
- `a[href^="http" i]` selects links that start with `http`, ignoring the case (*Http*, *http*, *HTTP*, etc)

## Pseudo-classes

Pseudo-classes let you define styles for element when it's in a special state or position.

```css
selector:pseudo-class {
    property: value;
}
```

```css
a:hover {
    text-decoration: underline;
}
```

## Pseudo-elements

Pseudo-elements are used to insert content before/after the element
or to style a part of an element (eg. first line of a paragraph). Note the double semicolon (`::`).

```css
selector::pseudo-element {
    property: value;
}
```

```css
a[target="_blank"]::after {
  content: "↗";
  color: blue;
}
```

The above code will add an arrow to all links that open in new tab.
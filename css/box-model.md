# Box model

Every piece of content on the website is rendered as a rectangle with 5 properties:

- width
- height
- border
- margin
- padding

Combined, those properties define how an element is presented to the user.

[](codepen://maciej-kucharski/ZmQLbY)

## Width and height

```css
.box {
    background-color: chocolate;
    width: 100px;
    height: 100px;
}
```

### Width

The horizontal size of the box content area. Defaults to:
- `auto` aka the parent width for `display: block` elements
- as much as the content of the element need for `display: inline-block`
- cannot be set `display: inline` elements

### Height

Much the same as `width`, but vertical. The height of an element is determined by element’s content. 
Like `width` it cannot be set for `display: inline` elements.

## Border

Border width around the element's content. It is not included in the element's width, so:
```css
.box {
    background-color: chocolate;
    width: 100px;
    height: 100px;
    border: 2px solid black;
}
```
The box takes up `104px` of space (`100px` of content width + 2 * `2px`).

## Padding

Padding is the space added between the element's content and its border. 
Like the border it is not included in the element's width:

```css
.box {
    background-color: chocolate;
    width: 100px;
    height: 100px;
    padding: 10px;
}
```

The box is now bigger: `220px` × `220px`.

## Margin

Margin is the reserved space around the element:

```css
.box {
    background-color: chocolate;
    width: 100px;
    height: 100px;
    margin: 20px;
}
```

## The `box-sizing` property
```css
.box {
    background-color: chocolate;
    width: 100px;
    height: 100px;
    border: 5px solid red;
    padding: 25px; 
    margin: 20px;
}
```
What are the dimensions of the `.box`? It's `100px + 2*5px + 2*25px == 160px`.

The way CSS calculates elements width is counter-intuitive and often cause of layout problems.
Thankfully it can be changed by using the `border-sizing` property. 
It has two possible values: 
- `content-box` being the default
- `border-box` makes `padding` and `border` included in the element's `width` and `height`

Setting `box-sizing: border-box` on *every* element of the website results in much more 
reasonable result of the above question: `.box` is exactly `100px` wide.

```css
*, *::before, *::after {
    box-sizing: border-box;
}
```

## Read more

- [CSS Box Model for Beginner: Unlocking the Magic of CSS](https://hackernoon.com/css-box-model-45ecf4ac219e)
- [Box Sizing | CSS-Tricks](https://css-tricks.com/box-sizing/)
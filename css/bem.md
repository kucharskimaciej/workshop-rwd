# Class naming convention - BEM

> There are only two hard things in Computer Science: cache invalidation and naming things.
>   
> -- Phil Karlton

Since most projects will have multiple developers or thrid-party stylesheets loaded, there's another issue - classname/selector clashes.

## Block Element Modifier

```css
.block__element--modifier {}
``` 

### Block

A block represents a self-contained part of your website. Examples of blocks: header, content, sidebar, footer, and search.

```css
.header {}
.sidebar {}
```

### Element

An elements is part of the block and makes no sense outside it. Each block contains at least one element.

```css
.header__logo {}
.sidebar__section {}
```

### Modifier

A modifier represents a visual variation of a block. 

```css
.header--sticky {}
.sidebar--wider {}
```

---

```html
<article class="content content--wide">
    <p class="content__text content__text--featured">Lorem ipsum...</p>

    <p class="content__text">Lorem ipsum...</p>
    
    <footer class="content__footer">
        <a href="#" class="content__read-more">Read more</a>
    </footer>
</article>
```

```scss
.content {
  width: 60%;
  background-color: white;
}

.content--wide { /* only styles that differ from normal .content */
  width: 80%;
}

.content__text {
  font-size: 16px;
}

.content__text--featured {
  font-weight: bold;
}

.content__read-more {
  color: #008cff;
  text-decoration: underline;
}

```

## Further reading

- [BEM 101 | CSS-Tricks](https://css-tricks.com/bem-101/)
- [How to Use BEM Methodology | Toptal](https://www.toptal.com/css/introduction-to-bem-methodology)
- [BEM by Example | Sparkbox | Web Design and Development](https://seesparkbox.com/foundry/bem_by_example)
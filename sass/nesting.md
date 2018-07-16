# Nesting CSS selectors and rules

## Basic nesting

Selectors in Sass can be nested:

```scss
.parent {
  background-color: red;

  .child {
    font-size: 12px;
  }
}
```

The above code compiles down to:

```css
.parent {
    background-color: red;
}

.parent .child {
    font-size: 12px;
}
```

There's no limit on number of levels in nesting, but it needs to be used with caution and
a common practice is to keep it at maximum 3 or 4 - selectors like that may result in specificity issues.

## The `&` operator

The `&` symbol tells Sass to repeat the whole parent selector. 
This way you can chain classes using the nesting syntax:

```scss
.parent {
  &.child { // resulting selector: .parent.child
    background-color: blue;
  }
}
```

It can also be used to generate compound selectors (think BEM):

```scss
.parent {
  &--highlighted { background-color: coral; } // .parent--highlighted
  &__child-element { background-color: blue } // .parent__child-element
}
```

Note: the resulting selector is using **only one class** - extremely useful from scalability perspective.

It can also be used to style the element differently based on a class higher-up the DOM tree:

```scss
.overlay {
  width: 60%;

  body.page--wide & {
    width: 80%;
  }
  
  // modernizr flag
  .no-js & {
    display: none;
  }
}
/*
 .overlay { width: 60%; }
 body.page--wide .overlay { width: 80%; }
 .no-js .overlay { display: none; }
 */

```

## Read more
- [Beware of Selector Nesting in Sass — SitePoint](https://www.sitepoint.com/beware-selector-nesting-sass/)
- [The Sass Ampersand | CSS-Tricks](https://css-tricks.com/the-sass-ampersand/)


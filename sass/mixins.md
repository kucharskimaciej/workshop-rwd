# Mixins

Mixins are used to make a set of properties reusable.

## `@mixin` directive syntax
The mixin directive syntax is very similar to that of a function:

```scss
@mixin mixin-name([...arguments]) {
  property: value;
  
  selector {
    property: value;
  }
}
```

```scss
@mixin overlay($background-color: transparent) {
  bottom: 0;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  background-color: $background-color;
}

.product__link-overlay {
  @include overlay;
}

.modal-background {
  @include overlay(rgba(0, 0, 0, .8));
}
```

## The `@content` directive

Using the `@content` you can pass css properties to a mixin.

```scss
@mixin button() {
  display: inline-block;
  border-radius: 2px;
  padding: 8px 10px;
  font-size: 16px;
  text-decoration: none;
  @content;
}

.success {
  @include button {
    background: #228b22;
    color: #fff;
  }
}

.cancel {
  @include button {
    background: #778899;
    color: #f8f8f8;
  }
}
```

## Read more

- [Anatomy of a mixin | Sass in the Real World: book 1 of 4](https://anotheruiguy.gitbooks.io/sassintherealworld_book-i/handy-tools/anatomy-of-a-mixin.html)
- [Sass Basics: The Sass Mixin Directive — SitePoint](https://www.sitepoint.com/sass-basics-the-mixin-directive/)
- [How to Use Sass Mixins ― Scotch](https://scotch.io/tutorials/how-to-use-sass-mixins)
- [Sass mixins - Free tutorial to learn HTML and CSS](https://marksheet.io/sass-mixins.html)
- [10 SASS (SCSS) mixins you should be using in your projects](https://engageinteractive.co.uk/index.php/blog/top-10-scss-mixins)
- [Helpful SASS Mixins | Responsive Web Design](https://responsivedesign.is/articles/helpful-sass-mixins/)
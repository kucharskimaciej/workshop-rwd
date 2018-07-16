# Variables

## Defining variables

Variables in `scss` files start with the `$` sign:
```scss
$variable-name: variableValue;
```

Any valid css value can be used:
```scss
$pretty-blue: #1d90ff;

$primary-color: $pretty-blue;
$secondary-color: #fce473;

$serif: "Times New Roman", Georgia, serif;
$sans-serif: "Roboto", "Source Sans Pro", "Open Sans", Arial, sans-serif;

$column-spacing: 20px;
```

## Using variables

The variable value will replace the variable during compilation:

```scss
.featured {
  color: $primary-color;
  font-face: $sans-serif;
  border-bottom: 1px solid $secondary-color;
}
```

will be compiled to:

```css
.featured {
  color: #1d90ff;
  font-face: "Roboto", "Source Sans Pro", "Open Sans", Arial, sans-serif;
  border-bottom: 1px solid #fce473;
}
```

## Variable scope

All variables that are declared outside functions or mixins (more on that later) are **global**:

```scss
$border-width: 1px;

.button--wide-border {
  $border-width: 2px; // intent: set the border with just for the current selector
  
  border-width: $border-width;
}

// later in code
.featured {
  border: $border-width solid green; // $border-width is actually 2px, not 1px
}
```

Since SASS version 3.3, reassigning variable value in such way will result in compilation warning.

## The `!default` flag

A variable can be defined with the `!default` flag:

```scss
$column-spacing: 30px !default;
```

The new `$column-spacing` variable value (`30px`) will only be assigned if it's the first time the variable is defined.

## Read more

- [Sass variables - Free tutorial to learn HTML and CSS](https://marksheet.io/sass-variables.html)
- [Setting variables | Sass in the Real World: book 1 of 4](https://anotheruiguy.gitbooks.io/sassintherealworld_book-i/handy-tools/setting-variables.html)
- [Variable scoping | Sass in the Real World: book 1 of 4](https://anotheruiguy.gitbooks.io/sassintherealworld_book-i/handy-tools/variable-scoping.html)
- [!default and !global | Sass in the Real World: book 1 of 4](https://anotheruiguy.gitbooks.io/sassintherealworld_book-i/handy-tools/default-flag.html)
# Functions

Exactly as you'd expect a function takes in a number of arguments and returns a value. Here's the `@function` directive syntax:

```scss
@function function-name([...arguments]) {
  // logic
  @return value
}
```

```scss
$base-font-size: 16px;

html {
 font-size: $base-font-size;
}

@function rem($value, $base: $base-font-size) {
  @return $value/$base * 1rem;
}
```
## Read more

- [Sass Basics: The Function Directive — SitePoint](https://www.sitepoint.com/sass-basics-function-directive/)
- [How To Write Your Own Custom Sass Functions](https://vanseodesign.com/css/custom-sass-functions/)
- [Using pure Sass functions to make reusable logic more useful](http://thesassway.com/advanced/pure-sass-functions)
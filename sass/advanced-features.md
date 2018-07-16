# Flow control and lists

## `@if` and `@else`

```scss
@mixin button($border: none) {
    display: inline-block;
    border-radius: 2px;
    padding: 8px 10px;
    font-size: 16px;
    text-decoration: none; 
    
    @if $border == thin {
      border-width: 1px;
    } 
    @else if $border == wide {
      border-width: 2px;
    }
    @else {
      border-width: 0;
    }
}

.button {
  @include button(wide);
}

```

## `@for`

```scss
$number-of-columns: 12;

@for $i from 1 through $number-of-columns {
  .column-#{$i} {
    width: $i * (100%/$number-of-columns);
  }
}
```

## Lists

Lists in Sass can contain any type of value and the syntax is not very strict. 
All of the definitions below have the same result:

```scss
$list: item-1 item-2 item-3;
$list-with-commas: item-1, item-2, item-3;
$list-in-parens: (item-1, item-2, item-3);
```

Lists can be nested:

```scss
$nested: (
  (item-1, item-2, item-3),
  (item-4, item-5, item-6)
);

$nested-too: item-1 item-2 item-3, item-4 item-5 item-6
```

**Important**: indexes in lists start at 1.

## Looping over lists with @each

```scss
$pages: (
  (home wide),
  (article normal),
  (gallery wide)
);

@mixin page($size: normal) {
  margin: 0 auto;
  
  @if $size == wide {
    width: 80%;
  }
  @else {
    width: 60%;
  }
}

@each $page-name, $page-size in $pages {
  .page-#{$page-name} {
    @include page($page-size);
  }
}
```

Outputs:

```css
.page-home {
  margin: 0 auto;
  width: 80%;
}

.page-article {
  margin: 0 auto;
  width: 60%;
}

.page-gallery {
  margin: 0 auto;
  width: 80%;
}
```

## Maps

Very similar to lists, but with slightly stricter syntax. 
Properties of a map can be accessed using the `map-get` function:

```scss
$pages: (
  home: (
    size: wide,
    background: white
  ),
  article: (
    size: normal,
    background: #f8f8f8
  )
);

@mixin page($size: normal) {
  margin: 0 auto;
  
  @if $size == wide {
    width: 80%;
  }
  @else {
    width: 60%;
  }
}

@each $page-name, $properties in $pages {
  .page-#{$page-name} {
    @include page(map-get($properties, size));
    background: map-get($properties, background);
  }
}
```

## Read more
- [Sass control directives: @if, @for, @each and @while](http://thesassway.com/intermediate/if-for-each-while)
- [Advanced SCSS, or, 16 cool things you may not have known your stylesheets could do · GitHub](https://gist.github.com/jareware/4738651)
- [Understanding Sass lists](https://hugogiraudel.com/2013/07/15/understanding-sass-lists/)
- [Lists in Sass: syntax and use cases with examples – clubmate.fi](http://clubmate.fi/lists-in-sass-syntax-and-use-cases-with-examples/)
- [Sass Maps vs. Nested Lists — SitePoint](https://www.sitepoint.com/sass-maps-vs-nested-lists/)
# Just enough jQuery to survive

## Selecting elements

```html
<header class="page__header">
    <a class="page__header__logo" href="/">Company</a>

    <nav class="page__header__nav>
        <a class="page__header__nav__item" href="#">Item</a>
        <a class="page__header__nav__item" href="#">Item</a>
        <a class="page__header__nav__item" href="#">Item</a>
    </nav>
</header>
```
```js
$('a'); // select all links on the page
var $header = $('.page__header__nav'); // select the navigation
$('a', $header); // select the links in the navigation, or:
$header.find('a');
```

## Handling events

```js
$('.js-log').on('click', function(event) {
    console.log('click!', event.target);
});
```

## Run code after the HTML is ready
A lot of the code will depend on the DOM Tree (representation of HTML in JS).

```js
$(document).ready(function() {
    // run the code
});

// or

$(function() {
    // run the code
});
```

## Using custom plugins

After including the plugin in the bundle, it will be available on the jQuery object:

```js
$('selector').plugin();
```


# Components

The Bootstrap is primarily an UI component library.
Provided components span from very simple ones like buttons or badges to more complicated like carousels and modals.

There are components that require some javascript to be provided. There are also some dependencies:
- all components use jQuery,
- all components require Bootstrap's `util.js` helpers,
- Dropdowns, popovers, and tooltips require the Popper.js library
Both those libs need to be included before the component code.

## Using simple components

Those components are just some classes and appropriate HTML structure:

```html
<div class="card">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <h6 class="card-subtitle">Card subtitle</h6>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>
  </div>
</div>
```

## Using components with JS

On top of having a set HTML structure
some of the components are using custom `data-*`
attributes to [provide hooks for JavaScript](https://github.com/twbs/bootstrap/blob/v4-dev/js/src/dropdown.js#L512):

```html
<div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle"
          type="button" id="dropdownMenuButton"
          data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown button
  </button>
  <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
    <a class="dropdown-item" href="#">Lorem</a>
    <a class="dropdown-item" href="#">Ipsum!</a>
    <a class="dropdown-item" href="#">Dolor sit</a>
  </div>
</div>
```

Alternatively, the plugin can be initialized directly via JS:
```js
$('.dropdown-toggle').dropdown();
```

Many of the components accept options when initializing,
enable a programmatic API and emit custom events.
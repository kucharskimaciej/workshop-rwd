# Grid

Sophisticated and responsive grid system is the main feature of the Bootstrap framework.

## Simple columns

Create equal width columns

```html
<div class="row">
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
    <div class="col">Column</div>
</div>
```

Define the width of the columns (example assumes the total number of columns to be 12):

```html
<div class="row">
    <div class="col-6">Column</div>
    <div class="col-6">Column</div>
    <div class="col-8">Column</div>
    <div class="col-4">Column</div>
</div>
```

The columns will wrap if they don't fit the row.

## Responsive columns

```html
<div class="row">
    <div class="col-sm-6 col-md-4 col-lg-3">Item</div>
    ...
</div>
```

Columns in this grid will:

* take 25% width on desktops (large screens)
* take 33% width on tablets (or landscape phones)
* take 50% width on large phones
* take the full row on small phones

## Container
```html
<div class="container">
    <!-- content -->
</div>
```

The `.container` class provides a wrapper for the main page content.
Centers the content and provides some horizontal padding.

## Tasks

[](codepen://maciej-kucharski/xQdxyy)

## Read more

* [Grid system - Bootstrap](https://getbootstrap.com/docs/4.1/layout/grid/)

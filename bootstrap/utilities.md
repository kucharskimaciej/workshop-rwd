# Utilities

## Reboot

The library comes built into Bootstrap and provides a default,
consistent across the browsers styling of basic HTML elements.

## Responsive images

Basic technique for responsive images is implemented out of the box:

```html
<img class="img-fluid" src="...">
```

The `.img-fluid` class applies `max-width: 100%; height: auto`
styling so that the image resizes properly.

## Display classes

Provides classes that can change the display property of the element, based on breakpoint:

```
<div class="d-none d-md-block">...</div>
```

The `div` will be hidden for phones and visible for tablets and desktops.

## Aspect ratio

While primarily used for embedding external media, can be also used to force aspect ratio for custom elements:

<div class="embed-responsive embed-responsive-1by1">
  <div class="embed-responsive-item">This will always be square</div>
</div>

Available aspect-ratio classes are created based on the
`$embed-responsive-aspect-ratios` variable in Bootstrap's config.

## Read more

* [Reboot](https://getbootstrap.com/docs/4.1/content/reboot/)
* [Images](https://getbootstrap.com/docs/4.1/content/images/)
* [Display](https://getbootstrap.com/docs/4.1/utilities/display/)
* [Aspect Ratio](https://getbootstrap.com/docs/4.1/utilities/embed/)
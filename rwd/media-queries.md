# Media queries

Media queries let you apply different styles to an element based on device size, orientation, type, and pixel density.
The media query is, in essence, an `if` statement about the browser/device properties: 
if the statement evaluates to `true`, the styles inside will be applied:

```scss
@media screen and (min-width: 600px) {
  // styles to apply
}
```

### Media type

```scss
@media print { ... }
```

Describes a general category of the device that displays the page:

- `all` - the default value, applies to all devices
- `screen` - applies to devices that display the page on a screen (computers! phones!)
- `print` - used when printing and in print preview
- `speech` - intended for speech synthesizers.

### Dimensions

```scss
@media (min-width: 640px) { ... }
```

Describe the size of the browser window: `width`, `height`. 
Can be modified with `min-` and `max-` prefixes (`min-width`, `min-height`, `max-width`, `max-height`)


### Orientation and aspect ratio

```scss
@media (orientation: landscape) { ... }
@media (orientation: portrait) { ... }
@media (aspect-ratio: 16/9) { ... }
```

- `orientation: landscape`: the device is wider than it's tall
- `orientation: portrait`: the device is taller than it's wide
- `aspect-ratio: width/height`: ratio of device width to it's height. Can be prefixed with `min-` and `max-`.

## Read more

- [CSS Media Queries & Using Available Space | CSS-Tricks](https://css-tricks.com/css-media-queries/)
- [Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
- [Media Queries](https://mediaqueri.es/)
- [Media Queries for Standard Devices | CSS-Tricks](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/)
- [Logic in Media Queries | CSS-Tricks](https://css-tricks.com/logic-in-media-queries/)
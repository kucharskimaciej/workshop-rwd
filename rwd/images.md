# Responsive images

Displaying images on different devices comes with three problems: 
 
 - the file size problem,
 - the cropping problem (aka art direction problem),
 - and the resolution scaling problem (aka device pixel ratio problem)

## The minimum solution

Make the image scale with the size of its parent:

```scss
.responsive-image {
    display: block;
    max-width: 100%;
}
```

This solution doesn't really solve any of the problems above, but at least the image doesn't break the layout.

## Using background

Instead of using an image, the background-image will be used. This allows for finer control over the image with CSS and/or JS:

```html
<div class="image"></div>
```

```css
.image {
    background-image: url('https://placeimg.com/640/480/any');
}

@media (max-width: 640px) {
    .image {
        background-image: url('https://placeimg.com/320/240/any')
    }
}
```

Pros:
- solves all the above problems

Cons 
- it's hard to generate this code automatically
- it's hard to keep the image in correct proportions
- bad for SEO and screen readers
 
## Using the `srcset` attribute

The `srcset` let's you define list of sources for the `<img>` tag and
have the browser decide which to use based on the device pixel-ratio:

```html
<img src="product.jpg" srcset="product.jpg 1x, product-2x.jpg 2x"> 
```

In this case the `product.jpg` will be used for regular screens and the `product-2x.jpg` for retina displays.

For more control over which image is actually loaded, you can use the `w` descriptor:

```html
<img src="medium.jpg" 
     srcset="small.jpg 500w, medium.jpg 1000w, large.jpg 2000w">
```

The `w` descriptor tells the browser how wide an image is (in pixels). 
The browser then runs the following calculations (assumed device width: 400px) to get device pixel-ratio for all the files:
 
 - `500/400 = 1.25`
 - `1000/400 = 2.5`
 - `2000/400 = 5`

## Using the `<picture>` element

Used to get even more fine-grained control over which file to load:

```html
<picture>
    <source srcset="small.jpg" media="(max-width: 500px)">
    <source srcset="medium.jpg" media="(max-width: 1000px)">
    <source srcset="large.jpg" media="(min-width: 1001px)">
    <img src="medium.jpg">
</picture>
```

## Read more

- [Responsive Images: If you’re just changing resolutions, use srcset. | CSS-Tricks](https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/)
- [\<picture>: The Picture element - HTML: HyperText Markup Language | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)
- [Responsive Images Tutorial | HTML & CSS Is Hard](https://internetingishard.com/html-and-css/responsive-images/)
- [How to Build Responsive Images with srcset — SitePoint](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)
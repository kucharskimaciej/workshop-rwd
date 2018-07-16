# Browser inconsistencies

Modern browsers render elements and handle styles (mostly) according to standards. 
The differences come from different default styles applied to browsers 
or bleeding-edge features not being supported: the latest versions of the popular browsers can do some awesome things which older browsers can’t – but they still have to be supported. 

## Handling default browser styles

Each browser applies some styling to most common elements like lists, links or inputs. 
Trouble: each browsers applies *different* styling to those elements. 
To make sure they are rendered consistently and in-line with modern standards it's best to use an already prepared stylesheet:

- [reset.css](https://github.com/shannonmoeller/reset-css) - drop all styling for the elements. Very invasive, but small. Requires you to write styles for everything.
- [normalize.css](https://necolas.github.io/normalize.css) - set same styles for the elements in every browser. 
- [sanitize.css](https://github.com/csstools/sanitize.css) - slightly less obtrusive version of the above

## Checking for feature support

The go-to solution for checking browser support and other usefull info for a feature is [Can I Use...](caniuse.com). 
You can also find a per feature summary (based on *Can I Use* and user experiences) on [HTML5 Please!](http://html5please.com/). 

## Detecting if a feature is supported programmatically

[Modernizr](https://modernizr.com/) is a collection of tests that run against the user browser as it loads your page. 
Those tests detect if a given features is supported or not and add an appropriate class the `html` element.

## Read more 

- [Modernizr Documentation](https://modernizr.com/docs)
- [CSS Normalize & CSS Reset – Daphne Watson – Medium](https://medium.com/@DaphneWatson/css-normalize-css-reset-which-one-do-you-prefer-6e8cc593ac41)
- [Using Normalize.css For Homogeneous Development - Hongkiat](https://www.hongkiat.com/blog/normalized-css/)
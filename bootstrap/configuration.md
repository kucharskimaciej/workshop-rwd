# Configuring Bootstrap

The assumption here is that the project is building the Bootstrap framework
using it's own build tool and is using the SCSS source files instead of precompiled CSS.

## Import what's needed

Bootstrap's [`bootstrap.scss` file](https://github.com/twbs/bootstrap/blob/9201a805101943f9ec088639d520d7d2874bbed1/scss/bootstrap.scss) includes the whole framework:

```scss
/*!
 * Bootstrap v4.1.3 (https://getbootstrap.com/)
 * blah, blah...
 */

@import "functions";
@import "variables";
@import "mixins";
@import "root";
@import "reboot";
@import "type";
@import "images";
@import "code";
@import "grid";
@import "tables";
@import "forms";
@import "buttons";
@import "transitions";
@import "dropdown";
@import "button-group";
@import "input-group";
@import "custom-forms";
...more imports!
```

**Ignore that file**. Create a custom import file, and only import components/parts that are really needed:

```scss
@import "../node_modules/bootstrap/scss/functions";
@import "../node_modules/bootstrap/scss/variables";
@import "../node_modules/bootstrap/scss/mixins";
@import "../node_modules/bootstrap/scss/root";
@import "../node_modules/bootstrap/scss/reboot";
@import "../node_modules/bootstrap/scss/type";
@import "../node_modules/bootstrap/scss/images";
// @import "code"; -- not imported
@import "../node_modules/bootstrap/scss/grid";
@import "../node_modules/bootstrap/scss/tables";
@import "../node_modules/bootstrap/scss/forms";
@import "../node_modules/bootstrap/scss/buttons";
// @import "transitions"; -- no animations needed
@import "../node_modules/bootstrap/scss/dropdown";
// @import "button-group"; -- not even once
@import "../node_modules/bootstrap/scss/input-group";
@import "../node_modules/bootstrap/scss/custom-forms";
```

## Theme

The above file links to [`_variables.scss`](https://github.com/twbs/bootstrap/blob/9201a805101943f9ec088639d520d7d2874bbed1/scss/_variables.scss)

```scss
@import "../node_modules/bootstrap/scss/variables";
```

Instead of using variables straight from bootstrap,
the values should be copied over to a separate file and modified as needed.

Import the file instead of the original:

```scss
@import "./project-variables";
```

Special attention variables:

* `$theme-colors` - the primary colors used by bootstrap
* `$grid-breakpoints` and `$container-max-widths` - control the responsiveness of the website
* `$font-size-base` and `$font-family-*` - typography

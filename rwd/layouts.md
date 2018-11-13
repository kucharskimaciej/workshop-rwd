# Fluid layouts

The main takeaway of the responsive design is that it's one page that fits all sizes.
That means that all elements on the page should scale with the size (width) of the device.

### Fluid grid

Layout element sizes should not be hardcoded. Use `%` instead:

```scss
.column-1 {
    // ...
    width: 25%;
}
```

### Other units

All other units should also be replaced with a relative unit, preferably `rem` or `%`:

```scss
.column-1 {
    // ...
    padding: 0 .5rem;
}

h1 {
    font-size: 3rem;
    border-bottom: 1px solid black;
}

h1 small {
    font-size: 60%; // or 0.6em
}

.logo {
    width: 5rem;
    height: 5rem;
    margin-right: 2rem;
}
```

### Scaling the layout

Provided the layout is coded with relative units and `rems` or `ems` are used wherever possible, scaling it is just a matter of a simple query:

```scss
html {
    font-size: 16px;
}

@media (max-width: 40rem) { //  < 640px
    html {
        font-size: 12px;
    }
}
```

## Tasks
[](codepen://maciej-kucharski/xQgVYY)

## Read more
- [PX, EM or REM Media Queries? | Zell Liew](https://zellwk.com/blog/media-query-units/)
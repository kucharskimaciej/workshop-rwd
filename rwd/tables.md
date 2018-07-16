# Responsive tables

Tables are hard to present on mobile -- the screen is small and tables typically hold large amounts of data.
There is however a number of ways data tables can be made useful on mobile devices.

## Simple overflow

The main issue with rendering tables on small screens is just that they don't fit horizontally. 
Let's fix that by adding a scroll if the table is too wide:

```scss
.table--overflow {
    display: block;
    overflow-x: auto;
    max-width: 100%;
}
```

[](codepen://maciej-kucharski/QByMJd)

## Flipping the table

The above solution has only one problem - the user can't see the headers if table has many rows. 
This approach mends that issue, but complicates the code:

[](codepen://maciej-kucharski/mjVMNy)

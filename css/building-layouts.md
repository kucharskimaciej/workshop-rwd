# Building layouts

Most modern layout are build based on a grid:

## Float-based grids

Used mostly for compatibility with browsers that don't support flexbox.
Downside of using floats is having to manage columns of different height.

```scss
.row {
    margin: 0 -10px;
}

// clear floats
.row::after {
    content: "";
    display: table;
    clear: both;
}

.column-1,
.column-2,
.column-3,
.column-4,
...so on {
    padding: 0 10px;
    float: left;
}

.column {
    width: 25%;
}

.column-2 {
    width: 50%;
}

...so on
```

[](codepen://maciej-kucharski/rQOOyy)

## Flex grid

Current standard is using `flexbox` for grids, which allows finer control over how the grid is displayed while not having same issues as floats.

[](codepen://maciej-kucharski/GwpJMy)




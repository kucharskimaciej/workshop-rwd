# Desktop first vs mobile first approach

The difference between those approaches is how you architect your CSS code, especially the which media queries are used.

## Desktop first

Desktop first approach means that the code is written for the desktop
version of the website and later "fixed" so it looks good on mobile devices.
Dead give-away of such code are `max-width` media queries:

```scss
.post__title {
  font-size: 8rem;
  
  @media (max-width: 40rem) {
    font-size: 4rem;
  }
}
```

## Mobile first

This approach requires you to first code the website for mobile and then make appropriate changes for desktop.
Most media queries will have the `min-width` condition:

```scss
.post__title {
  font-size: 4rem;
  
  @media (min-width: 40rem) {
    font-size: 8rem;
  }
}
```

## Read more

- [Mobile First Design: Why It’s Great and Why It Sucks - Top Digital Agency | San Francisco & Austin](https://mayvendev.com/blog/mobilefirst)
- [How To Write Mobile-first CSS | Zell Liew](https://zellwk.com/blog/how-to-write-mobile-first-css/)
- [Mobile-first CSS – mrmrs – Medium](https://medium.com/@mrmrs_/mobile-first-css-48bc4cc3f60f)
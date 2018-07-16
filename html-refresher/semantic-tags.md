# Semantic tags in HTML

## Layout elements
* `header`
	* page header
	* header of an `article` or a `section`
* `nav`
	* navigation bar
* `aside`
	* sidebar
* `section`
	* grouping of content
	* usually has a header
* `article`
	* independent part of the content
	* internet forum post
	* article in a newspaper
	* blog entry
	* should have a header `header`
* `footer`
	* defines a footer for a document/`section`/`article`

### Elementy dot. zawartości
* `main`
	* main part of the content
	* applies both the the whole document and any `article`s/`section`s
* `figure`
	* illustrations
	* diagrams
	* photos
	* code blocks
* `figcaption`
	* caption for a figure
* `pre`
	* preformatted text
	* keeps whitespaces
	* usually displayed with monospace font


## Stop using
* `center`, `font`, `big` - use CSS instead
* `i` - use `em` to signify emphasis
	* the `i` element is used for icons (breaking rules, but very popular)
* `b` - use `strong` instead
* `u` - use CSS
* `s` and `strikethrough` - use `del` to signify removed text. If used just for the strikethrough effect — use CSS.
* `small` can be used, but for side comments (disclaimers, notes, etc), not for styling


## Further reading

- [HTML5 semantic elements and Webflow: the essential guide | Webflow Blog](https://webflow.com/blog/html5-semantic-elements-and-webflow-the-essential-guide)
- [An Overview of HTML5 Semantics by Michelle on CodePen](https://codepen.io/mi-lee/post/an-overview-of-html5-semantics)

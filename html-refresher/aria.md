# ARIA

ARIA stands for *Accessible Rich Internet Applications*. It's a set of attributes that can be added to
HTML elements with goal of improving the website accessibility by clearly communicating role, state or other properties of the element.

## ARIA landmark roles
Identify the purpose the element serves, more than just the element tag.

* `role="banner"` contains main heading/title of the page — used on `header` element. One per page.
* `role="complementary"` — additional section of the page, used on `aside` element
* `role="contentinfo"` — element that contains additional information about the document content. One per page, typically on a `footer` element
* `role="form"` — element that contains form control; do not use on actual `form` element, but rather on containers for standalone controls
* `role="main"` the main content of the component; usually on the `main` element. One per page
* `role="navigation"` contains links/other navigation elements. Usually on `nav` element
* `role="search"` search for the document; typically a form

## Other ARIA role attributes
* `role="button"` mark elements other than `<button>` as buttons. Sometimes useful
	* Elements marked with this role can also use `aria-pressed` attribute to signify the button state (ie. toggle buttons)
	* should have `aria-label` or `aria-labelledby` attribute, especially if content doesn’t describe the action well (ie. close button with ‘x’ as a content)
* `role=“combobox”`, `role=“listbox”`  mark elements that allow to select options, that are not standard `<select>` — ie. typeahead, custom dropdown implementation
* `role=“option”` use within the above; mark an option of a custom dropdown.
* `role=“dialog”` custom modals
* `role=“checkbox”`, `role=“radio”` custom elements that represent checkboxes and radio buttons. `aria-checked` attribute to provide the state of the element
*  `role=“toolip”`

## Further reading
- [The Roles Model | Accessible Rich Internet Applications (WAI-ARIA) 1.0](https://www.w3.org/WAI/PF/aria/roles)
- [Using ARIA - Accessibility | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques)
- [Using the aria-label attribute - Accessibility | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)
- [Using the aria-labelledby attribute - Accessibility | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-labelledby_attribute)
- [Using the button role - Accessibility | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_button_role)
- [How to Use ARIA Effectively with HTML5 — SitePoint](https://www.sitepoint.com/how-to-use-aria-effectively-with-html5/)


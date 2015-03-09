---
title: CSS Selectors
---

## CSS Selectors

### Type Selector

There are a few different types of selectors. The simplest selector is the type selector. The **type selector** will select all XHTML tags on a page which are of a certain type. For example, this selector is appropriate for selecting all images on the page. To use the type selector

> *Note*: For more information on the type selector, view the official [W3C Documentation](http://www.w3.org/TR/CSS21/selector.html#type-selectors).

**Example: Making all Paragraphs use Blue Text**

If your XHTML contains the following code:

```html
<p>
  Hello, world.
</p>
<p>
  This is a paragraph.
</p>
```

And is linked to a CSS file containing the following code:

```css
p {
  color: #0000FF;
}
```

Then the webpage will appear like this:

> <p style="color:#0000FF;">
>   Hello, world.
> </p>
> <p style="color:#0000FF;">
>   This is a paragraph.
> </p>

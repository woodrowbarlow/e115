---
title: In-Line Styling
---

## In-Line Styling

The simplest way of applying CSS rules to an element is to simply inject the rule directly into the element's tag in the XHTML document. This is done by means of an attribute which has not been previously discussed, but which can be applied to any XHTML tag: the style attribute.

In an XHTML document, the style attribute can be added to any tag, and the value of that attribute is a list of CSS rules. Those CSS rules will be applied to the element in question.

**Example: Making a Paragraph use Bold Arial Font**

The following code:

```html
<p style="font-family: Arial; font-weight: bold;">
  This paragraph has bold text in the Arial font.
</p>
```

Would produce the following result:

> <p style="font-family: Arial; font-weight: bold;">
>   This paragraph has bold text in the Arial font.
> </p>

**Example: Adding a Border to an Image**

The following code:

```html
<img src="images/ncsu.png" alt="NCSU Logo" style="border: 3px dashed #000000" />
```

Would produce the following result:

> <img src="../9/images/ncsu.png" alt="NCSU Logo" style="border: 3px dashed #000000" />

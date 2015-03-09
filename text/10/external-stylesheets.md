---
title: External Stylesheets
---

### Setting Up an External Stylesheet

CSS is usually used by creating a stylesheet file and linking your XHTML code to that file. The stylesheet file will contain a list of rules, and selectors which define what parts of the XHTML code the rules apply to. To begin, create a new blank text file, save it with a `.css` file extension, and store it somewhere in your `www` directory. Now you will need to add a special XHTML tag (shown below) somewhere in the head section of any webpages which will use your CSS styles. This tag links your webpage to your stylesheet.

```html
<link href="style.css" rel="stylesheet" type="text/css" />
```

Make sure that you've put this tag in the head section of your webpage (not the body section), and that the value of the `href` attribute contains a path to the CSS file you've just created. Repeat this for any pages you want to style with your CSS file.

### Stylesheet Syntax

The stylesheet is organized into "blocks" of CSS rules. Each block is composed of a selector, followed by a list of rules enclosed with curly braces (`{` and `}`). A CSS **selector** is a way of defining the scope of the rules; in other words, a selector defines to which elements the rules will be applied. The example below shows the generic syntax of a stylesheet.

```css
/* this is a block of CSS rules */
selector {
  property: value;
  property: value;
}

/* this is another block */
selector {
  property: value;
  property: value;
}
```

> *Note*: In CSS, lines that begin with `/*` and end with `*/` are *comments*. Just like XHTML comments, they have no impact on the webpage; they are only displayed in the code and are meant to add documentation or any other notes to the code.

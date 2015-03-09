---
title: CSS and Styling
---

# Basic Web Pages

 * [Introduction](introduction.html)
 * [Formatting Tags](formatting-tags.html)

## Introduction to CSS

### What is CSS?

We learned in the last chapter than XHTML is used to categorize data in a way that the browser can make meaningful inferences; for example, the browser can guess that a heading tag should be displayed big and bold. CSS, or **Cascading Style Sheets**, is a way of overriding the browser's default display style. In other words, CSS allows us to write a set of rules which define exactly how to display a particular type of data on a website. A CSS rule might translate to something like "display all paragraphs in the Arial font".

### Practical Applications

Beyond the ability to customize, CSS provides the ability to easily create a consistent look and feel across an entire website very easily. A website can use one CSS file for every page - each page will have its own unique data and information, but all pages will have a similar appearance, and changing the appearance for the entire website can be done instantly by modifying a single file. This consistency helps your website to maintain a unified visual theme or brand, providing an easy end-user experience for visitors.

### More Information

Like XHTML, all features of the CSS rules language are standardized by the World Wide Web Consortium (the W3C). The most recent major language version for CSS is CSS3, but new sets of rules are being accepted as part of the official language all the time. W3C provides an online tool that anyone can use in order to test whether a piece of CSS code is completely valid, called the [CSS Validation Service](https://jigsaw.w3.org/css-validator/).

Because CSS is constantly evolving (even faster than XHTML), this textbook will introduce you to the syntax and uses of CSS and will discuss the most frequently used CSS rules. The content discussed in this textbook is a very small subset of what is possible in CSS, and, for further reading, one might peruse the [Mozilla Developer Network's CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS) or the [Official W3C Language Specification](http://www.w3.org/TR/CSS/).

### Important Programs

CSS files are written using plain-text editors, just like XHTML files. Most text editors which are specialized for editing HTML and XHTML documents also have specialized features for editing CSS files. One such recommended text editor for Windows users is [Notepad++](http://notepad-plus-plus.org/); an equivalent software for Mac OSX is [TextWrangler](http://www.barebones.com/products/textwrangler/download.html).

### Learning Objectives

 * Learn to override the browser's default presentation style using CSS rules.
 * Understand selector scope, and utilize name, id, and class selectors.
 * Learn to define sizes and colors on the screen using accepted units.
 * Create a consistent style across multiple web pages using an external stylesheet.
 * Use the style attribute to handle edge cases.

## XHTML Formatting Tags

XHTML has a few in-line text tags that are rendered in the browser as basic text effects (like bold or italic text). These tags do not utilize CSS (although the browser could be told to render them differently via CSS). These tags are detailed below because of their usefulness in styling a webpage's content.

### Strongly Important (Bold) and Emphasized (Italic) Text

The **strong text tag** is used to denote that certain words or phrases within a paragraph (or any chunk of text) are strongly important. By default, the browser displays strong text as bold.

The **emphasized text tag** is used to emphasize certain words or phrases within a paragraph or any chunk of text. By default, the browser displays emphasized text as italic.

> *Caution*: Some older textbooks use the tags `b`, `i`, and `u` to create bold, italic, and underlined text. These tags are rendered the same way by the browser, but have slightly different meanings. Using the `strong` tag rather than `b` is considered more correct, because the browser understands that it should be considered important (this converys real meaning about the data) rather than merely bold (this is simply typographical). The same is true for the other tags. In general, do not use the `b`, `i`, and `u` tags.

<dl>
    <dt>Tag Names</dt> <dd>strong, em</dd>
    <dt>Tag Description</dt> <dd>Designate strongly important or emphasized text.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>In-line</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<p>
    This text is <strong>very important</strong>, while this is <em>emphasized</em>.
</p>
```

Would produce the following result:

> <p>
>     This text is <strong>very important</strong>, while this is <em>emphasized</em>.
> </p>

### Inserted (Underlined) and Deleted (Strikethrough) Text

The **inserted text tag** is used to denote that certain words or phrases within a paragraph (or any chunk of text) that have been inserted into a document (often to denote recent changes). This tag is often used as a way of displaying underlined text, because that is how most browsers display inserted text by default.

The **deleted text tag** is used to denote that certain words or phrases within a paragraph (or any chunk of text) have been replaced or are otherwise defunct. By default, the browser displays emphasized text with a line through it.

<dl>
    <dt>Tag Names</dt> <dd>ins, del</dd>
    <dt>Tag Description</dt> <dd>Designate inserted or deleted text.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>In-line</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<p>
    Inserted text appears <ins>underlined</ins>; however, deleted text has a <del>line through it</del>.
</p>
```

Would produce the following result:

> <p>
>     Inserted text appears <ins>underlined</ins>; however, deleted text has a <del>line through it</del>.
> </p>

### Subscript and Superscript

The **Subscript Tag** is a typographical tag used to render text which is slightly smaller with a lowered baseline. The **Superscript Tag** is used for text which is slightly smaller with a raised baseline. These are often useful when typing mathematical formulas or similar data, or creating footnote citations.

<dl>
    <dt>Tag Names</dt> <dd>sub, sup</dd>
    <dt>Tag Description</dt> <dd>Designate subscript or superscript text.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>In-line</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<p>
    When converting between decimal and binary, it is helpful to know that 2<sup>10</sup> = 1024.
    The number 26<sub>10</sub> (base 10) is equal to 00011010<sub>2</sub> (base 2).
</p>
```

Would produce the following result:

> <p>
>     When converting between decimal and binary, it is helpful to know that 2<sup>10</sup> = 1024.
>     The number 26<sub>10</sub> (base 10) is equal to 00011010<sub>2</sub> (base 2).
> </p>

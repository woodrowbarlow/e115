---
title: CSS and Styling
---

# Basic Web Pages

 * [Introduction](introduction.html)
 * [Formatting Tags](formatting-tags.html)
 * [Measurement Units](measurement-units.html)
 * [CSS Rules](css-rules.html)
 * [In-Line Styling](in-line-styling.html)
 * [External Stylesheets](external-stylesheets.html)
 * [CSS Selectors](css-selectors.html)
 * [Property Chart](property-chart.html)

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

## Measurement Units on the Web

In order to achieve full control over the visual design of a webpage, the ability to accurate define distances and colors on the screen is essential. Units of measurement on the web are diverse, but the most commonly used units are detailed below.

### Colors

Modern computer screens are capable of displaying 24 bits of color, or 224 different colors. CSS can make use of all of these colors. Rather than coming up with 16,777,216 names for all these colors, we can specify them with hex codes.

Computer screens create color by mixing varying amounts of red, green, and blue light. Combining them in different intensities creates the illusion of different colors. For example, black can be thought of as zero red light, zero green light, and zero blue light; white, on the other hand, is lots of all three colors of light. Any color that the screen can display can be specified as a mixture of just red, green, and blue light. This is called an **additive color system**.

The mixture is represented as three bytes: one byte for red, one for green, and another for blue. Recall that a byte can have a value between 0 and 255. Rather than specifying them as a triple of decimal numbers, each byte can be conveniently represented exactly as two hexadecimal digits. **Hexadecimal**, or hex, is, like decimal and binary, a positional number system; however hex digits are base 16. They are written using 0-9 for the first 10 numerals, and A-F for the remaining 6 numerals. Decimal 10 becomes hexadecimal A, 11 becomes B, etc., up to F. The values 0 through 255 become 00 through FF.

CSS uses hex to specify colors. They begin with a hash followed by six hex digits. The first two hex digits represent the red intensity, the next two represent green, and the last two represent blue: #rrggbb. For example, a bright red color can be thought of as full red intensity with zero intensity green and blue, thus #FF0000. When red and green light are mixed, the result, #FFFF00, is yellow.

For a comprehensive list of hex colors and their names, refer to [Wikipedia](http://en.wikipedia.org/wiki/List_of_colors).

### Distances

Due to the wide variety of web-enabled device displays, all with different physical sizes and pixel densities, distances are a little more difficult to measure on the web.

The most literal way of measuring distances is by using the pixel unit. In css, a **pixel** is a unit of distance based on a mathematical approximation of the smallest dot a computer screen can display. This means that, even on two laptops that have a 15-inch screen, a pixel might appear smaller on one than the other if the first screen had a higher display resolution. Pixels are considered appropriate for resizing (or adjusting other properties of) any elements on a webpage: text, images, etc.

Another commonly used unit of measurement is the percentage unit. The **percentage unit** is based off of the containing element's font size (or the browser's default font size, if no font size is defined for the containing element). This means that if a user has changed their brower's font size, elements which are measured in percentage may scale as well - this can be advantageous, if anticipated properly. Because the percentage unit is so closely coupled with font size, it is not very appropriate for resizing elements other than text (for example, giving an image a width of 200% will *not* cause the image to be twice as wide as it was).

Similar to the percentage unit is the em unit. One **em** approximates the width of the letter 'M' (the widest character in the English alphabet) in the font size of the containing element (or the browser's default font size, if no font size is defined for the containing element), although the actual measurement is slightly larger than that. Like the percentage unit, this can cause scaling if the user has adjust the browser's default font size. This unique, although seemingly obtuse, unit of measurement has a mostly historic relevance in the typesetting industry and is still quite popular in the digital age. Because the percentage unit is so closely coupled with font size, it is not very appropriate for resizing elements other than text.

For more information about measurements of distance on the web, review the [W3C formal definitions](http://www.w3.org/TR/CSS21/syndata.html#length-units), or search for any of the many blog articles written by web developers which discuss the relative merits of each type of unit.

## CSS Rules Syntax

CSS is, essentially, a language for defining and selectively applying a collection of formatting rules to a webpage. In CSS, a **rule** is a property followed by list of values for that property, and rules always follow a simple syntax. A **property** simply specifies which feature is being defined. There are many properties (more than can be covered in this book) which define visual features such as the font, color, size, positioning, shadow effects, 3d translations, etc. of elements on the webpage. The second part of the rule is a list of values, with each value separated by a space. Each **value** might be any type of information (color, size, rotation, etc.) and must be listed in a specific order (the exact values required and their order depends on the property being set).

Properties are separated from the values by a colon (`:`), values are separated from each other by a space (` `), and the rule is finished with a semicolon (`;`). The example below shows a rule which, if applied to an element, would give the element a 2-pixel-wide solid red border.

```css
border: 2px solid #FF0000;
```

The property is "border", and the values are the width, style, and color of the border. To view a list of the most common properties and notes regarding how they are used, view the property chart section of this chapter.

## In-Line Styling

The simplest way of applying CSS rules to an element is to simply inject the rule directly into the element's tag in the XHTML document. This is done by means of an attribute which has not been previously discussed, but which can be applied to any XHTML tag: the style attribute. The value of that attribute is a list of CSS rules, and those CSS rules will be applied to the element in question.

> *Note*: The examples below use rules which contain properties that have not been introduced. To read about these properties and how they can be used, view the Property Chart section at the end of this chapter.

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

> *Note*: Technically, the semicolon on the *last* rule in a list of rules is optional; therefore, it is common to omit the semicolon when using in-line styling to apply only one rule. Whether or not to omit it in this case comes down to personal preference.

### Why Use In-Line Styling?

Although it is the easiest method of styling an element, in-line styling does not help achieve one of the biggest advantages of CSS: the ability to make a change in one file in order to update the style of an entire website. If an entire website were styled using in-line styling, an update would require modifying each and every page. It is introduced here as a simple way of understanding how CSS rules work, but, in practical application, in-line styling is rarely used except to handle edge cases on certain pages which are exceptions to the website's overall style.

## Setting Up an External Stylesheet

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

### Class Selector

TODO

### ID Selector

TODO

## Property Chart

TODO

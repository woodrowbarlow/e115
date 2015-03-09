---
title: In-Line Styling
---

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

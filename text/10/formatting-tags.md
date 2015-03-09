---
title: Formatting Tags
---

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

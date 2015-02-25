---
title: Text
---

## Text

In XHTML, text has no meaning on its own - all meaning must be derived from tags that are applied to the text. When text has meaning, the browser can decide an intelligent way to display that text. The following tags are used to structure text within a webpage.

### The Paragraph Tag

This is the most basic type of text tag. The **paragraph tag** represents a single, self-contained paragraph. The content between the opening and closing tags is displayed in its own block. Paragraphs automatically add space above and below the text, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>p</dd>
    <dt>Tag Description</dt> <dd>Create a paragraph.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<p>
    Hello, world.
</p>
<p>
    This is a paragraph.
</p>
```

Would produce the following result:

> <p>
>     Hello, world.
> </p>
> <p>
>     This is a paragraph.
> </p>

### Heading Tags

**Heading tags** are used to create titles and subtitles for sections of your webpage. Heading tags generate text of varying size which is bold and which represents concepts such as a chapter title, or a blog article title. The content between the opening and closing tags is displayed as bold text. Heading tags automatically add space above and below the text, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Names</dt> <dd>h1, h2, h3, h4, h5, h6</dd>
    <dt>Tag Description</dt> <dd>Create a heading. The h1 heading is the largest, the h6 heading is the smallest.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<h2>Hello, world.</h2>
<p>
    This is a paragraph.
</p>
```

Would produce the following result:

> <h2>Hello, world.</h2>
> <p>
>     This is a paragraph.
> </p>

### The Line Break Tag

Because of the way elements are spaced in XHTML, pressing enter in your text editor is not enough to move text to a new line on the final web page. Instead, we must explicitly insert a **line break tag** to tell the browser to move text to a new line. This tag is a self-closing tag.

<dl>
    <dt>Tag Name</dt> <dd>br</dd>
    <dt>Tag Description</dt> <dd>Insert a line break at the current location.</dd>
    <dt>Tag Type</dt> <dd>Self-Closing</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<p>
    Hello, world. <br />
    This is a paragraph.
</p>
```

Would produce the following result:

> <p>
>     Hello, world. <br />
>     This is a paragraph.
> </p>

### The Horizontal Rule

The **horizontal rule** creates a full-width horizontal gray bar, to be used as a section divider between pieces of content. This tag is self-closing. The horizontal rule automatically adds space above and below, ensuring that nothing else is on the same line. 

<dl>
    <dt>Tag Name</dt> <dd>hr</dd>
    <dt>Tag Description</dt> <dd>Create a horizontal rule, to be used as a content divider.</dd>
    <dt>Tag Type</dt> <dd>Self-Closing</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example**

The following code:

```HTML
<h2>Hello, world.</h2>
<hr />
<p>
    This is a paragraph.
</p>
```

Would produce the following result:

> <h2>Hello, world.</h2>
> <hr />
> <p>
>     This is a paragraph.
> </p>

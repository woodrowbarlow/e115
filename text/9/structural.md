## Structural

Because XHTML gives semantic meaning to data by categorizing it, sometimes applying a tag to something doesn't actually have a visual result on the rendered webpage. One example of this is categorizing chunks of code into categories like "navigation", "main", "footer", etc. Organizing code into these "categories" (sometimes called **containers**) is done by using any of the many **structural tags**. Organizing parts of your page into containers makes styling your page (using the techniques in chapter 10) easier and more flexible, and would make advanced web programming (with languages like JavaScript) easier. Additionally, a more semantically defined webpage is parsed more easily by computers - this will help search engines report accurate descriptions of your page, and will help users of disability software like screen readers to get a more accurate experience when visiting your page.

### The Div Tag

The **div tag** is a generic container tag. It is used to put a part of your page into a container, but the div container doesn't have any inherent semantic meaning to a computer. The div tag is meant to be used when a more applicable structural container tag doesn't exist. The div tag automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>div</dd>
    <dt>Tag Description</dt> <dd>Define a generic container. This has no inherent semantic meaning and no visual result on the webpage.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example: Putting Elements in a Div Container**

The following code:

```HTML
<div>
    <h2>Hello, world.</h2>
    <p>
        This is a paragraph.
    </p>
</div>
```

Would produce the following result:

> <h2>Hello, world.</h2>
> <p>
>     This is a paragraph.
> </p>

### The Span Tag

The **span tag** is a generic container tag to be used in-line. The span container doesn't have any inherent semantic meaning to a computer. The span tag is usually used to select certain words within text, rather than a chunk of code.

<dl>
    <dt>Tag Name</dt> <dd>span</dd>
    <dt>Tag Description</dt> <dd>Define a generic in-line container. This has no inherent semantic meaning and no visual result on the webpage.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example: Putting Content in a Span Container**

The following code:

```HTML
<h2>Hello, world.</h2>
<p>
    This is a <span>paragraph</span>.
</p>
```

Would produce the following result:

> <h2>Hello, world.</h2>
> <p>
>     This is a paragraph.
> </p>

### Other Container Tags

Many more container tags were introduced with version 5 of the XHTML specifications. These new container tags are special, because they have semantic meaning. Although they behave the same as a div tag, all of the tags below have an intended purpose, and using them for that intended purpose means that a computer can understand the way your page is structured. The list below is a partial list only. To learn more, read the [W3C wiki article about structural elements](http://www.w3.org/wiki/HTML_structural_elements), or try browsing the [Mozilla Developer's Network](https://developer.mozilla.org/en-US/).

<dl>
    <dt>Tag Names</dt> <dd>header, nav, footer, section, main, article, aside, figure, figcaption</dd>
    <dt>Tag Description</dt> <dd>Define a semantic container. Each tag has an intended purpose, but all are displayed without special formatting by most browsers.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

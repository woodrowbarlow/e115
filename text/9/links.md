---
title: Links
---

## Links

Websites are rarely composed of a single web page. Usually, there are many inter-connected pages, and users navigate between these pages by clicking on links. On the web, a **link** is something which can be clicked with the mouse in order to re-direct the browser to a new page. Usually, a link is presented as blue, underlined text. Sometimes, a link is a clickable image.

### The Anchor Tag

The **anchor tag** denotes the beginning and end of the clickable content for a link. The content of the anchor tag can be plain text or any inline XHTML element; most commonly, plain text is used, but it is also common to use an image.

The anchor tag has a required attribute, **href** (short for "Hyperlink Reference"), and the value of this attribute is a URL which represents the destination for the browser when the link is clicked. The anchor tag also supports a special option attribute, **target**. If the value of target is `_blank`, the link will be opened in a new browser tab or window.

<dl>
    <dt>Tag Name</dt> <dd>a</dd>
    <dt>Tag Description</dt> <dd>Create a link, the contents of which will be clickable.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>href</dd>
    <dt>Special Attributes</dt> <dd>target</dd>
</dl>

> *Note*: Like the image tag's `src` attribute, the `href` attribute can accept either an absolute or relative URL. If linking to a different website, include the URL protocol (usually either "http://" or "https://", this can be copy-pasted from your browser's address bar) at the beginning to denote that it is an absolute URL

**Example: Plain-text Link**

The following code:

```HTML
<p>
    This is a paragraph. This paragraph contains a <a href="http://ncsu.edu">link</a>.
</p>
```

Would produce the following result:

> <p>
>     This is a paragraph. This paragraph contains a <a href="http://ncsu.edu">link</a>.
> </p>

**Example: Image Link in a New Tab**

The following code:

```HTML
<p>
    Click the image below to open the google homepage in a new tab. <br />
    <a href="http://ncsu.edu" target="_blank">
        <img src="images/ncsu.png" alt="NCSU Homepage" />
    </a>
</p>
```

Would produce the following result:

> <p>
>     Click the image below to open the google homepage in a new tab. <br />
>     <a href="http://ncsu.edu" target="_blank">
>         <img src="images/ncsu.png" alt="NCSU Homepage" />
>     </a>
> </p>

> *Note*: For this example to work, you would need an image file called "google.png" to be inside of a folder called "images", and the folder called "images" would need to be in the same folder that your webpage is stored in.

**Email Links**

In addition to linking to webpages, the anchor tag can link to an email address. To do this, the value of the href attribute is set to the word "mailto", followed by a colon, followed by a recipient's email address. Clicking an email link will cause the user's email client to launch, with the "compose new message" dialogue already filled in.

> *Note*: Using the `target` attribute in conjunction with an email link is meaningless.

**Example: Email Link**

The following code:

```HTML
<p>
    Click <a href="mailto:jschmoe@ncsu.edu">here</a> to email Joe Schmoe.
</p>
```

Would produce the following result:

> <p>
>     Click <a href="mailto:jschmoe@ncsu.edu">here</a> to email Joe Schmoe.
> </p>

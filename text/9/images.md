---
title: Images
---

## Images

Images are used in websites to achieve visual effects which are not possible (or are difficult) with text alone. Website commonly use images for graphics elements such as a logo, or for features such as an online photo album.

### The Image Tag

The **image tag** is used to embed a digital photograph or visual graphic into a webpage. This tag is self-closing. Images, by default, are placed in-line with text.

The image tag has two required attributes. The value of the **src** (short for "source") attribute is a path to the image file which should be displayed; this can be an absolute URL An **Absolute URL** is a direct web address to the image file, beginning with "http://" or "https://" - this is useful when embedding an image that is hosted on another website. A **Relative URL** is a path to the image file relative to the current webpage - this is useful when embedding an image that is hosted on your website.

The value of the **alt** attribute (short for "alternative") is a plain-text string which provides a human-readable description of the image. This text will be displayed by the browser if the image fails to load, or if the user has images disabled. This text is also read aloud by the screen-reading software used by blind persons who navigate the web.

<dl>
    <dt>Tag Name</dt> <dd>img</dd>
    <dt>Tag Description</dt> <dd>Embed an image within the webpage.</dd>
    <dt>Tag Type</dt> <dd>Self-Closing</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>src, alt</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example: Using an Absolute URL**

The following code:

```HTML
<p>
    This is a paragraph. There is an image below this text. <br />
    <img src="http://brand.ncsu.edu/img/2x1-brick.png" alt="NCSU Logo" />
</p>
```

Would produce the following result:

> <p>
>     This is a paragraph. There is an image below this text. <br />
>     <img src="images/ncsu.png" alt="NCSU Logo" />
> </p>

**Example: Using a Relative URL**

The following code:

```HTML
<p>
    This is a paragraph. There is an image below this text. <br />
    <img src="images/ncsu.png" alt="NCSU Logo" />
</p>
```

Would produce the following result:

> <p>
>     This is a paragraph. There is an image below this text. <br />
>     <img src="images/ncsu.png" alt="NCSU Logo" />
> </p>

> *Note*: For this example to work, you would need an image file called "ncsu.png" to be inside of a folder called "images", and the folder called "images" would need to be in the same folder that your webpage is stored in.

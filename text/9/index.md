---
title: Basic Web Pages
---

# Basic Web Pages

 * [Introduction](#introduction)
 * [Account Preparation](#account-preparation)
 * [Tags](#tags)
 * [Bare Minimums](#bare-minimums)
 * [Text](#text)
 * [Images](#images)
 * [Links](#links)
 * [Lists](#lists)
 * [Tables](#tables)
 * [Structural](#structural)

## Introduction

### What is it?

XHTML (or eXtensible Hypertext Markup Language) is a variant of HTML markup language, used to define the document structure of text, images, and other elements for the web. XHTML is a simple way of structuring information in plain-text (using a plain-text editor) via XHTML tags. This structured information can be interpreted in a meaningful way by a web browser, and presented as a webpage.

At its core, XHTML is a way of categorizing types of information. It is not a way of formatting a document, merely a way of defining the components of a document; however, a document full of semantically categorized information can be displayed in an intelligent way by software. For example, web browsers will usually display a piece of text as large and bold if that text is categorized as a heading.

### Practical Applications

XHTML can be used to create a basic static webpage. In conjunction with the lessons in chapter 10, this webpage can be flexibly styled and presented at your creative whim. The ability to easily create your own webpage allows you to share information over the world wide web and maintain a personal piece of virtual real estate. One great application of XHTML skills would be to create a professional web presence where you might present your resume and an autobiography.

### W3C Compliance

The W3C, or World-Wide Web Consortium, is a standards organization tasked with developing standardized practices for web development. This group is responsible for drafting the specifications for XHTML, among other things; in other words, the W3C is the group which decides the “correct” way websites should be created.

The most recent specification for XHTML, according to the W3C governing body, is XHTML5. This version is considered greatly simplified from previous versions – cutting out redundancies and providing flexible options for organizational elements. The W3C provides a tool to ensure that your markup is strictly valid XHTML5 code called the [W3C Validator](http://validator.w3.org/).

### More Information

This textbook only covers the basics of XHTML5. There are many aspects of the language which will not be covered here. To read more about XHTML5 features, or to get clarification for a certain topic, take a look at the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5). If you don’t mind some heavy technical reading, you can also read the official [W3C technical specifications](http://www.w3.org/html/wg/drafts/html/master/).

### Important Programs

XHTML is a markup language written in *plain-text*. This means that XHTML should only be written in a plain-text editor, not in a word processing software. Word processing software inserts information into the text file about the text formatting (for example: font, color, font size, etc.), but does so in a format that is not compatible with XHTML. Plain-text editors, on the other hand, save only the text information with no implied formatting – this allows us to manually define all formatting in XHTML format.

Some plain-text editors are designed for writing markup and other code. These editors display the code with useful color formatting (which help you understand the code syntax) although that formatting is not saved in the file (it only exists to aide the code author). One such recommended (and free) software for Windows users is [Notepad++](http://notepad-plus-plus.org/); an equivalent software for Mac OSX is [TextWrangler](http://www.barebones.com/products/textwrangler/download.html).

### Learning Objects

 * Understand the purpose and application of XHTML code.
 * Understand the concept of valid code and code standards.
 * Be able to read and modify an XHTML document.
 * Create links, tables, and lists within an XHTML document.
 * Be able to create a new XHTML document from scratch.

## Account Preparation

Full-time students at NCSU with active Unity accounts are allocated space on the AFS servers from which to host a small website, if they so desire. In order to take advantage of this offering, you must manually configure your account and storage space first.

Understanding how your account should be set up is important. If you ever wanted to remove permissions so that your site could no longer be viewed by the public, take note below of what permissions are set and remove them.

### Manual Setup

1. Sign into your terminal.
2. Create a new directort directly inside your home directory with the name `www`.
3. Give the AFS user `www:servers` the look permission in your home directory.
4. Give the AFS user `www:servers` the read and look permissions in your newly created `www` directory.
5. Using your text editor and ExpanDrive, create a new file in your newly created `www` directory called `index.html`.
6. In your web browser, navigate to http://www4.ncsu.edu/~unityid/ (making sure to substitute your own unity id) and ensure there is no error message.
 * As you edit the `index.html` file, your changes will be reflected on this webpage.

```bash
mkdir ~/www
fs sa ~/ www:servers l
fs sa ~/www www:servers rl
```

If you want to perform maintenance on your webpage, you may desire to bring it “offline” temporarily. You can do so by temporary removing the permissions for the ‘www’ directory.

```bash
fs sa ~/www www:servers none
```

### Why is there an Error?

It is important to note that if there is not an `index.html` file in your `www` directory, you will see an error. Most likely one of the following errors: **The requested URL /~unityid/index.html was not found on this server.**, or a **403 Forbidden**.

To rectify this error, simply create a blank `index.html` page and save it to your `www` directory.

If you are looking for a file of a different name, simply type the URL http://www4.ncsu.edu/~unityid/name.html into your web browser.

## Tags

Tags are the basis of markup languages like XHTML. **Tags** define elements and sections within the document. A tag can be used to insert an image, a link, a paragraph of text, a navigation bar, or many other things into your web page. Tags can also be used to define semantic categories, which often do not have a direct visual representation on the webpage, but which allows the content to be structured in a meaningful way.

XHTML tags are visually easy to identify. They are always enclosed in “angle brackets” (these are the `<` and `>` characters). In an XHTML document, anything enclosed in angle brackets is to be interpreted as a tag rather than as textual information. These tags will present formatting information in a specific syntax to the browser. XHTML tags come in two variants: paired tags and self-closing tags.

### Paired Tags

**Paired tags** are used to denote content which has a clear beginning and an end. As suggested by the name, these tags are always used in pairs: an opening tag is always eventually followed by a closing tag, with content in between.

An opening tag, in its simplest form, contains the opening angle bracket (`<`), followed by the tag’s name in lowercase letters, followed by the closing angle bracket (`>`). The tag’s name will always be a single word. The closing tag looks the same, but contains a single forward slash (`/`) after the opening angle bracket. The example below shows the usage of a paired tag for creating paragraphs. Notice the content in between the tags – this will become the text of the paragraph.

```HTML
<p>
    Hello, world
</p>
```
    
> *Note*: Don't worry about what these specific tags mean yet; they will be formally introduced in their own sections. Focus instead on the *syntax*.

### Self-Closing Tags

**Self-closing tags**, by contrast, do not have a beginning and an end; they represent a single, self-contained element which cannot have elements inside of it. As a result, self-closing tags do not come in pairs.

A self-closing tag begins with an opening angle bracket (`<`), followed by the tag’s name in lowercase letters, followed by a forward slash (`/`) and a closing angle bracket (`>`). Some choose to also put a space before the slash; this is based on preference. The example below shows the usage of a self-closing tag for inserting line breaks.

```HTML
<br />
```

### Nested Tags

Paired tags can often have other tags inside of them - this is a technique known as **nesting**. Nesting tags inside of each other can be metaphorically represented by Russian nesting dolls. One example of when nesting might be useful is when you want to put a line break in the middle of a paragraph.

To achieve nesting, simply place the inner tag (or pair of tags) after the outer opening tag, but before the outer closing tag. If your inner tag is paired, be sure the inner tag is closed before closing the outer tag.

The example below shows a self-closing tag being nested inside of a paired tag.

```HTML
<p>
    Hello, <br />World
</p>
```

This example shows a paired tag being nested inside of a paired tag.

```HTML
<p>
    Hello, <span>World</span>.
</p>
```

### Tags with Attributes

Certain tags can sometimes have attributes. **Attributes** are used to specify additional information beyond simply what type of tag is being used. For example, when creating a link in a webpage, an attribute must be used in order to specify the destination of the link.

Attributes are provided as attribute-value pairs. That is, each attribute is syntactically formatted as an attribute name (all lowercase and always one word) followed by an equals sign (`=`), followed by a value surrounded by quotation marks (`"`). Attribute-value pairs are listed immediately after the tag name, and are separated from the tag name by a space. In the case of paired tags, attributes are listed only in the opening tag. A tag can have more than one attribute - when this is the case, each attribute-value pair is separated from the others by a space.

The following example shows the syntactical formatting of a paired tag with an attribute. Notice that the value of the attribute is surrounded by quotation marks - this value might be a numeric, text, or other data value, depending on the attribute being used.

```HTML
<a href="http://google.com">Google Homepage</a>
```

> *Note*: Once again, remember that these tags, and their attributes, will be formally introduced in their own right. Focus only on becoming acquainted with the syntax.

The following example shows the syntactical formatting of a self-closing tag with two attributes.

```HTML
<img src="puppies.jpg" alt="Puppies playing." />
```

### XHTML Comments

An XHTML **comment** is similar to a tag, but is not technically an XHTML tag. A comment is used to insert notes into the code which will have no visual impact upon the final result in the web browser whatsoever. This is useful in order to leave reminders to yourself, or to explain parts of your code to other people who may need to modify it. Think of a comment as similar to the annotation features in your word processor – you can view the annotations while you are editing the document, but when you print the document out, the annotations will no longer be visible.

XHTML comments look very different to the traditional type of tags discussed previously. A comment always begins with a certain sequence of characters (`<!--`) and ends with another sequence of characters (`-->`). XHTML comments do not have tag names or attributes within the angle brackets. Instead, they can contain any arbitrary string of text.

The example below shows the usage of a comment. The comment will not be displayed on the final webpage, but will be visible when editing the code.

```HTML
<!-- Note to self: 
     include a short bio in this paragraph. -->
<p>
    Hello, world.
</p>
```

> *Note*: Make sure the message you type in your comment is separated from the special sequences of characters with at least one space on each end.

In addition to adding messages for future coders (or yourself) to look at, comments are useful for temporarily removing parts of your code. Would you like to see what your page looks like without one of your paragraphs, but you aren't ready to remove the code entirely? Just comment it out!

## Bare Minimums

In order to be XHTML5 compliant, there is a basic **skeleton framework** that must be in place. The purpose of this skeleton is to declare which specification version of XHTML we are using, to define some biographical data about the webpage, and to establish the requisite structural categories of the webpage.

The skeleton framework below can be copied directly as a starting template – only be sure to update the content of the title tag to reflect your webpage.

```HTML
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="UTF-8" />
        <title>Your title goes here.</title>
    </head>
    <body>
        <!-- The content of your webpage goes here. -->
    </body>
</html>
```

### DOCTYPE Declaration and HTML Tag

The **document type declaration** (or DOCTYPE), although surrounded by angle brackets, is not technically an XHTML tag; it is a special instruction that warns the web browser that all following text should be interpreted as HTML. The first real tag, **the html tag**, contains an attribute which says which version of HTML we will be using (in this case, XHTML5). Notice that the html tag is not closed until the very last line of the document – this should always be the case.

### Head Section

The **head section** of the webpage is used to define biographical data about the webpage. Nothing in this section is directly visible to the end user; rather, it contains mostly information that a search engine might use to label your website.

Within the head section, the **meta tag** can be used to define various properties for your webpage: author, publishing date, etc. In this case, it is being used to define which characters are permitted to be used on your website. For example, some character sets include only basic Latin letters, while others include Japanese Kanji or Arabic characters. The UTF-8 character set is a good middle ground and is recommended for use on the web.

Another inhabitant of the head section is the **title tag**, which specifies a title for your website. Search engines will use this title to categorize your website, and the browser will use this title to label the browser tab.

### Body Section

Anything that will be visible on the final webpage should be somewhere inside of the **body section**. This includes (but is not limited to) text, images, links, videos, etc. Elements which have a direct visual representation on the webpage should never go in the head section.

### Good Coding Style

XHTML code is easiest to read, write, and edit when it is neatly spaced out and nested. There is no right or wrong way to space out your code, but there are a few generally agreed upon guidelines which will help make your code more readable.

 * Avoid putting multiple tags on one line.
 * If a tag has a significant amount of content, put the opening and closing tags on their own lines, separate from the content.
 * If something (either a content or another tag) is nested inside of a tag, and it is on its own line, use a tab or spaces to indent the inner content.

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
    <img src="http://brand.ncsu.edu/img/2x1-brick.png" />
</p>
```

Would produce the following result:

> <p>
>     This is a paragraph. There is an image below this text. <br />
>     <img src="images/ncsu.png" />
> </p>

**Example: Using a Relative URL**

The following code:

```HTML
<p>
    This is a paragraph. There is an image below this text. <br />
    <img src="images/ncsu.png" />
</p>
```

Would produce the following result:

> <p>
>     This is a paragraph. There is an image below this text. <br />
>     <img src="images/ncsu.png" />
> </p>

> *Note*: For this example to work, you would need an image file called "ncsu.png" to be inside of a folder called "images", and the folder called "images" would need to be in the same folder that your webpage is stored in.

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

## Lists

Lists are one of the options for organizing short pieces of information. Depending on the type of list used, a list might be presented as a series of bullet points or as a series of numbered items. Lists can be layered, and types of lists can be combined. In XHTML, there are three tags used in combination to create lists.

### The Unordered List Tag

An **unordered list** is a list presented as a series of bullet points; that is, each list item in an unordered list is automatically preceded by a solid black dot. The unordered list tag must be used in conjunction with the list item tag, explained below. The unordered list automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>ul</dd>
    <dt>Tag Description</dt> <dd>Create an unordered (bulleted) list.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

### The Ordered List Tag

An **ordered list** is a list presented as a series of numbered points; that is, each list item in an ordered list is automatically preceded by a number (the first item is preceeded by the number one, and the assigned number is incremented for each list item). The ordered list tag must be used in conjunction with the list item tag, explained below. The ordered list automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>ol</dd>
    <dt>Tag Description</dt> <dd>Create an ordered (numbered) list.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

### The List Item Tag

A **list item** is merely an entry in a list. The list item tag is only used within an unordered list or within an ordered list. Each list item is preceeded either by a bullet point or by a number, depending upon whether it is within an unordered or ordered list (respectively). The content of a list item can be any combination of plain text and inline elements.

<dl>
    <dt>Tag Name</dt> <dd>li</dd>
    <dt>Tag Description</dt> <dd>Denote a list item within an unordered or ordered list.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example: Unordered List**

The following code:

```HTML
<ul>
    <li>Milk</li>
    <li>Eggs</li>
    <li>Bread</li>
</ul>
```

Would produce the following result:

> <ol>
>     <li>
>         Homework
>         <ul>
>             <li>Physics Lab</li>
>             <li>Calculus Webassign</li>
>         </ul>
>     </li>
>     <li>Laundry</li>
>     <li>
>         Grocery Shopping
>         <ul>
>             <li>Milk</li>
>             <li>Eggs</li>
>        </ul>
>     </li>
> </ol>

**Example: Layered (Nested) Lists**

The following code:

```HTML
<ol>
    <li>
        Homework
        <ul>
            <li>Physics Lab</li>
            <li>Calculus Webassign</li>
        </ul>
    </li>
    <li>Laundry</li>
    <li>
        Grocery Shopping
        <ul>
            <li>Milk</li>
            <li>Eggs</li>
        </ul>
    </li>
</ol>
```

Would produce the following result:

> 1. Homework
>  * Physics Lab
>  * Calculus Webassign
> 2. Laundry
> 3. Grocery Shopping
>  * Milk
>  * Eggs

## Tables

A table is another option for organizing short pieces of information. It is especially useful for information that has a type and value (or values). A table has rows, and can have any number of cells within each row; traditionally, to create a "grid-style" table, each row has the same number of cells as each other row. Each cell can be a data cell or a header cell (header cells are typically displayed with bold text). In XHTML, there are four tags used in combination to create tables.

### The Table Tag

The **table tag** defines a container which can have rows and cells, forming a table of data. The table tag automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>table</dd>
    <dt>Tag Description</dt> <dd>Define a container for a data table.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

### The Table Row Tag

The **table row tag** creates a row which can be filled with cells. The table row tag can only be used within a table tag. The table row tag automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>tr</dd>
    <dt>Tag Description</dt> <dd>Define a row within a table which can be filled with cells.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Block</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

### The Data Cell Tag

The **table data cell tag** creates a cell within a table row which is intended to be displayed as unformatted data. The data cell tag can only be used within a table row. The data cell tag automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>td</dd>
    <dt>Tag Description</dt> <dd>Define a cell within a table row filled with unformatted data.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

### The Header Cell Tag

The **table header cell tag** creates a cell within a table row which is intended to be displayed as a title. Header cells are usually displayed with bold and centered text. The header cell tag can only be used within a table row. The header cell tag automatically adds space above and below, ensuring that nothing else is on the same line.

<dl>
    <dt>Tag Name</dt> <dd>th</dd>
    <dt>Tag Description</dt> <dd>Define a cell within a table row filled with titular data.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

**Example: Table with Header Row**

The following code:

```HTML
<table>
    <tr>
        <th>Sample No.</th>
        <th>Distance (m)</th>
        <th>Weight (kg)</th>
        <th>Color</th>
    </tr>
    <tr>
        <td>1</td>
        <td>4.6</td>
        <td>65</td>
        <td>Red</td>
    </tr>
    <tr>
        <td>2</td>
        <td>12</td>
        <td>36</td>
        <td>Red</td>
    </tr>
    <tr>
        <td>3</td>
        <td>32.4</td>
        <td>89</td>
        <td>Blue</td>
    </tr>
</table>
```

Would produce the following result:

> <table>
>     <tr>
>         <th>Sample No.</th>
>         <th>Distance (m)</th>
>         <th>Weight (kg)</th>
>         <th>Color</th>
>     </tr>
>     <tr>
>         <td>1</td>
>         <td>4.6</td>
>         <td>65</td>
>         <td>Red</td>
>     </tr>
>     <tr>
>         <td>2</td>
>         <td>12</td>
>         <td>36</td>
>         <td>Red</td>
>     </tr>
>     <tr>
>         <td>3</td>
>         <td>32.4</td>
>         <td>89</td>
>         <td>Blue</td>
>     </tr>
> </table>

## Structural

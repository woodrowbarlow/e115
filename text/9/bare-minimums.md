---
title: Bare Minimums
---

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

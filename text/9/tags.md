---
title: Tags
---

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

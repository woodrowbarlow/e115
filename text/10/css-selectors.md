---
title: CSS Selectors
---

## CSS Selectors

### Type Selector

There are a few different types of selectors. The simplest selector is the type selector. The **type selector** will select all XHTML tags on a page which are of a certain type. For example, this selector is appropriate for selecting all images on the page. To use the type selector, simply type the tag's name in front of the CSS block.

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

### ID Selector

Any XHTML element can be given the ID attribute, the value of which can be any arbitrary string without spaces. In effect, this gives a "name" to an element, so that you can refer to it by name again later. For example, if you have an image at the top of your page, you might give it the ID "logo". No two elements on a webpage can have the same ID.

The CSS **ID Selector** is used to select an item based on its assigned ID. This selector is appropriate for selecting one specific element on the page. To use the ID selector, simply type a hash sign (`#`) followed by the tag's ID in front of the CSS block.

> *Note*: For more information on the ID selector, view the official [W3C Documentation](http://www.w3.org/TR/CSS21/selector.html#id-selectors).

**Example: Adding a Background Color to a Table**

If your XHTML contains the following code:

```html
<table id="mydata">
  <tr>
    <td>Chrysler</td>
    <td>Oddysey</td>
  </tr>
  <tr>
    <td>Dodge</td>
    <td>Ram</td>
  </tr>
</table>
```

And is linked to a CSS file containing the following code:

```css
#mydata {
  background-color: #00FF00;
}
```

Then the webpage will appear like this:

> <table style="background-color: #00FF00;">
>   <tr>
>     <td>Chrysler</td>
>     <td>Oddysey</td>
>   </tr>
>   <tr>
>     <td>Dodge</td>
>     <td>Ram</td>
>   </tr>
> </table>

### Class Selector

Like the ID attribute discussed above, there is another attribute which can be used on any XHTML element called the class attribute. This attribute is similar to the ID attirbute, but instead of assigning a "name" for a single element, it is used to assign an element to a "family" of similar elements. Unlike the ID attribute, a value for the class attribute can be re-used as many times as desired on a given page.

The CSS **Class Selector** is used to select items based on their assigned class. This selector is appropriate for selecting a hand-picked collection of elements. To use the class selector, simply type a period (`.`) followed by the tag's class in front of the CSS block.

> *Note*: For more information on the class selector, view the official [W3C Documentation](http://www.w3.org/TR/CSS21/selector.html#class-html).

**Example: Making Certain Elements Bold**

If your XHTML contains the following code:

```html
<p>
  This is a <span class="boldtext">paragraph</span>, and it contains a <a href="http://ncsu.edu" class="boldtext">link</a>.
</p>
```

And is linked to a CSS file containing the following code:

```css
.boldtext {
  font-weight: bold;
}
```

Then the webpage will appear like this:

> <p>
>   This is a <span style="font-weight:bold">paragraph</span>, and it contains a <a href="http://ncsu.edu"  style="font-weight:bold">link</a>.
> </p>

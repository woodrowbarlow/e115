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
    <li>Homework</li>
    <ul>
        <li>Physics Lab</li>
        <li>Calculus Webassign</li>
    </ul>
    <li>Laundry</li>
    <li>Grocery Shopping</li>
    <ul>
        <li>Milk</li>
        <li>Eggs</li>
    </ul>
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

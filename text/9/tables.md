---
title: Tables
---

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

The **table data cell tag** creates a cell within a table row which is intended to be displayed as unformatted data. The data cell tag can only be used within a table row.

<dl>
    <dt>Tag Name</dt> <dd>td</dd>
    <dt>Tag Description</dt> <dd>Define a cell within a table row filled with unformatted data.</dd>
    <dt>Tag Type</dt> <dd>Paired</dd>
    <dt>Display Type</dt> <dd>Inline</dd>
    <dt>Required Attributes</dt> <dd>None</dd>
    <dt>Special Attributes</dt> <dd>None</dd>
</dl>

### The Header Cell Tag

The **table header cell tag** creates a cell within a table row which is intended to be displayed as a title. Header cells are usually displayed with bold and centered text. The header cell tag can only be used within a table row.

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

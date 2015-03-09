---
title: CSS Rules
---

## CSS Rules Syntax

CSS is, essentially, a language for defining and selectively applying a collection of formatting rules to a webpage. In CSS, a **rule** is a property followed by list of values for that property, and rules always follow a simple syntax. A **property** simply specifies which feature is being defined. There are many properties (more than can be covered in this book) which define visual features such as the font, color, size, positioning, shadow effects, 3d translations, etc. of elements on the webpage. The second part of the rule is a list of values, with each value separated by a space. Each **value** might be any type of information (color, size, rotation, etc.) and must be listed in a specific order (the exact values required and their order depends on the property being set).

Properties are separated from the values by a colon (`:`), values are separated from each other by a space (` `), and the rule is finished with a semicolon (`;`). The example below shows a rule which, if applied to an element, would give the element a 2-pixel-wide solid red border.

```css
border: 2px solid #FF0000;
```

The property is "border", and the values are the width, style, and color of the border. To view a list of the most common properties and notes regarding how they are used, view the property chart section of this chapter.

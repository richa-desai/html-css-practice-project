# Box Model
* When laying out a document, the browser's rendering engine represents each element as a rectangular box.
* CSS determines all properties of these boxes.
* Properties of box Model:
    1. content: Used to displays the text, images, etc, that can be sized using the width & height property.
    1. padding: Used to create space around the element, inside any defined border.
    1. border: Used to cover the content & any padding, & also allows to set the style, color, and width of the border.
    1. margin: Used to create space around the element i.e., around the border area.
* The following figure illustrates the Box model in CSS:

    ![Box Model](./resources/images/box_model.png)

* Below code will set the dimentions shown in the image:
```css
p {
 width: 794px;
 height: 160px;
 padding: 50px 20px;
 border: 5px;
 margin: 50px 30px;
}
```
* The total width for the element can be calculated as:
```
Total element width = width + left padding + right padding + left border + right border + left margin + right margin
```
* Therefore, the total width of the p element is:
```
Total width = 794 + 20 + 20 + 5 + 5 + 30 + 30 = 904 px
```

* The total height for the element can be calculated as:
```
Total element height = height + top padding + bottom padding + top border + bottom border + top margin + bottom margin
```
* Therefore, the total height of the p element is:
```
Total height = 160 + 50 + 50 + 5 + 5 + 50 + 50 = 370 px
```
* If the box-sizing property is set to border-box on an element, padding and border are included in the width and height. The code below ensures that all elements are sized in this more intuitive way.
```css
* {
  box-sizing: border-box;
}
```
# Inline versus Block Elements.
* Block elements: They consume the entire width available irrespective of their sufficiency. They always start in a new line and have top and bottom margins. It does not contain any other elements next to it.
* Examples of Block elements:

    1. `<h1>`-`<h6>`
    1. `<div>`
    1. `<hr>`
    1. `<li>`
    1. `<ul>`
    1. `<p>`
    1. `<table>`
* Inline elements: Inline elements occupy only enough width that is sufficient to it and allows other elements next to it which are inline. Inline elements don’t start from a new line and don’t have top and bottom margins as block elements have.
* Examples of Inline elements:
    1. `<a>`
    1. `<br>`
    1. `<script>`
    1. `<input>`
    1. `<img>`
    1. `<span>`
    1. `<b>`
    1. `<label>`

# Positioning: Relative/Absolute
Relative Position: Property will cause element to adjust from its normal position. The other objects or elements will not fill the gap.

Syntax:
```css
position: relative;
```

Absolute Position: Property will cause element to adjust its position with respect to its parent. If no parent is present, then it uses the document body as parent.

```css
position: absolute;
```

# Common CSS structural classes / Common CSS styling classes
Structural pseudo classes allow access to the child elements present within the hierarchy of parent elements. E.g. select first-child element, last-child element, alternate elements present within the hierarchy of parent elements.

Selector|Example|Example description
---|---|---
.class1 .class2|.name1 .name2|Selects all elements with name2 that is a descendant of an element with name1
element element|div p|Selects all `<p>` elements inside `<div>` elements
element>element|div > p|Selects all `<p>` elements where the parent is a `<div>` element
:active|a:active|Selects the active link
:first-child|p:first-child|Selects every `<p>` element that is the first child of its parent
:first-of-type|p:first-of-type|Selects every `<p>` element that is the first `<p>` element of its parent
:focus|input:focus|Selects the input element which has focus
:hover|a:hover|Selects links on mouse over
:last-child|p:last-child|Selects every `<p>` element that is the last child of its parent
:last-of-type|p:last-of-type|Selects every `<p>` element that is the last `<p>` element of its parent
:link|a:link|Selects all unvisited links
:nth-child(n)|p:nth-child(2)|Selects every `<p>` element that is the second child of its parent
:nth-last-child(n)|p:nth-last-child(2)|Selects every `<p>` element that is the second child of its parent, counting from the last child
:nth-last-of-type(n)|p:nth-last-of-type(2)|Selects every `<p>` element that is the second `<p>` element of its parent, counting from the last child
:nth-of-type(n)|p:nth-of-type(2)|Selects every `<p>` element that is the second `<p>` element of its parent
:only-of-type|p:only-of-type|Selects every `<p>` element that is the only `<p>` element of its parent
:only-child|p:only-child|Selects every `<p>` element that is the only child of its parent
:visited|a:visited|Selects all visited links


# CSS Specificity
* Decides which specific set will be applied to the element, when more than one set of CSS rules apply to the same element
* Specificity Rules include:  

    1. External stylesheet has lowest precedence.
    1. Internal CSS is overridden by inline CSS.
    1. Inline CSS overrides all other selectors.

* Specificity Hierarchy: Every element selector has a position in the Hierarchy. 

    1. Inline style: Inline style has highest priority.
    1. Identifiers(ID): ID have the second highest priority.
    1. Classes, pseudo-classes and attributes: Classes, pseudo-classes and attributes comes next. 
    1. Elements and pseudo-elements: Elements and pseudo-elements have lowest priority. 

# References
1. [Mozilla Web Docs Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
1. [Geeks For Geeks](https://www.geeksforgeeks.org)
1. [CSS Selectors - W3Schools](https://www.w3schools.com/cssref/css_selectors.php)
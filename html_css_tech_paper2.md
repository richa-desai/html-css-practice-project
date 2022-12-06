# CSS Responsive Queries
* All screen sizes can be handled
* Uses `@media` rule
* Example - If the browser window is 600px or smaller, the background color will be lightblue:
```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```
* **Always Design for Mobile First**
* Advantage of Mobile First: Page displays faster on smaller devices.
* Typical Device Breakpoints
    1.  Extra small devices (phones, 600px and down)
    1. Small devices (portrait tablets and large phones, 600px and up)
    1. Medium devices (landscape tablets, 768px and up)
    1. Large devices (laptops/desktops, 992px and up)
    1. Extra large devices (large laptops and desktops, 1200px and up)

# Flexbox/Grid
* The **Flexible Box** Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.
* Syntax -
    ```css
    .class {
        display:flex;
    }
    ```
* Flexbox Elements
    1. Flex Container
    1. Flex Items
* All direct children of the flex container automatically become flex items.
* CSS Flex Responsive: Easily handles contents in different screen sizes.
* The **CSS grid** layout module is used to create a grid-based layout system, with the help of rows and columns
* Syntax -
    ```css
    .class {
        display:grid;
    }
    ```
* A grid layout consists of a parent element, with one or more child elements.
* All direct children of the grid container automatically become grid items.

# Common header meta tags
* Define keywords for search engines:
```html
<meta name="keywords" content="HTML, CSS, JavaScript">
```

* Define a description of your web page:
```html
<meta name="description" content="Free Web tutorials for HTML and CSS">
```

* Define the author of a page:
```html
<meta name="author" content="John Doe">
```

* Refresh document every 30 seconds:
```html
<meta http-equiv="refresh" content="30">
```

* Setting the viewport to make your website look good on all devices:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```


# Best practices in HTML and CSS
1. Syntax
    * Don't forget optional closing tags.
    * Don't capitalize tags.
    * Use soft tabs with two spaces—they're the only way to guarantee code renders the same in any environment.
    * Always use double quotes, never single quotes, on attributes.
1. doctype
    * Ensures that the browser makes a best-effort attempt at following the relevant specifications
1. Attribute Order 
    1. class
    1. id, name
    1. data-*
    1. src, for, type, href, value
    1. title, alt
    1. role, aria-*
1. Reducing MarkUp (Example)
    ```html
    <!-- Not so great -->
    <span class="avatar">
    <img src="...">
    </span>

    <!-- Better -->
    <img class="avatar" src="...">
    ```
1. Alt-text (For images)
1. CSS Syntax
    * When grouping selectors, keep individual selector to a single line.
    * Include one space before the opening brace.
    * End all declarations with a semi-colon.
    * Lowercase all hex values, e.g., #fff.
1. Media Query Placement
    * Always try to place your media query selector close to the relevant sets.



# References
1. [HTML and CSS Good Practices](https://dev.to/codewithtee/15-html-and-css-good-practices-4608)
1. [Geeks For Geeks - Grid and Flex](https://www.geeksforgeeks.org)
1. [CSS Media Queries - W3Schools](https://www.w3schools.com/css/css3_mediaqueries_ex.asp)
1. [Meta Tags](https://www.ionos.com/digitalguide/websites/web-development/the-most-important-meta-tags-and-their-functions/)
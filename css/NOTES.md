# Learn CSS

CSS, or _Cascading Style Sheets_ is the language used to style HTML content on a web page.

## Setup and Selectors

### Inline Styles

You can use the `style` attribute to place CSS directly into an HTML file. The attribute is placed in the opening tag and follows the traditional CSS format. Multiple styles can be added under one `style` tag.

HTML also allows you to write CSS code in a dedicated section called the `<style>` tag. It must be placed inside the `<head>` element.

### Linking the CSS File

To link a CSS file to an HTML file, a `<link/>` must be placed in the head of the HTML file. It requires three attributes:

1. `href` : the path to the CSS file
2. `type` : the type of document being linked to (_text/css_)
3. `rel` : the relationship between the HTML and CSS files (_stylesheet_)

### Tag Names

A CSS _selector_ changes the style of any HTML element that matches its name. For example, the selector `p { color: red; }` will change the font color of every paragraph in an HTML file to red.

### Class Names

If you want to target a more specific group of elements, you can tag an element with a `class` attribute. To select an element by its tag in CSS, you must prepend the class name with a period. To make an element red with the class attribute,

HTML:
`<p class="brand">Hello.</p>`

CSS:
`.class { color: red; }`

It is possible for an element to have more than one class attributed to it. They added to the attribute and separated by a space.

### ID Names

If an HTML element needs to be styled uniquely, we can use the `id` attribute. This is denoted in CSS by prepending a _#_ to the id name.

### Classes and IDs

Classes and IDs are used for different purposes. Classes are meant to be reused for many elements, while IDs should style only one element. This is because IDs override tag and class styles. You should avoid overuse of ID tags.

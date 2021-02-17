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

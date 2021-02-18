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

CSS best practice styles elements using the lowest degree of specificity, so that styles are easy to override when necessary. If possible, use a tag selector. If not, use a class selector. If even that is not enough, use an ID selector.

### Chaining Selectors

It is possible to have elements with multiple selectors. If you wanted to style selective h1 elements a certain way, you can chain a class selector to a tag selector:

`h1.special {}`

This _only_ affects `<h1>` elements that carry the `class` value _"special"_. It would not affect any other element type to carry that class.

### Nested Elements

If HTML elements are nested within other elements (e.g. list items), you can style them by assigning a class to the outer element, then specify the element you want to style.

`.main-list li {}` targets the list items inside an ordered/unordered list whose class is `main-list`.

### More on Chaining

The selector `.main p{}` would not affect _all_ paragraph elements; only those paragraphs inside the `.main` element would be affected. It overrides any more general paragraph rule that exists.

### Multiple Selectors

If multiple selectors have repetitive style attributes, you can avoid that repetition by separating the selectors by a comma to style both.

## CSS Visual Rules

**font-family** : When deciding typeface, keep in mind:

1. A specified font in a stylesheet must be installed on a user's computer to display on the webpage.
2. Default typeface is _Times New Roman_.
3. Having too many typefaces slows down page loading.
4. If a typeface consists of more than one word, enclose it in quotes.

**font-size** : The font size is measured in _px_, or pixels.

**font-weight** : This controls how thin or bold text looks. Values include _bold_ and _normal_.

**text-align** : This property will align to its parent. It can align to the _left_ hand side, _right_ hand side, or _center_ of its parent.

**color** : Color can affect the foreground and the background.

- _color_ : the color an element appears in
- _background-color_ : the color that appears in the background

**opacity** : Measured from 0 to 1, 1 is fully visible and 0 is fully invisible.

**background-image** : We can change the background of an element into an image. The value provided must be a url, which is written as `url("example.jpg")`.

**!important** : Applied to specific attributes, this will override _any_ style regardless of its specificity. A justification for its use is when working with multiple stylesheets.

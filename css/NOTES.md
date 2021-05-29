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

## The Box Model

The box model allows the browser to interpret elements on a webpage as though they existed within a box.

The box model's properties are:

- width/height : width/height of content area, measured by pixels
- padding : space between the content area and border
- border : thickness and style of the border
- margin : amount of space between border and outside edge of the element

### Borders

Borders can be set with a width, style, and color.

- **width** : A border's thickness. Can be set in pixels or with _thin_, _medium_, or _thick_.
- **style** : Border design. Check [MDN Web Docs](#https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#values) for different styles.
- **color** : Color of the border.

The default border is:

`border: medium none color;`

If one or more of these values are not set, as in the example below, the browser assigns the default value.

`border: solid red;`

### Border Radius

You can change the corners of a border with `border-radius`. This can be set either with pixels or percentages.

### Padding

Padding expands background color beyond the content area. The `padding` element allows you to set padding for each side of the box by a specfied number of pixels. You can also be more specific by using `padding-top`, `padding-right`, `padding-bottom`, and `padding-left`.

Setting padding for each side one by one is too much work. Instead, we can specify them in a single declaration. Starting from the top, we can declare padding in a clockwise rotation, like so:

`padding: 6px 10px 12px 5px;`

If top and bottom equal each other, and left and right equal each other, we can use this shortcut:

`padding: 5px 6px;`

### Margins

Margin specifies the size of the space directly outside the box. This is written using the same rules as padding.

Margin is unique from padding in that it allows you to center content using the value _auto_. In order to center an element, you must also set the element's **width**.

### Margin Collapse

Vertical margins collapse (padding does not), while horizontal margins and padding are always added together.

### Minimum and Maximum Height and Width

To avoid issues with screen size changes, CSS can limit the range of widths and heights the element's box can be sized to.

This is done with **min-width**, **max-width**, **min-height**, and **max-height**.

### Overflow

Overflow controls what happens when content overflows from the box. It can be set to:

- _hidden_ : overflow content is hidden
- _scroll_ : a scrollbar is added to scroll content
- _visible_ : overflow is displayed outside the box

### Resetting Defaults

In the absence of an external stylesheet, browsers have default values for margin and padding. This can sometimes cause problems for developers, so resetting these defaults ensures you are working with a clean slate.

`* { margin: 0; padding: 0; }`

### Visibility

Elements can be hidden from view with **visibility**. This has two values: _hidden_ and _visible_.

The difference between **visibility**: _hidden_ and **display**: _none_ is that **display** removes the element from the web page completely, while **visibility** will still have space reserved for it, and can still be viewed by users looking at the source code in their browser.

### Changing the Box Model

Under the default box model, padding and border thickness affect the overall dimensions of the box, making it difficult to accurately size.

We can use the **box-sizing** property to change the type of box model the browser should use. Its default value is _content-box_, but we can change it to _border-box_, which includes border thickness and padding in the overall dimensions. This way, we only need to specify the overall height and width of the content box, and the border thickness and padding will be subtracted from those dimensions instead of added to it.

If you want to implement the new box model for all elements in the browser, use the universal selector (`*`).

## Display and Positioning

### Position

The **position** of an element can be set to four values: _static_ (default), _relative_, _absolute_, and _fixed_.

_relative_ - position relative to its static position. Positioned using offset properties

- top - moves element down
- bottom - moves element up
- left - moves element right
- right - moves element left

_absolute_ - position for element will be ignored by all other elements on page

_fixed_ - element will remain in a specific position on page regardless of scrolling

### Z-Index

The **z-index** refers to the depth of elements. The greater the index, the more shallow the element.

### Inline Display

**Display** property has three values: _inline_, _block_, and _inline-block_.

Inline elements take up only the space necessary to fulfill their purpose. These include elements like `<em>`, `<strong>`, and `<a>`, which are often found inline with another element.

In CSS, we can apply this value to any element to make it appear inline with another element.

### Block Display

These elements include all levels of heading elements and differ from inline elements in that they are not displayed on the same line as content around them.

### Inline-Block Display

This value combines the features of the previous two.

### Float

The **float** property is used to move an element as far to the _left_ or _right_ of a container as possible.

### Clear

**Clear** specifies how elements should behave when they run up against each other on a page.

- _left_: the left side of the element will not touch any element within the same container
- _right_: the right side will not touch any element in the same container
- _both_: neither side will
- _none_: the element can touch either side

## Color

Colors are portrayed in four formats: named colors, hexadecimal, rgb, and hsl.

### Foreground vs Background

Foreground color affects the color of the element. Background color affects the space behind the element.

### Hexadecimal

Color can be portrayed as hexadecimals: 6 digits fronted by a #. If pairs of the hexadecimal are the same it can be shortened to 3 digits.

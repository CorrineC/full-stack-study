# HTML

HTML (declarative) is a language used to describe content and structure of documents.

## Elements and Structure

### Notes

- Add `<!DOCTYPE html>` to the beginning of every html doc to make sure the browser interprets your code correctly. You still have to include `<html></html>`.
- Images can be links.
- Whitespace is your friend.

### Common Tags

- Tags don't need closers if they don't enclose content

#### Section Tags

`<body></body>` - information displayed directly on page

`<div></div>` - div (container that divides page into sections; useful for applying CSS styles to a group of elements)

`<head></head>` - contains page metadata

`<a> href=""</a>` - anchor (link); can link to target ids w/ `#`

`<br/>` - break

`<em></em>` - italics

`<h1> to <h6>` - headers

`<img src="link.jpg"/>` - image

`<li></li>` - list item

`<ol></ol>` - ordered list

`<p>Stuff</p>` - paragraph

`<span></span>` - separates small pieces of text

`<strong></strong>` - bold

`<title></title>` - webpage name

`<ul></ul>` - unordered list

`<video src="" width="" height="" controls>Video not supported</video>` - video

### Attributes

`alt` - alternative text; caption for images

`controls` - loads basic video controls

`height` - height (will auto adjust with width)

`href` - hyperlink reference (used for anchor tags)

`id` - section identifier

`src` - image source URL

`target` - (anchor attribute) specifies how link should be opened; value `"_blank"` means open in new tab

`width` - width

## Tables

Tables can be split into a head (`<thead>`), body (`<tbody>`), and footer (`<tfoot>`).

`<table>` - creates table

`<td colspan="3">` - table data

`<th>` - table heading

`<tr>` - table row

### Table Attributes

`colspan` - data can span columns

`rowspan` - data can span rows

## Forms

The `<form>` element is useful for HTTP requests.

`<form action="/example.html" method="POST"></form>`

The `action` attribute is where the info is sent.

The `method` attribute determines what transformation will be used on the info (HTTP verbs like POST are not case-sensitive; POST is capitalized out of convention).

The `<input/>` element has a `type` attribute which determines how the element shows up and interacts on a web page.

Setting `type` to:

- "text" : creates field for text input
- "password" : creates field that censors text input
- "number" : creates field for number input
- "range" : creates slider to select from range of numbers
- "checkbox" : creates checkbox
- "radio" : creates radio button
- "list" : pairs inputs a datalists of the same id
- "submit" : creates submit button

Additionally, if we want to submit the form, we need to include the `name` attribute as well. The `value` prefills the input field.

The `<label>` element specifies which input id to target.

// Do these attributes have a conventional order? //

The `<select>` element uses `<option>` to render dropdown lists.

The `<datalist>` element uses `<option>` and works with `<input/>` to search choices.

A `<textarea>` is a customizable text field.

`<textarea rows="3" cols="40">Sample text here.</textarea>`

When a form is submitted the fields that accept input are sent as name=value pairs.

### Form Validations

Client-side validation checks input data on the browser and verifies it before sending it to the server. It saves time, protects the server from malicious code or data, and allows for quick feedback to users.

Input fields in a form that are not optional can be enforced with the `required` attribute.

`<input id="allergies" name="allergies" type="text" required/>`

We can also require min and max values for number and range fields, and minlength and maxlength values for the number of characters in a text field.

The `pattern` attribute can be assign a regular expression (regex). Inputs must match the regex to be submitted.

For example, a valid credit card would match the pattern "[0-9]{14,16}". Valid cards contain only numbers and 14-16 digits in total.

## Semantic HTML

Semantic HTML is useful for accessibility, search engine optimization, and understandability. Screen readers and browsers are better able to interpret code, search engines are more likely to identify your website's content, and developers find semantic HTML easier to read?

A `<header>` container usually contains navigational links and introductory content. `<nav>` contains a block of navigation links. It can be used in a header or on its own. The `<main>` element encapsulates the main content on a webpage, including `<section>`s (elements in a document with the same theme) `<article>`s (element that holds content which makes sense on its own); `<footer>` contains contact info, copyright info, terms of use, site maps, and reference to top page links. The `<aside>` element can be used for additional information such as bibliographies, endnotes, comments, pull quotes, and sidebars.

The elements `<figure>` and `<figcaption>` are like an aside with images.

The `<audio>` tag also exists. A `<source/>` element is place inside it.

// Why? //

`<video>` : uses attributes like `controls`, `autoplay`, `loop`. `<embed/>` exists, but it's deprecated.

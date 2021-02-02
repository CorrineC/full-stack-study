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

The `<input/>` element has a `type` attribute which determines how the element shows up and interacts on a web page. Additionally, if we want to submit the form, we need to include the `name` attribute as well. The `value` prefills the input field.

The `<label>` element specifies which input id to target.

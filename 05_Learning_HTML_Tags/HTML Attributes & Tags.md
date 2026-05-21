# HTML Attributes & Tags Guide

## HTML Attributes

### What are HTML Attributes

* Provide additional information about elements
* Placed within opening tags
* Common examples: `href`, `src`, `alt`
* Use `name="value"` format
* Can be single or multiple per element

### ID Property

* **Unique Identifier**: Each ID must be unique within a page
* **Anchoring**: Enables direct linking using `#id` in URLs
* **CSS & JavaScript**: Used for selecting elements for styling or scripting

---

## HTML Tags

### Heading Tag

* Defines headings in a document
* Range: `<h1>` to `<h6>`
* `<h1>` is most important, `<h6>` is least
* Important for SEO
* Helps structure content

### Paragraph Tag

* Defines paragraphs
* Enclosed within `<p>` and `</p>`
* Adds automatic spacing before and after
* Text wraps automatically
* Common in text-heavy content

### Line Break Tag (`<br>`)

* Adds a line break within text
* Empty tag (no closing required)
* `<br>` and `<br/>` both valid

### Horizontal Rule Tag (`<hr>`)

* Creates a horizontal line
* Empty tag
* Acts as a divider

---

### Image Tag

* Used to embed images
* Uses `src` for image URL
* `alt` provides alternative text
* Can be resized using `width` and `height`
* Self-closing (no end tag required)
* Supports `loading="lazy"` for performance

---

### Video Tag

* Embeds video files
* Uses `src` attribute for video URL
* Supports formats like MP4, WebM

#### Example:

```html
<video src="riyaz.mp4">Error</video>
```

#### Attributes:

* `src` → video file URL
* `width` → adjusts width (height auto-adjusts)
* `controls` → shows play/pause controls
* `autoplay` → plays automatically on load
* `loop` → repeats video
* `preload` → loading behavior (`auto`, `metadata`, `none`)

---

### Anchor Tag (`<a>`)

* Creates hyperlinks
* Requires `href` attribute
* Can link to internal or external pages
* Supports `target` attribute

---

### Navigation Tag (`<nav>`)

* Encloses navigation menus
* Semantic element for navigation
* Commonly contains `<ul>`, `<ol>`, and `<a>`
* Improves accessibility (screen readers)

---

### Text Formatting Tags

* `<b>` → Bold
* `<i>` → Italic
* `<u>` → Underline
* `<s>` or `<strike>` → Strikethrough

> Used for styling and emphasis

---

### Preformatted Tag (`<pre>`)

* Preserves formatting
* Maintains whitespace and line breaks
* Useful for displaying code
* Enclosed within `<pre>` and `</pre>`

---

### Big / Small Tags

* `<big>` → Increases text size
* `<small>` → Decreases text size
* Less used (CSS preferred)

---

### Superscript / Subscript

* `<sup>` → Superscript
* `<sub>` → Subscript
* Used in equations and footnotes
* Changes position, not size

---

## Character Entity Reference

### What are Character Entity References

* Used to display reserved/special characters
* Syntax starts with `&` and ends with `;`

| Entity    | Output  |
| --------- | ------- |
| `&amp;`   | &       |
| `&nbsp;`  | (space) |
| `&minus;` | -       |
| `&quot;`  | "       |
| `&apos;`  | '       |

---

## Div Tag (`<div>`)

* **Purpose**: Container for other elements
* **Non-Semantic**: No inherent meaning
* **Styling**: Used with CSS for layout
* **Flexible**: Can use classes and IDs

---

## Span Tag (`<span>`)

* **Purpose**: Inline styling of text
* **Non-Semantic**: No specific meaning
* **Styling**: Used for color, font, effects
* **Inline Nature**: Does not break text flow

# Complete HTML Revision Notes

## Basic to Advanced \| HTML Living Standard / Modern HTML

> These notes consolidate the topics in your HTML Revision Notes, Phases
> 1-4, and Roadmap, then organize them into a practical reference.
> Examples use modern HTML syntax. HTML defines structure and meaning;
> CSS controls presentation; JavaScript adds behavior.

------------------------------------------------------------------------

## Table of Contents

- [1. What is HTML?](#1-what-is-html)
- [2. HTML Document Structure](#2-html-document-structure)
- [3. HTML Attributes](#3-html-attributes)
- [4. Text and Content Elements](#4-text-and-content-elements)
- [5. Links and Navigation](#5-links-and-navigation)
- [6. Images and Responsive Images](#6-images-and-responsive-images)
- [7. Lists](#7-lists)
- [8. Tables](#8-tables)
- [9. Forms](#9-forms)
- [10. Audio, Video, and Embedded Content](#10-audio-video-and-embedded-content)
- [11. Semantic HTML](#11-semantic-html)
- [12. Accessibility (A11Y)](#12-accessibility-a11y)
- [13. SEO-Related HTML](#13-seo-related-html)
- [14. HTML Entities and Special Characters](#14-html-entities-and-special-characters)
- [15. Metadata and Resource Elements](#15-metadata-and-resource-elements-in-head)
- [16. Advanced / Modern HTML Features](#16-advanced--modern-html-features)
- [17. Browser Storage APIs](#17-browser-storage-apis-javascript-apis-not-html-tags)
- [18. Responsive Design](#18-responsive-design-htmls-role)
- [19. Performance and Core Web Vitals](#19-performance-and-core-web-vitals)
- [20. HTML Validation and Developer Tools](#20-html-validation-and-browser-developer-tools)
- [21. Common Mistakes and Corrections](#21-common-mistakes-and-corrections)
- [22. Obsolete or Deprecated Elements](#22-obsolete-or-deprecated-elements-to-avoid)
- [23. Complete Real-World Example](#23-complete-real-world-example-accessible-registration-page)
- [24. Practice Roadmap and Revision Checklist](#24-practice-roadmap-and-revision-checklist)
- [25. Quick Interview Questions](#25-quick-interview-questions)

---

# 1. What is HTML?

**HTML (HyperText Markup Language)** is the standard markup language
used to describe the structure and meaning of web content.

-   **HTML:** structure and content.
-   **CSS:** presentation, layout, colors, typography, responsiveness.
-   **JavaScript:** behavior, interaction, application logic.
-   **Browser:** parses HTML into the DOM (Document Object Model),
    applies CSS, runs JavaScript, and renders the page.

HTML is a markup language, not a programming language. It describes
content using elements and attributes.

## 1.1 Tag, element, and attribute

``` html
<p class="intro">Hello, world!</p>
```

-   `<p>`: opening tag.
-   `</p>`: closing tag.
-   `Hello, world!`: text content.
-   `class="intro"`: attribute.
-   The complete construct is a paragraph **element**.

An element can contain text, other elements, or both. The elements
inside another element are its **children**; the containing element is
their **parent**.

## 1.2 Nesting

Correct nesting:

``` html
<p>This is <strong>important</strong> text.</p>
```

Incorrect nesting:

``` html
<!-- Incorrect: elements overlap rather than nest -->
<p><strong>Important text</p></strong>
```

Close elements in the reverse order in which they were opened. Some
elements have optional end tags under specific HTML parsing rules, but
writing clear, properly nested markup is best practice.

## 1.3 Element categories

-   **Normal elements:** usually have a start tag, content, and end tag,
    e.g. `p`, `div`, `button`.
-   **Void elements:** cannot contain content and have no end tag,
    e.g. `img`, `br`, `hr`, `input`, `meta`, `link`, `source`, `area`,
    `base`, `col`, `embed`, `param` (obsolete), `track`, `wbr`.
-   **Raw-text / escapable raw-text elements:** special parsing rules
    apply to elements such as `script`, `style`, `textarea`, and
    `title`.

HTML void elements should be written without a closing tag:

``` html
<img src="logo.png" alt="Company logo">
<br>
<hr>
<input type="email">
```

`<img />` is accepted in HTML syntax, but the slash is unnecessary. Do
not write `</img>`.

------------------------------------------------------------------------

# 2. HTML Document Structure

A standard HTML document:

``` html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="A short description of this page.">
  <title>My First HTML Page</title>
</head>
<body>
  <header>
    <h1>Hello, HTML!</h1>
  </header>

  <main>
    <p>This is my first web page.</p>
  </main>
</body>
</html>
```

### Document parts

  -----------------------------------------------------------------------
  Part                                Purpose
  ----------------------------------- -----------------------------------
  `<!doctype html>`                   Selects standards mode for modern
                                      HTML. It is a declaration, not an
                                      HTML element.

  `<html>`                            Root element containing the
                                      document.

  `lang="en"`                         Declares the primary language; use
                                      the correct language code,
                                      e.g. `hi`, `en`, `gu`.

  `<head>`                            Contains metadata, title, resource
                                      links, styles, and other
                                      information about the document.

  `<meta charset="UTF-8">`            Declares character encoding. Place
                                      it near the beginning of `head`.

  Viewport meta                       Helps mobile browsers use the
                                      device width for layout.

  `<title>`                           Names the document in the browser
                                      tab and is important for search
                                      results and bookmarks.

  `<body>`                            Contains the document's visible
                                      page content.
  -----------------------------------------------------------------------

### Important points

-   The usual file extension is `.html`; `.htm` is also recognized.
-   The common home-page filename is `index.html`.
-   Use lowercase, descriptive filenames and hyphens instead of spaces:
    `about-us.html`.
-   `!` followed by Emmet expansion in many editors generates a starter
    HTML document.
-   HTML tag names are case-insensitive in HTML documents, but lowercase
    is the convention.
-   Attribute values should normally be quoted.
-   Indentation does not usually change the rendered layout, but makes
    code readable.

## 2.1 Comments

Comments are not rendered as page content:

``` html
<!-- This is a single-line comment. -->

<!--
  This is a
  multi-line comment.
-->
```

Do not put sensitive information in comments. Users can inspect page
source.

## 2.2 Character encoding

Use UTF-8 so common languages and symbols can be represented:

``` html
<meta charset="UTF-8">
```

------------------------------------------------------------------------

# 3. HTML Attributes

Attributes provide additional information or configure an element.

``` html
<a href="https://example.com" target="_blank">Visit Example</a>
<img src="team.jpg" alt="The project team">
<input type="text" id="username" name="username">
```

## 3.1 Common global attributes

These can be used on many HTML elements:

  ----------------------------------------------------------------------------
  Attribute               Purpose                 Example
  ----------------------- ----------------------- ----------------------------
  `id`                    Unique identifier in a  `id="main"`
                          document                

  `class`                 Reusable grouping / CSS `class="card featured"`
                          or JS hook              

  `style`                 Inline CSS declaration  `style="color: red"`

  `title`                 Advisory information,   `title="More information"`
                          often shown as a        
                          tooltip                 

  `lang`                  Language of an          `lang="hi"`
                          element's content       

  `dir`                   Text direction: `ltr`,  `dir="rtl"`
                          `rtl`, `auto`           

  `hidden`                Indicates content is    `hidden`
                          not currently relevant  
                          for display             

  `tabindex`              Controls focusability   `tabindex="0"`
                          and tab order           

  `contenteditable`       Makes content editable  `contenteditable="true"`
                          by the user             

  `draggable`             Indicates whether an    `draggable="true"`
                          element can be dragged  

  `spellcheck`            Requests                `spellcheck="true"`
                          spelling/grammar        
                          checking                

  `data-*`                Stores custom data on   `data-product-id="42"`
                          an element              
  ----------------------------------------------------------------------------

`id` values should be unique within a document. A `class` can be reused
and an element can have multiple classes.

``` html
<article id="post-1" class="post featured">
  <h2>HTML Basics</h2>
</article>
```

## 3.2 Boolean attributes

A Boolean attribute is true when present; writing `required="false"`
does **not** make it false. Omit the attribute to make it false.

``` html
<input type="email" required>
<button disabled>Unavailable</button>
<video controls autoplay muted></video>
```

## 3.3 Custom data attributes

``` html
<button data-user-id="25" data-role="admin">View user</button>

<script>
  const button = document.querySelector("button");
  console.log(button.dataset.userId); // "25"
  console.log(button.dataset.role);   // "admin"
</script>
```

The values are strings. `data-user-id` becomes `dataset.userId`.

------------------------------------------------------------------------

# 4. Text and Content Elements

## 4.1 Headings: `h1` to `h6`

``` html
<h1>HTML Guide</h1>
<h2>Forms</h2>
<h3>Input Types</h3>
<h4>Email Input</h4>
<h5>Validation</h5>
<h6>Additional Notes</h6>
```

-   `h1` is the highest-level heading; `h6` is the lowest.
-   Use headings to represent document hierarchy, not merely to make
    text large.
-   Do not skip heading levels without a structural reason.
-   A page often has one main `h1`, but HTML does not impose a strict
    one-`h1` rule. Use a logical heading outline.

## 4.2 Paragraph: `p`

``` html
<p>HTML describes the structure of web content.</p>
<p>This is another paragraph.</p>
```

Browsers normally display paragraphs as separate blocks with spacing.

## 4.3 Line break: `br`

Use for a meaningful line break, such as an address or poem---not to
create page spacing.

``` html
<p>
  21 Example Street<br>
  Ahmedabad, Gujarat<br>
  India
</p>
```

## 4.4 Thematic break: `hr`

Represents a thematic change between sections:

``` html
<p>First topic.</p>
<hr>
<p>Next topic.</p>
```

## 4.5 Preformatted text: `pre`

Whitespace and line breaks inside `pre` are preserved:

``` html
<pre>
Name       Age
Riyaz      25
Aman       27
</pre>
```

Often combined with `code` for source code:

``` html
<pre><code>const message = "Hello";</code></pre>
```

## 4.6 Text-level semantic and formatting elements

  -----------------------------------------------------------------------
  Element                             Meaning / use
  ----------------------------------- -----------------------------------
  `strong`                            Strong importance, seriousness, or
                                      urgency

  `b`                                 Draws attention without adding
                                      importance

  `em`                                Stress emphasis

  `i`                                 Alternate voice, term, or mood

  `mark`                              Highlight relevant text

  `small`                             Side comments or fine print

  `s`                                 Content that is no longer accurate
                                      or relevant

  `del`                               Deleted content in an edit

  `ins`                               Inserted content in an edit

  `u`                                 Non-textual annotation, such as a
                                      proper-name mark; do not use merely
                                      for decoration

  `sub`                               Subscript

  `sup`                               Superscript

  `code`                              Fragment of computer code

  `kbd`                               User input from keyboard

  `samp`                              Sample output from a program

  `var`                               Variable name

  `q`                                 Short inline quotation

  `blockquote`                        Longer quoted section

  `cite`                              Title of a creative work

  `abbr`                              Abbreviation or acronym

  `dfn`                               Defining instance of a term

  `time`                              Machine-readable date/time

  `data`                              Human-readable content with a
                                      machine-readable value

  `wbr`                               Optional line-break opportunity
  -----------------------------------------------------------------------

Examples:

``` html
<p><strong>Warning:</strong> Save your work before closing.</p>
<p>I <em>really</em> recommend learning semantic HTML.</p>
<p>Sale price: <del>₹2,000</del> <ins>₹1,500</ins></p>
<p>Water: H<sub>2</sub>O</p>
<p>Square: x<sup>2</sup></p>
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save.</p>
<p>Output: <samp>File saved successfully.</samp></p>
<p>The variable <var>total</var> stores the sum.</p>
<p><abbr title="HyperText Markup Language">HTML</abbr> is a markup language.</p>
<p><time datetime="2026-11-24">24 November 2026</time></p>
```

### Important distinctions

-   `strong` is semantic importance; `b` is attention without that
    meaning.
-   `em` adds stress emphasis; `i` marks alternate voice or terminology.
-   `del` and `ins` communicate edits; `s` indicates information that is
    no longer relevant.
-   Use CSS for purely visual styling.

## 4.7 `div` and `span`

-   `div`: generic flow/container element with no inherent semantic
    meaning; commonly used to group block-level content.
-   `span`: generic phrasing/inline container with no inherent semantic
    meaning.

``` html
<div class="profile-card">
  <h2>Riyaz</h2>
  <p>Frontend developer</p>
  <p>Status: <span class="available">Available</span></p>
</div>
```

Use a semantic element when one accurately describes the content; use
`div` or `span` when no more meaningful element fits.

------------------------------------------------------------------------

# 5. Links and Navigation

The anchor element creates hyperlinks.

``` html
<a href="https://developer.mozilla.org/">MDN Web Docs</a>
```

## 5.1 Absolute and relative URLs

``` html
<!-- Absolute URL -->
<a href="https://example.com/about">About</a>

<!-- Relative URL: same folder -->
<a href="about.html">About</a>

<!-- Relative URL: child folder -->
<a href="pages/contact.html">Contact</a>

<!-- Parent folder -->
<a href="../index.html">Home</a>
```

## 5.2 Link to a section on the same page

``` html
<a href="#contact">Go to contact section</a>

<section id="contact">
  <h2>Contact</h2>
  <p>Contact details...</p>
</section>
```

## 5.3 Useful anchor attributes and schemes

``` html
<a href="mailto:hello@example.com">Send email</a>
<a href="tel:+911234567890">Call us</a>
<a href="report.pdf" download>Download report</a>
<a href="https://example.com" target="_blank" rel="noopener">
  Open external site
</a>
```

-   `href`: destination URL.
-   `target="_blank"`: opens a new browsing context, commonly a new tab.
-   `rel="noopener"`: prevents the opened page from controlling the
    opener through `window.opener`; modern browsers generally apply this
    protection to `_blank`, but explicit use is clear.
-   `rel="noreferrer"`: also suppresses the referrer header.
-   `download`: asks the browser to download a resource; behavior
    depends on origin and response headers.
-   `mailto:` opens an email handler; `tel:` opens a calling handler
    where supported.

Do not use `href="#"` as a substitute for a button. Use `<button>` for
an action and `<a>` for navigation.

------------------------------------------------------------------------

# 6. Images and Responsive Images

## 6.1 `img`

``` html
<img src="images/team.jpg" alt="Three developers working together"
     width="800" height="500">
```

Important attributes:

-   `src`: image URL/path.
-   `alt`: text alternative. Describe the image's purpose or meaningful
    information.
-   `width` and `height`: intrinsic dimensions; help reserve layout
    space and reduce layout shift.
-   `loading="lazy"`: defers loading of off-screen images.
-   `loading="eager"`: requests normal eager loading.
-   `decoding="async"`: allows asynchronous image decoding where
    supported.

For a decorative image, use an empty alt value:

``` html
<img src="decorative-line.svg" alt="">
```

Do not omit `alt` casually. A missing `alt` can cause assistive
technology to announce a filename or URL.

## 6.2 Lazy loading

``` html
<img src="gallery/photo-1.jpg" alt="Mountain landscape"
     width="1200" height="800" loading="lazy">
```

Use lazy loading for images below the initial viewport. Do not lazy-load
the page's likely Largest Contentful Paint (LCP) hero image; it may
delay the main content.

## 6.3 `picture` and `source`

Use `<picture>` for art direction or format alternatives:

``` html
<picture>
  <source media="(max-width: 600px)" srcset="images/portrait-mobile.jpg">
  <source type="image/avif" srcset="images/landscape.avif">
  <img src="images/landscape.jpg" alt="A landscape at sunrise">
</picture>
```

The `img` element is the fallback and provides the alternative text.

## 6.4 `srcset` and `sizes`

Let the browser choose an appropriate image candidate:

``` html
<img
  src="photo-800.jpg"
  srcset="photo-400.jpg 400w,
          photo-800.jpg 800w,
          photo-1200.jpg 1200w"
  sizes="(max-width: 600px) 100vw, 50vw"
  width="1200"
  height="800"
  alt="A lake surrounded by mountains">
```

-   `srcset` lists image candidates and their widths (`w`) or pixel
    densities (`x`).
-   `sizes` tells the browser how much layout width the image is
    expected to occupy.
-   These attributes help the browser select a suitable resource; they
    do not themselves resize the image in CSS.

------------------------------------------------------------------------

# 7. Lists

## 7.1 Unordered list: `ul`

Use when order is not important:

``` html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

## 7.2 Ordered list: `ol`

Use for ordered steps or rankings:

``` html
<ol>
  <li>Create an HTML file.</li>
  <li>Write the document structure.</li>
  <li>Open it in a browser.</li>
</ol>
```

Useful `ol` attributes:

``` html
<ol type="A" start="3">
  <li>Third item</li>
  <li>Fourth item</li>
</ol>

<ol reversed>
  <li>Third</li>
  <li>Second</li>
  <li>First</li>
</ol>
```

-   `type`: numbering style (`1`, `A`, `a`, `I`, `i`).
-   `start`: starting number.
-   `reversed`: counts down.

## 7.3 Description list: `dl`

For terms and their descriptions:

``` html
<dl>
  <dt>HTML</dt>
  <dd>Defines web page structure.</dd>
  <dt>CSS</dt>
  <dd>Controls presentation and layout.</dd>
</dl>
```

## 7.4 Nested lists

``` html
<ul>
  <li>Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
    </ul>
  </li>
  <li>Backend</li>
</ul>
```

A list's direct children should be list items (`li`); nested lists
normally belong inside an `li`.

------------------------------------------------------------------------

# 8. Tables

Use tables for **tabular data**, not for page layout.

## 8.1 Basic structure

``` html
<table>
  <caption>Employee Information</caption>
  <thead>
    <tr>
      <th scope="col">ID</th>
      <th scope="col">Name</th>
      <th scope="col">Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Riyaz</td>
      <td>₹50,000</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Aman</td>
      <td>₹45,000</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row" colspan="2">Total</th>
      <td>₹95,000</td>
    </tr>
  </tfoot>
</table>
```

## 8.2 Table elements

  Element             Purpose
  ------------------- ------------------------------------
  `table`             Table container
  `caption`           Table title/description
  `thead`             Header rows
  `tbody`             Main data rows
  `tfoot`             Footer/summary rows
  `tr`                Table row
  `th`                Header cell
  `td`                Data cell
  `colgroup`, `col`   Group/describe columns for styling

## 8.3 `colspan` and `rowspan`

``` html
<table>
  <tr>
    <th>Name</th>
    <th colspan="2">Contact</th>
  </tr>
  <tr>
    <td>Riyaz</td>
    <td>Email</td>
    <td>Phone</td>
  </tr>
  <tr>
    <td rowspan="2">Aman</td>
    <td>Work email</td>
    <td>111</td>
  </tr>
  <tr>
    <td>Personal email</td>
    <td>222</td>
  </tr>
</table>
```

-   `colspan`: a cell spans multiple columns.
-   `rowspan`: a cell spans multiple rows.
-   Use `scope="col"` or `scope="row"` on simple header cells to clarify
    relationships.
-   For complex tables, use appropriate header IDs and `headers`
    associations.

------------------------------------------------------------------------

# 9. Forms

Forms collect data and submit it to a server or handle it with
JavaScript.

## 9.1 Form structure

``` html
<form action="/register" method="post">
  <label for="name">Name</label>
  <input id="name" name="name" type="text" required>

  <button type="submit">Register</button>
</form>
```

-   `action`: URL that receives the form submission.
-   `method`: HTTP method, commonly `get` or `post`.
-   `name`: key used when the control's value is submitted.
-   `id`: identifies the control and connects it to a label.
-   `enctype`: encoding type; use `multipart/form-data` for file
    uploads.
-   `autocomplete`: allows browser autofill hints.
-   `target`: browsing context for the response.
-   `novalidate`: disables built-in constraint validation for the form.

### GET vs POST

-   **GET:** form data is appended to the URL as a query string.
    Suitable for searches and retrieval; avoid submitting sensitive data
    this way.
-   **POST:** form data is sent in the request body. Common for
    creating/updating data and file uploads.
-   Neither method replaces server-side validation or authorization.

## 9.2 Label

``` html
<label for="email">Email address</label>
<input type="email" id="email" name="email">
```

The `for` value must match the control's `id`. A label can also wrap its
control:

``` html
<label>
  <input type="checkbox" name="updates">
  Send me updates
</label>
```

Labels improve usability and accessibility.

## 9.3 Input types

``` html
<input type="text">
<input type="password">
<input type="email">
<input type="url">
<input type="tel">
<input type="search">
<input type="number">
<input type="range">
<input type="date">
<input type="time">
<input type="datetime-local">
<input type="month">
<input type="week">
<input type="checkbox">
<input type="radio">
<input type="file">
<input type="color">
<input type="hidden">
<input type="submit">
<input type="reset">
<input type="button">
<input type="image" src="submit.png" alt="Submit">
```

Notes: - `tel` does not enforce a universal phone-number format; use an
appropriate `pattern` if needed. - `number` is for numeric quantities,
not phone numbers or postal codes. - `hidden` is not a security
mechanism; users can inspect or modify it. - `file` can use `accept` to
guide the file picker, but the server must verify uploaded files.

## 9.4 Common input attributes

  Attribute                  Meaning
  -------------------------- ---------------------------------------------------------
  `name`                     Submission key
  `value`                    Initial/submitted value
  `placeholder`              Hint; not a replacement for a label
  `required`                 Value must be supplied
  `readonly`                 User cannot edit; value is still submitted
  `disabled`                 Control is unavailable and not submitted
  `checked`                  Initially selects checkbox/radio
  `selected`                 Initially selects an option
  `multiple`                 Allows multiple values/files where supported
  `min`, `max`               Numeric/date bounds
  `step`                     Allowed increment
  `minlength`, `maxlength`   Text length constraints
  `pattern`                  Regular-expression constraint for supported text inputs
  `autocomplete`             Autofill purpose hint
  `autofocus`                Requests initial focus; use sparingly
  `accept`                   File picker type hint
  `list`                     Connects an input to a `datalist`

## 9.5 Radio buttons

Use the same `name` to create one mutually exclusive group. Give each
choice a distinct `value`.

``` html
<fieldset>
  <legend>Choose a plan</legend>
  <label><input type="radio" name="plan" value="basic" checked> Basic</label>
  <label><input type="radio" name="plan" value="pro"> Pro</label>
</fieldset>
```

## 9.6 Checkboxes

Each checkbox can be selected independently:

``` html
<fieldset>
  <legend>Skills</legend>
  <label><input type="checkbox" name="skills" value="html"> HTML</label>
  <label><input type="checkbox" name="skills" value="css"> CSS</label>
  <label><input type="checkbox" name="skills" value="js"> JavaScript</label>
</fieldset>
```

## 9.7 Select and option

``` html
<label for="country">Country</label>
<select id="country" name="country" required>
  <option value="">Choose a country</option>
  <option value="in">India</option>
  <option value="us">United States</option>
  <option value="uk">United Kingdom</option>
</select>
```

Grouped choices:

``` html
<select name="course">
  <optgroup label="Frontend">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
  </optgroup>
  <optgroup label="Backend">
    <option value="node">Node.js</option>
  </optgroup>
</select>
```

## 9.8 Textarea

``` html
<label for="message">Message</label>
<textarea id="message" name="message" rows="5"
          cols="40" maxlength="500"
          placeholder="Write your message"></textarea>
```

Unlike `input`, the initial text for a textarea goes between its tags.

## 9.9 Buttons

``` html
<button type="button">Run action</button>
<button type="submit">Submit form</button>
<button type="reset">Reset form</button>
```

Inside a form, a button without a specified type generally behaves as a
submit button. Specify `type` explicitly to avoid accidental
submissions.

## 9.10 Other form elements

### Fieldset and legend

Group related controls:

``` html
<fieldset>
  <legend>Personal details</legend>
  <label for="full-name">Full name</label>
  <input id="full-name" name="fullName">
</fieldset>
```

### Datalist

Provides suggestions while allowing other values:

``` html
<label for="browser">Browser</label>
<input id="browser" name="browser" list="browsers">
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Edge">
</datalist>
```

### Output

Represents the result of a calculation or user action:

``` html
<form oninput="result.value = Number(a.value) + Number(b.value)">
  <input type="number" id="a" value="2">
  +
  <input type="number" id="b" value="3">
  =
  <output name="result" for="a b">5</output>
</form>
```

## 9.11 Native HTML validation

``` html
<form>
  <label for="username">Username</label>
  <input id="username" name="username" required
         minlength="3" maxlength="20"
         pattern="[A-Za-z0-9_]+">

  <label for="age">Age</label>
  <input id="age" name="age" type="number" min="18" max="100">

  <label for="email-address">Email</label>
  <input id="email-address" name="email" type="email" required>

  <button type="submit">Submit</button>
</form>
```

-   `required`: value must be present.
-   `type="email"`: checks basic email syntax.
-   `min` / `max`: numeric or date bounds.
-   `minlength` / `maxlength`: text length.
-   `pattern`: regular-expression constraint.
-   `step`: numeric/date increment.

Browser validation improves UX but is not a security boundary. Always
validate and sanitize data on the server too. Client-side checks can be
bypassed.

## 9.12 `readonly` vs `disabled`

  -----------------------------------------------------------------------
  `readonly`                          `disabled`
  ----------------------------------- -----------------------------------
  User cannot edit the value          User cannot interact with the
                                      control

  Usually remains focusable           Normally removed from tab order

  Value is submitted                  Value is not submitted

  Applies to supported text-like      Applies to many form controls
  controls                            
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# 10. Audio, Video, and Embedded Content

## 10.1 Audio

``` html
<audio controls>
  <source src="audio/song.mp3" type="audio/mpeg">
  <source src="audio/song.ogg" type="audio/ogg">
  Your browser does not support audio playback.
</audio>
```

Common attributes: `controls`, `autoplay`, `loop`, `muted`, `preload`.

Autoplay with sound is commonly blocked by browsers. Avoid autoplay
unless there is a strong reason.

## 10.2 Video

``` html
<video controls width="640" height="360"
       poster="images/video-cover.jpg">
  <source src="videos/demo.mp4" type="video/mp4">
  <source src="videos/demo.webm" type="video/webm">
  Your browser does not support HTML video.
</video>
```

Common attributes: - `controls`: browser playback controls. -
`autoplay`: requests automatic playback. - `muted`: starts muted. -
`loop`: repeats playback. - `poster`: preview image before playback. -
`preload`: hints how much media to preload (`none`, `metadata`, `auto`).

## 10.3 Captions and subtitles: `track`

``` html
<video controls>
  <source src="lesson.mp4" type="video/mp4">
  <track src="captions-en.vtt" kind="captions"
         srclang="en" label="English" default>
</video>
```

Captions improve accessibility. A WebVTT (`.vtt`) file contains timed
text cues.

## 10.4 iframe

Embeds another browsing context, often used for maps or video players:

``` html
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  title="HTML tutorial video"
  width="560"
  height="315"
  loading="lazy"
  allowfullscreen>
</iframe>
```

-   Give an iframe a descriptive `title`.
-   Use a provider's official embed URL; many websites block being
    embedded.
-   Consider `sandbox` and a restrictive permissions policy for
    untrusted embeds.
-   Do not embed arbitrary pages without considering security and
    privacy.

------------------------------------------------------------------------

# 11. Semantic HTML

Semantic elements describe the role and meaning of content. They help
browsers, search engines, developers, and assistive technologies
understand page structure.

## 11.1 Main structural elements

  Element      Purpose
  ------------ -----------------------------------------------------
  `header`     Introductory content for a page or section
  `nav`        Major navigation links
  `main`       Dominant content of the document
  `section`    Thematic grouping, usually with a heading
  `article`    Self-contained, independently distributable content
  `aside`      Tangential/related content
  `footer`     Footer for a page or section
  `address`    Contact information for a person or organization
  `search`     Search or filtering controls
  `h1`--`h6`   Heading hierarchy

## 11.2 Example semantic page

``` html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Developer Blog</title>
</head>
<body>
  <header>
    <h1>Developer Blog</h1>
    <nav aria-label="Main navigation">
      <a href="/">Home</a>
      <a href="/articles.html">Articles</a>
      <a href="/contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section aria-labelledby="latest-heading">
      <h2 id="latest-heading">Latest articles</h2>

      <article>
        <header>
          <h3>Getting Started with HTML</h3>
          <p>Published <time datetime="2026-11-24">24 November 2026</time></p>
        </header>
        <p>HTML gives meaning and structure to web content.</p>
        <a href="/html-basics.html">Read article</a>
      </article>
    </section>

    <aside>
      <h2>Related topics</h2>
      <p>Explore CSS and JavaScript.</p>
    </aside>
  </main>

  <footer>
    <p>&copy; 2026 Developer Blog</p>
  </footer>
</body>
</html>
```

## 11.3 `article` vs `section` vs `div`

-   `article`: content that can stand on its own, such as a blog post,
    news story, or forum post.
-   `section`: a thematic grouping within a page, generally with a
    heading.
-   `div`: generic container when no semantic element is appropriate.

A page can contain multiple `header`, `footer`, `section`, and `article`
elements. Usually there should be one main content element (`main`)
representing the page's dominant content.

## 11.4 Other useful semantic elements

``` html
<figure>
  <img src="chart.png" alt="Sales increased during the year">
  <figcaption>Annual sales trend.</figcaption>
</figure>

<details>
  <summary>What is HTML?</summary>
  <p>HTML is the markup language used to structure web content.</p>
</details>
```

-   `figure` and `figcaption`: self-contained media/content and its
    caption.
-   `details` and `summary`: disclosure widget with expandable content.
-   `dialog`: dialog box or modal interface; JavaScript is commonly used
    to show and close it.
-   `menu`: list of commands or menu items (not a general replacement
    for every navigation list).

------------------------------------------------------------------------

# 12. Accessibility (A11Y)

Accessibility means making content and controls usable by people with
different abilities and assistive technologies.

## 12.1 Core practices

1.  Use semantic HTML before adding ARIA.
2.  Provide meaningful `alt` text for informative images; use `alt=""`
    for decorative images.
3.  Associate every form control with a label.
4.  Use real buttons for actions and links for navigation.
5.  Keep a logical heading hierarchy.
6.  Ensure keyboard users can reach and operate interactive controls.
7.  Use descriptive link text; avoid vague repeated labels such as
    "click here".
8.  Provide captions/transcripts for relevant media.
9.  Do not communicate information using color alone.
10. Set the correct page language with `lang`.

## 12.2 ARIA basics

ARIA (Accessible Rich Internet Applications) adds accessibility
information when native HTML does not express the needed role, name,
state, or relationship.

``` html
<button type="button" aria-label="Close dialog">×</button>

<nav aria-label="Primary navigation">
  <a href="/">Home</a>
  <a href="/about">About</a>
</nav>

<span aria-hidden="true">★</span>
```

Common attributes: - `aria-label`: accessible name. - `aria-labelledby`:
references another element that labels this element. -
`aria-describedby`: references a description. - `aria-hidden="true"`:
hides an element from the accessibility tree (not necessarily
visually). - `aria-expanded`: indicates expanded/collapsed state. -
`aria-controls`: identifies content controlled by an element. -
`aria-live`: announces dynamic updates. - `role`: supplies a role when
native semantics are insufficient.

**Rule:** Prefer a native `<button>` over `<div role="button">`. ARIA
does not automatically add keyboard behavior, focus behavior, or
functionality.

## 12.3 Keyboard accessibility

-   Interactive elements should be keyboard-operable.
-   Preserve a visible focus indicator.
-   Avoid positive `tabindex` values that create confusing custom tab
    order.
-   Native links, buttons, inputs, and selects already provide useful
    keyboard behavior.

------------------------------------------------------------------------

# 13. SEO-Related HTML

SEO is broader than HTML, but good document markup helps search engines
interpret content.

## 13.1 Head metadata

``` html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>HTML Tutorial for Beginners</title>
  <meta name="description"
        content="Learn HTML structure, elements, forms, tables, and semantic markup.">
  <meta name="author" content="Riyaz">
  <link rel="canonical" href="https://example.com/html-tutorial">
  <link rel="icon" href="/favicon.ico">
</head>
```

-   `title`: unique, descriptive page title.
-   `description`: concise summary that may be used in search snippets.
-   `author`: document author metadata.
-   `canonical`: preferred URL for duplicate or similar pages; use
    carefully.
-   `icon`: favicon.
-   A URL slug is part of the URL, not a meta tag.

## 13.2 Social sharing metadata

Open Graph example:

``` html
<meta property="og:title" content="HTML Tutorial">
<meta property="og:description" content="A practical HTML guide.">
<meta property="og:type" content="article">
<meta property="og:url" content="https://example.com/html-tutorial">
<meta property="og:image" content="https://example.com/images/html.jpg">
```

These tags help platforms create link previews. Platform support and
exact behavior vary.

## 13.3 SEO best practices

-   Write a useful, unique title and description.
-   Use headings that reflect the content hierarchy.
-   Use descriptive links and meaningful image alternatives.
-   Use semantic elements appropriately.
-   Make pages mobile-friendly and fast.
-   Provide crawlable links and avoid hiding important content behind
    inaccessible interactions.
-   Keep URLs descriptive and stable.
-   Do not stuff keywords or add headings purely for search engines.

------------------------------------------------------------------------

# 14. HTML Entities and Special Characters

Entities represent reserved characters or symbols.

  Entity       Character / meaning
  ------------ ---------------------
  `&lt;`       `<`
  `&gt;`       `>`
  `&amp;`      `&`
  `&quot;`     `"`
  `&apos;`     `'`
  `&nbsp;`     non-breaking space
  `&copy;`     ©
  `&reg;`      ®
  `&trade;`    ™
  `&euro;`     €
  `&pound;`    £
  `&yen;`      ¥
  `&mdash;`    ---
  `&ndash;`    --
  `&hellip;`   ...
  `&times;`    ×
  `&divide;`   ÷

Example:

``` html
<p>5 &lt; 10 and 10 &gt; 5.</p>
<p>Tom &amp; Jerry</p>
<p>&copy; 2026 My Website</p>
```

Numeric character references are also possible, e.g. `&#169;` for ©. Use
UTF-8 directly for many characters when appropriate.

------------------------------------------------------------------------

# 15. Metadata and Resource Elements in `head`

## 15.1 Common metadata

``` html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="Page description">
<meta name="theme-color" content="#ffffff">
```

## 15.2 Link external resources

``` html
<link rel="icon" href="/favicon.ico">
<link rel="stylesheet" href="/css/styles.css">
```

## 15.3 Add CSS and JavaScript

``` html
<style>
  body { font-family: Arial, sans-serif; }
</style>

<script src="/js/app.js" defer></script>
```

-   `style` contains CSS.
-   `script` contains or loads JavaScript.
-   `defer` downloads an external classic script while parsing and
    executes it after parsing, preserving order among deferred classic
    scripts.
-   `async` executes an external script as soon as it is ready;
    execution order is not guaranteed.
-   Module scripts (`type="module"`) are deferred by default.

------------------------------------------------------------------------

# 16. Advanced / Modern HTML Features

## 16.1 `contenteditable`

Makes an element's content editable by the user:

``` html
<p contenteditable="true">You can edit this paragraph.</p>
```

This alone does not provide persistence, collaboration, sanitization, or
a full rich-text editor. Those require application logic.

## 16.2 `details` and `summary`

``` html
<details>
  <summary>Show answer</summary>
  <p>HTML stands for HyperText Markup Language.</p>
</details>
```

Add `open` to show the details initially:

``` html
<details open>
  <summary>More information</summary>
  <p>This content is initially visible.</p>
</details>
```

## 16.3 `progress` and `meter`

``` html
<label for="upload">Upload progress</label>
<progress id="upload" value="70" max="100">70%</progress>

<label for="disk">Disk usage</label>
<meter id="disk" min="0" max="100" low="30" high="80"
       optimum="20" value="65">65%</meter>
```

-   `progress`: completion progress of a task.
-   `meter`: scalar measurement within a known range, such as disk usage
    or rating.

## 16.4 `template`

Stores inert markup that is not rendered until code clones and inserts
it:

``` html
<template id="user-card-template">
  <article class="user-card">
    <h2 class="user-name"></h2>
  </article>
</template>

<div id="users"></div>

<script>
  const template = document.querySelector("#user-card-template");
  const card = template.content.cloneNode(true);
  card.querySelector(".user-name").textContent = "Riyaz";
  document.querySelector("#users").append(card);
</script>
```

Use `textContent` for untrusted text rather than injecting it as HTML.

## 16.5 `noscript`

Provides fallback content when scripting is disabled or unavailable:

``` html
<noscript>
  <p>This site needs JavaScript for some features.</p>
</noscript>
```

## 16.6 Dialog

``` html
<dialog id="info-dialog">
  <p>Welcome!</p>
  <form method="dialog">
    <button>Close</button>
  </form>
</dialog>

<button id="open-dialog" type="button">Open dialog</button>

<script>
  const dialog = document.querySelector("#info-dialog");
  document.querySelector("#open-dialog").addEventListener("click", () => {
    dialog.showModal();
  });
</script>
```

A modal dialog opened with `showModal()` provides built-in modal
behavior. Always provide a clear way to close it and manage focus
appropriately.

------------------------------------------------------------------------

# 17. Browser Storage APIs (JavaScript APIs, not HTML tags)

HTML documents can use browser APIs through JavaScript. `localStorage`
and `sessionStorage` are Web Storage APIs, not HTML elements.

## 17.1 localStorage

Persists data across browser restarts for the same origin, until
cleared:

``` html
<script>
  localStorage.setItem("username", "Riyaz");

  const username = localStorage.getItem("username");
  console.log(username);

  localStorage.removeItem("username");
  // localStorage.clear(); // removes all keys for this origin
</script>
```

## 17.2 sessionStorage

Stores data for the page's browsing session (typically scoped to a tab):

``` js
sessionStorage.setItem("temporary-token", "abc123");
const token = sessionStorage.getItem("temporary-token");
sessionStorage.removeItem("temporary-token");
```

### Differences

  -----------------------------------------------------------------------
  localStorage                        sessionStorage
  ----------------------------------- -----------------------------------
  Persists across browser restarts    Usually ends when the tab/session
                                      ends

  Shared by same-origin pages in the  Scoped to a top-level browsing
  same storage area                   context and origin

  Explicitly remove or clear it       Removed when the page session ends
  -----------------------------------------------------------------------

Both store strings. Convert objects with `JSON.stringify()` and
`JSON.parse()`:

``` js
const user = { name: "Riyaz", role: "developer" };
localStorage.setItem("user", JSON.stringify(user));

const savedUser = JSON.parse(localStorage.getItem("user") || "null");
```

Do not store passwords, sensitive secrets, or session credentials in Web
Storage without understanding the security implications. JavaScript
running on the origin can access it.

------------------------------------------------------------------------

# 18. Responsive Design: HTML's Role

Responsive design is primarily implemented with CSS, but HTML supplies
important support.

Viewport metadata:

``` html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Responsive images:

``` html
<picture>
  <source media="(max-width: 600px)" srcset="small-banner.jpg">
  <img src="large-banner.jpg" alt="Website banner">
</picture>
```

Use flexible content, appropriate image dimensions, and semantic
structure. CSS media queries, flexible layouts, and fluid sizing do most
of the layout work.

------------------------------------------------------------------------

# 19. Performance and Core Web Vitals

Good HTML can support performance:

-   Add `width` and `height` to images to reserve space.
-   Lazy-load off-screen images, not the critical hero/LCP image.
-   Use responsive image candidates (`srcset`, `sizes`).
-   Avoid unnecessary markup and deeply nested structures.
-   Load scripts with suitable `defer`, `async`, or module behavior.
-   Include meaningful alt text and semantic structure.

## 19.1 Core Web Vitals

  -----------------------------------------------------------------------
  Metric                  Measures                Good target
  ----------------------- ----------------------- -----------------------
  LCP (Largest Contentful Loading performance     ≤ 2.5 seconds
  Paint)                                          

  INP (Interaction to     Responsiveness to       ≤ 200 milliseconds
  Next Paint)             interactions            

  CLS (Cumulative Layout  Visual stability        ≤ 0.1
  Shift)                                          
  -----------------------------------------------------------------------

FCP (First Contentful Paint) measures when the first content is
rendered. It is a useful performance metric, but is not one of the three
Core Web Vitals.

------------------------------------------------------------------------

# 20. HTML Validation and Browser Developer Tools

## 20.1 Validate HTML

Use the W3C Nu HTML Checker to identify markup errors and warnings.
Validation does not guarantee accessibility, security, good SEO, or
correct application behavior.

## 20.2 Browser tools

-   **View Page Source:** shows the HTML source delivered by the server;
    common shortcut is `Ctrl + U`.
-   **Inspect / Developer Tools:** shows the live DOM, computed styles,
    network requests, console messages, and more.
-   The live DOM can differ from the original source because the browser
    parses HTML and JavaScript can modify it.

## 20.3 Useful references

-   MDN Web Docs: `https://developer.mozilla.org/docs/Web/HTML`
-   WHATWG HTML Standard: `https://html.spec.whatwg.org/`
-   W3C Nu HTML Checker: `https://validator.w3.org/nu/`

------------------------------------------------------------------------

# 21. Common Mistakes and Corrections

  ---------------------------------------------------------------------------
  Incorrect / weak practice           Better practice
  ----------------------------------- ---------------------------------------
  `<image src="x.png">`               `<img src="x.png" alt="Description">`

  `<img scr="x.png">`                 `src`, not `scr`

  `<p><strong>Text</p></strong>`      Properly nest and close elements

  `<input>` without a label           Associate a `<label>` with the input

  Placeholder used as the only label  Provide a visible label

  Table used to position a page       Use CSS layout; reserve tables for
                                      tabular data

  `<div>` used for every region       Use semantic elements where appropriate

  `<a href="#">Save</a>` for an       Use
  action                              `<button type="button">Save</button>`

  `disabled` when value must be       Consider `readonly` where supported
  submitted                           

  Relying only on browser validation  Validate again on the server

  Lazy-loading every image including  Eager-load critical above-the-fold
  hero                                imagery

  Using `br` repeatedly for spacing   Use CSS margins and layout

  Assuming hidden inputs are secure   Treat all client-submitted values as
                                      untrusted

  Using ARIA instead of native        Prefer native semantic HTML first
  controls                            
  ---------------------------------------------------------------------------

------------------------------------------------------------------------

# 22. Obsolete or Deprecated Elements to Avoid

Do not use old presentational elements in new projects. Use CSS for
presentation and modern semantic HTML for meaning.

Examples to recognize in legacy code:

-   `font`, `center`, `big`
-   `strike`, `tt`
-   `marquee`, `blink`
-   `frameset`, `frame`, `noframes`
-   `acronym`, `applet`, `basefont`
-   `dir`, `isindex`, `keygen`, `menuitem`
-   `param` in modern media embedding patterns

Some old elements may still render in browsers for compatibility, but
they should not be used in new work. The `<big>` element from older
notes is obsolete; use CSS. The `<s>` element is still valid and has a
specific meaning (content no longer accurate/relevant).

------------------------------------------------------------------------

# 23. Complete Real-World Example: Accessible Registration Page

``` html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="Register for a web development course.">
  <title>Course Registration</title>
</head>
<body>
  <header>
    <h1>Web Development Course</h1>
    <nav aria-label="Main navigation">
      <a href="#course">Course</a>
      <a href="#registration">Register</a>
    </nav>
  </header>

  <main>
    <section id="course">
      <h2>Learn web development</h2>
      <picture>
        <source media="(max-width: 600px)" srcset="course-mobile.jpg">
        <img src="course-desktop.jpg"
             alt="Students learning web development"
             width="1200" height="600">
      </picture>
      <p>Start with HTML, then learn CSS and JavaScript.</p>
    </section>

    <section id="registration">
      <h2>Registration form</h2>

      <form action="/register" method="post">
        <p>
          <label for="full-name">Full name</label>
          <input id="full-name" name="fullName" type="text"
                 autocomplete="name" required minlength="2">
        </p>

        <p>
          <label for="email">Email</label>
          <input id="email" name="email" type="email"
                 autocomplete="email" required>
        </p>

        <p>
          <label for="phone">Phone</label>
          <input id="phone" name="phone" type="tel"
                 autocomplete="tel">
        </p>

        <fieldset>
          <legend>Learning mode</legend>
          <label><input type="radio" name="mode" value="online" required> Online</label>
          <label><input type="radio" name="mode" value="classroom"> Classroom</label>
        </fieldset>

        <p>
          <label for="level">Current level</label>
          <select id="level" name="level" required>
            <option value="">Select level</option>
            <option value="beginner">Beginner</option>
            <option value="intermediate">Intermediate</option>
          </select>
        </p>

        <p>
          <label for="message">Additional message</label>
          <textarea id="message" name="message" rows="4"></textarea>
        </p>

        <p>
          <label>
            <input type="checkbox" name="terms" value="accepted" required>
            I agree to the terms.
          </label>
        </p>

        <button type="submit">Submit registration</button>
        <button type="reset">Clear form</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Web Development Course</p>
  </footer>
</body>
</html>
```

This example demonstrates document structure, metadata, navigation,
semantic layout, headings, responsive image markup, labels,
text/email/tel inputs, radio buttons, select, textarea, checkbox, native
validation, buttons, and footer.

------------------------------------------------------------------------

# 24. Practice Roadmap and Revision Checklist

## Phase 1 --- Foundation

-   [ ] HTML purpose and browser rendering
-   [ ] Document structure, doctype, `html`, `head`, `body`
-   [ ] Tags, elements, attributes, nesting, void elements
-   [ ] Headings, paragraphs, `br`, `hr`
-   [ ] Text formatting and semantic text elements
-   [ ] Comments
-   [ ] Links, absolute/relative URLs, page anchors
-   [ ] Images and `alt`
-   [ ] Ordered, unordered, and description lists
-   [ ] `div` and `span`

**Practice:** Build a personal bio page with a heading, paragraphs,
image, links, and lists.

## Phase 2 --- Intermediate

-   [ ] Tables: `caption`, `thead`, `tbody`, `tfoot`, `tr`, `th`, `td`
-   [ ] `colspan`, `rowspan`, `scope`
-   [ ] Forms: `form`, `label`, `input`, `textarea`, `select`, `option`
-   [ ] Input types and form attributes
-   [ ] Radio buttons, checkboxes, fieldset, legend
-   [ ] Buttons and button types
-   [ ] Native form validation
-   [ ] Audio, video, track, iframe
-   [ ] Meta tags and HTML entities

**Practice:** Build a student registration form and a table with at
least three columns and five data rows.

## Phase 3 --- Semantic HTML, SEO, and accessibility

-   [ ] `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`
-   [ ] `figure`, `figcaption`, `address`, `time`
-   [ ] `article` vs `section` vs `div`
-   [ ] Heading hierarchy
-   [ ] Image alternatives and form labels
-   [ ] Keyboard accessibility
-   [ ] ARIA basics
-   [ ] `data-*` attributes
-   [ ] Title, description, canonical, favicon, social metadata

**Practice:** Convert a div-only page into semantic HTML and create a
blog article layout.

## Phase 4 --- Advanced and professional HTML

-   [ ] `contenteditable`
-   [ ] `details` and `summary`
-   [ ] `progress` and `meter`
-   [ ] `template`
-   [ ] `noscript` and `dialog`
-   [ ] Lazy loading and responsive images (`picture`, `srcset`,
    `sizes`)
-   [ ] Browser storage concepts (`localStorage`, `sessionStorage`)
-   [ ] Script loading (`defer`, `async`, modules)
-   [ ] Performance and Core Web Vitals
-   [ ] Validation and DevTools

**Final project:** Build an HTML-only multi-section blog or landing page
with semantic layout, at least two articles, navigation, images with
appropriate loading behavior, one responsive image, an accessible
validated form, media or embedded content, and a footer.

------------------------------------------------------------------------

# 25. Quick Interview Questions

1.  **What is HTML?** A markup language used to structure web content.
2.  **HTML vs CSS vs JavaScript?** Structure vs presentation vs
    behavior.
3.  **Tag vs element?** A tag is markup syntax; an element is the
    complete structure represented by its tags and content.
4.  **What does doctype do?** Requests standards mode in modern
    browsers.
5.  **What is a void element?** An element that cannot have child
    content or an end tag, such as `img` or `input`.
6.  **What is semantic HTML?** Using elements whose names communicate
    the meaning and role of content.
7.  **`div` vs `span`?** Generic flow container vs generic inline
    phrasing container.
8.  **`strong` vs `b`?** Semantic importance vs attention without added
    importance.
9.  **`em` vs `i`?** Stress emphasis vs alternate voice/term.
10. **`id` vs `class`?** An ID identifies one element in a document;
    classes are reusable.
11. **GET vs POST?** GET puts form data in the URL; POST sends it in the
    request body.
12. **`readonly` vs `disabled`?** Read-only values are submitted;
    disabled controls are not.
13. **Radio vs checkbox?** Radio groups select one; checkboxes allow
    independent multiple selections.
14. **Why use `alt`?** Provides a text alternative for meaningful
    images.
15. **What is `iframe`?** An embedded browsing context.
16. **`article` vs `section`?** Standalone content vs thematic grouping.
17. **What is ARIA?** Attributes that expose accessible names, roles,
    states, and relationships when native HTML is insufficient.
18. **What is lazy loading?** Deferring resource loading until it is
    closer to being needed.
19. **`localStorage` vs `sessionStorage`?** Persistent same-origin
    storage vs storage scoped to a browsing session.
20. **Does HTML validation guarantee an accessible page?** No;
    validation checks markup conformance, not the full user experience.

------------------------------------------------------------------------

## Final note

"Complete HTML" is an evolving and very large standard. These notes
cover the core modern HTML topics expected for frontend development,
practical projects, and interviews. For edge cases and newly added
platform features, consult the WHATWG HTML Standard and MDN.

---

## License and Usage

You may use these notes for personal learning, revision, and reference. If you reuse or modify this material in a public repository, retain attribution where applicable and verify examples against current browser behavior and the official HTML documentation.

**Recommended references:**
- [MDN HTML documentation](https://developer.mozilla.org/docs/Web/HTML)
- [WHATWG HTML Standard](https://html.spec.whatwg.org/)
- [W3C Nu HTML Checker](https://validator.w3.org/nu/)


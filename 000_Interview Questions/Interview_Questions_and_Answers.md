# HTML Interview Questions & Answers

### Detailed explanations, practical examples, and interview-ready answers

**Level:** Beginner to Advanced\
**Focus:** HTML fundamentals, modern HTML, accessibility, Web
Components, and Core Web Vitals\
**Last reviewed:** November 2026

------------------------------------------------------------------------

## Table of Contents

1.  [What is the difference between HTML and
    HTML5?](#1-what-is-the-difference-between-html-and-html5)
2.  [What are semantic HTML tags and why are they
    important?](#2-what-are-semantic-html-tags-and-why-are-they-important)
3.  [Difference between block, inline, and inline-block
    elements](#3-difference-between-block-inline-and-inline-block-elements)
4.  [What is an iframe?](#4-what-is-an-iframe)
5.  [What are data attributes?](#5-what-are-data-attributes)
6.  [What is accessibility in HTML? Explain
    aria-\*](#6-what-is-accessibility-in-html-explain-aria-)
7.  [What is the use of
    contenteditable?](#7-what-is-the-use-of-contenteditable)
8.  [What does the picture tag do?](#8-what-does-the-picture-tag-do)
9.  [Explain Web Components in
    detail](#9-explain-web-components-in-detail)
10. [What are Core Web Vitals? Explain in
    depth](#10-what-are-core-web-vitals-explain-in-depth)
11. [Why is HTML so important?](#11-why-is-html-so-important)
12. [Quick interview revision](#12-quick-interview-revision)
13. [Official references](#13-official-references)

------------------------------------------------------------------------

# 1. What is the difference between HTML and HTML5?

## HTML

**HTML (HyperText Markup Language)** is the standard markup language
used to define the structure and meaning of content on web pages.

It describes elements such as headings, paragraphs, links, images,
forms, tables, and media.

## HTML5

**HTML5** was the name commonly used for the major evolution of HTML
that introduced a range of modern capabilities, including semantic
elements, native audio and video, improved forms, and APIs.

An important modern distinction: HTML is now maintained as a
continuously evolving **HTML Living Standard** rather than as a
completely separate, frozen "HTML5 language." Developers still commonly
say "HTML5" when referring to modern HTML features.

## Main differences

  -----------------------------------------------------------------------
  Area                    Earlier HTML (for       HTML5-era / modern HTML
                          example, HTML 4.01)     
  ----------------------- ----------------------- -----------------------
  Doctype                 Long, version-specific  Simple
                          declarations were       `<!doctype html>`
                          common                  

  Page structure          Layouts often used      Semantic elements such
                          generic `div` elements  as `header`, `nav`,
                                                  `main`, `article`, and
                                                  `footer`

  Audio/video             Often depended on       Native `audio` and
                          browser plugins         `video` elements

  Graphics                Commonly relied on      Native `canvas` and SVG
                          images or plugins       support

  Forms                   More limited built-in   Types such as `email`,
                          input types and         `date`, `number`, and
                          validation              native constraints such
                                                  as `required`

  Browser APIs            Fewer standardized      Modern APIs developed
                          built-in capabilities   alongside the HTML
                                                  platform

  Mobile support          Less consistent native  Better foundations for
                          support for modern      responsive,
                          mobile use cases        mobile-friendly
                                                  experiences
  -----------------------------------------------------------------------

## Example: basic modern HTML document

``` html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Modern HTML Page</title>
</head>
<body>
  <header>
    <h1>Welcome</h1>
  </header>

  <main>
    <p>This page uses modern HTML structure.</p>

    <video controls width="500">
      <source src="demo.mp4" type="video/mp4">
      Your browser does not support HTML video.
    </video>
  </main>
</body>
</html>
```

## Important points

-   `<!doctype html>` tells the browser to use standards mode. It does
    not itself create an HTML element.
-   Semantic HTML gives content meaningful structure.
-   Native media elements reduce the need for third-party plugins.
-   Modern form controls provide useful browser-level behavior and
    validation.
-   HTML does not replace CSS or JavaScript.

### Interview-ready answer

HTML is the markup language used to structure web content. HTML5 was the
name commonly given to a major evolution of HTML that introduced
semantic elements, native audio and video, improved forms, and other
modern browser capabilities. Today, HTML is maintained as a Living
Standard, so HTML5 is often used informally to mean modern HTML rather
than a separate language.

------------------------------------------------------------------------

# 2. What are semantic HTML tags and why are they important?

## Definition

**Semantic HTML** means choosing HTML elements that describe the meaning
and purpose of the content they contain.

A semantic element communicates what a section represents instead of
merely acting as a generic container.

## Non-semantic vs semantic HTML

### Non-semantic example

``` html
<div class="header">
  <h1>My Website</h1>
</div>

<div class="navigation">
  <a href="/">Home</a>
  <a href="/about">About</a>
</div>

<div class="content">
  <h2>About Us</h2>
  <p>We build web applications.</p>
</div>

<div class="footer">
  <p>Copyright 2026</p>
</div>
```

The browser sees generic `div` containers. Their class names do not give
those containers native HTML semantics.

### Semantic example

``` html
<header>
  <h1>My Website</h1>
</header>

<nav aria-label="Main navigation">
  <a href="/">Home</a>
  <a href="/about">About</a>
</nav>

<main>
  <section>
    <h2>About Us</h2>
    <p>We build web applications.</p>
  </section>
</main>

<footer>
  <p>&copy; 2026</p>
</footer>
```

## Important semantic elements

  -----------------------------------------------------------------------
  Element                 Purpose                 Typical example
  ----------------------- ----------------------- -----------------------
  `<header>`              Introductory content    Logo and page heading
                          for a page or section   

  `<nav>`                 Major navigation links  Main menu

  `<main>`                Dominant content of the Main article or
                          page                    application content

  `<section>`             Thematic grouping of    Services section
                          content                 

  `<article>`             Independent,            Blog post or news story
                          self-contained content  

  `<aside>`               Related or tangential   Sidebar
                          content                 

  `<footer>`              Footer for a page or    Copyright and related
                          section                 links

  `<figure>`              Self-contained          Image or chart
                          illustrative content    

  `<figcaption>`          Caption for a figure    Chart description

  `<address>`             Contact information for Author contact details
                          a person or             
                          organization            
  -----------------------------------------------------------------------

## Why is semantic HTML important?

### 1. Accessibility

Assistive technologies, including screen readers, can use semantic
landmarks and element roles to help users understand and navigate a
page.

For example, a screen-reader user can navigate to the main content or
navigation landmark.

### 2. SEO and content understanding

Search engines can use document structure and meaningful markup as
signals to understand page content. Semantic HTML supports clear
structure, but it does **not** guarantee a higher ranking.

### 3. Readability and maintainability

Compare:

``` html
<div class="header"></div>
<div class="main-content"></div>
<div class="footer"></div>
```

with:

``` html
<header></header>
<main></main>
<footer></footer>
```

The second version communicates its purpose directly.

### 4. Consistency

Native semantic elements have built-in browser and accessibility
behavior. This reduces the need to recreate common roles manually.

## `article` vs `section` vs `div`

  -----------------------------------------------------------------------
  Element                             When to use it
  ----------------------------------- -----------------------------------
  `article`                           When the content can stand alone or
                                      be reused independently

  `section`                           When grouping related content into
                                      a thematic section, generally with
                                      a heading

  `div`                               When a generic container is needed
                                      and no semantic element fits
  -----------------------------------------------------------------------

### Interview-ready answer

Semantic HTML means using elements according to their meaning, such as
`header`, `nav`, `main`, `article`, `section`, and `footer`. It improves
document structure, accessibility, maintainability, and helps search
engines understand the content. I prefer semantic elements over generic
`div` elements whenever their meaning matches the content.

------------------------------------------------------------------------

# 3. Difference between block, inline, and inline-block elements

These terms describe **CSS display behavior**, not immutable categories
of HTML tags. CSS can change an element's display behavior using the
`display` property.

## 3.1 Block elements

A block-level box in normal flow:

-   Starts on a new line.
-   Normally takes the available width of its containing block when its
    width is `auto`.
-   Respects `width` and `height`.
-   Supports margins and padding on all sides.

Common elements whose default outer display behavior is block include:

-   `div`
-   `p`
-   `h1` to `h6`
-   `section`
-   `article`
-   `header`
-   `footer`
-   `ul`
-   `ol`
-   `li`

Example:

``` html
<div class="box">First block</div>
<div class="box">Second block</div>
```

``` css
.box {
  background: lightblue;
  border: 1px solid navy;
  margin: 8px 0;
  padding: 12px;
}
```

The two `div` elements appear on separate lines by default.

## 3.2 Inline elements

An inline-level box:

-   Does not start a new line by itself.
-   Flows alongside text and other inline content.
-   Can wrap across lines.
-   Does not behave like a block for `width` and `height`; those
    properties generally do not apply to a non-replaced inline box.
-   Horizontal margins and padding affect surrounding content. Vertical
    padding and borders can paint outside the line box without pushing
    adjacent lines apart in the same way as block boxes.

Common inline elements include:

-   `span`
-   `a`
-   `strong`
-   `em`
-   `label`
-   `code`

Example:

``` html
<p>
  Learn <strong>HTML</strong>,
  <em>CSS</em>, and
  <span class="highlight">JavaScript</span>.
</p>
```

``` css
.highlight {
  color: red;
  background: yellow;
}
```

The inline elements remain within the paragraph's text flow.

## 3.3 Inline-block elements

An `inline-block` box:

-   Flows alongside surrounding inline content.
-   Does not force a new line before or after itself.
-   Respects `width` and `height`.
-   Supports padding, borders, and margins on all sides.
-   Behaves as a single inline-level item in the surrounding line.

Example:

``` html
<span class="badge">HTML</span>
<span class="badge">CSS</span>
<span class="badge">JavaScript</span>
```

``` css
.badge {
  display: inline-block;
  width: 110px;
  padding: 12px;
  margin: 5px;
  background: lightgreen;
  text-align: center;
}
```

The badges can sit next to one another while retaining explicit
dimensions.

## Comparison table

  ----------------------------------------------------------------------------------
  Feature           `display: block`   `display: inline`   `display: inline-block`
  ----------------- ------------------ ------------------- -------------------------
  Starts on a new   Yes, in normal     No                  No
  line              flow                                   

  Sits beside other Not by default     Yes                 Yes
  inline-level                                             
  content                                                  

  `width` and       Respected          Generally not       Respected
  `height`                             respected for       
                                       non-replaced inline 
                                       boxes               

  Horizontal margin Yes                Yes                 Yes

  Vertical margin   Yes                Does not work like  Yes
                                       block vertical      
                                       margin              

  Padding           All sides affect   Vertical padding    All sides affect box
                    box layout         does not push line  layout
                                       boxes apart like    
                                       block padding       

  Typical use       Sections and       Text-level content  Badges, compact controls,
                    containers                             sized inline items
  ----------------------------------------------------------------------------------

## One element can have different display values

``` html
<span class="as-block">I behave like a block.</span>
<div class="as-inline">I behave like inline content.</div>
<div class="as-inline-block">I behave like inline-block.</div>
```

``` css
.as-block {
  display: block;
}

.as-inline {
  display: inline;
}

.as-inline-block {
  display: inline-block;
  width: 150px;
  padding: 10px;
}
```

### Interview-ready answer

Block elements start on a new line and normally occupy the available
width. Inline elements remain in the text flow and generally do not
accept explicit width and height. Inline-block elements remain in the
same line like inline elements but accept width, height, and box-model
spacing like block boxes.

------------------------------------------------------------------------

# 4. What is an iframe?

## Definition

An **iframe (inline frame)** is an HTML element used to embed another
HTML document inside the current page.

It creates a separate nested browsing context.

Common use cases:

-   Embedding maps.
-   Embedding YouTube videos.
-   Displaying external documents or tools.
-   Integrating third-party widgets.

## Basic syntax

``` html
<iframe
  src="https://example.com"
  title="Example website"
  width="600"
  height="400">
</iframe>
```

### Important attributes

  -----------------------------------------------------------------------
  Attribute                           Purpose
  ----------------------------------- -----------------------------------
  `src`                               URL of the document to embed

  `title`                             Accessible description of the
                                      embedded content

  `width`                             Frame width

  `height`                            Frame height

  `loading`                           Loading hint, such as `lazy` or
                                      `eager`

  `allow`                             Permissions policy features
                                      available to the frame

  `allowfullscreen`                   Allows fullscreen presentation
                                      where supported

  `sandbox`                           Applies restrictions to the
                                      embedded content

  `srcdoc`                            Supplies HTML directly for the
                                      embedded document

  `referrerpolicy`                    Controls the referrer information
                                      sent when loading the frame
  -----------------------------------------------------------------------

## Example: YouTube embed

``` html
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  title="HTML tutorial video"
  loading="lazy"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  allowfullscreen>
</iframe>
```

Replace `VIDEO_ID` with the actual video ID and use the provider's
official embed URL.

## Example: responsive iframe

``` html
<div class="video-container">
  <iframe
    src="https://www.youtube.com/embed/VIDEO_ID"
    title="HTML tutorial"
    loading="lazy"
    allowfullscreen>
  </iframe>
</div>
```

``` css
.video-container {
  aspect-ratio: 16 / 9;
  width: 100%;
}

.video-container iframe {
  width: 100%;
  height: 100%;
  border: 0;
}
```

## Security considerations

1.  Give every meaningful iframe a descriptive `title`.
2.  Use `sandbox` when embedding content that should have restricted
    capabilities.
3.  Grant only the permissions required through `allow`.
4.  Embed content only from sources you trust.
5.  Do not assume the same-origin policy allows the parent page to read
    an iframe's internal DOM. Cross-origin documents are isolated by
    browser security rules.
6.  Some websites send headers such as `X-Frame-Options` or CSP
    `frame-ancestors` that prevent embedding.

### What does `sandbox` do?

It applies restrictions to the embedded document. Permissions can be
selectively restored using tokens such as `allow-scripts` or
`allow-forms`.

``` html
<iframe
  src="https://example.com"
  title="Restricted embedded page"
  sandbox>
</iframe>
```

Do not casually combine `allow-scripts` and `allow-same-origin` for
untrusted same-origin content; understand the security implications
before relaxing sandbox restrictions.

### Interview-ready answer

An iframe is an HTML element that embeds another document inside the
current page. It is commonly used for maps, videos, and third-party
widgets. Important attributes include `src`, `title`, `width`, `height`,
`loading`, `allow`, and `sandbox`. For accessibility, I provide a
meaningful title, and for security I restrict embedded content where
appropriate.

------------------------------------------------------------------------

# 5. What are data attributes?

## Definition

**Custom data attributes** are HTML attributes that begin with `data-`.
They allow developers to store custom, non-visible data on HTML
elements.

They are commonly used to connect HTML elements with JavaScript
behavior.

## Example

``` html
<button
  id="buy-button"
  data-product-id="101"
  data-product-name="Laptop"
  data-price="65000">
  Buy Now
</button>
```

The data is not displayed automatically. JavaScript can read it through
the element's `dataset` property.

``` html
<script>
  const button = document.querySelector("#buy-button");

  console.log(button.dataset.productId);   // "101"
  console.log(button.dataset.productName); // "Laptop"
  console.log(button.dataset.price);       // "65000"
</script>
```

## How does `dataset` convert attribute names?

  HTML attribute        JavaScript property
  --------------------- -----------------------
  `data-user-id`        `dataset.userId`
  `data-product-name`   `dataset.productName`
  `data-status`         `dataset.status`
  `data-is-active`      `dataset.isActive`

Hyphenated names are converted to camelCase.

## Read, update, and remove data

``` html
<div id="user" data-user-id="25" data-role="developer"></div>

<script>
  const user = document.querySelector("#user");

  // Read
  console.log(user.dataset.userId);

  // Update
  user.dataset.role = "admin";

  // Add
  user.dataset.status = "active";

  // Remove
  delete user.dataset.role;
</script>
```

Dataset values are strings. Convert them when a numeric or Boolean value
is needed:

``` js
const price = Number(button.dataset.price);
const isActive = button.dataset.active === "true";
```

## Use cases

-   Store product IDs.
-   Identify elements for event handling.
-   Pass small configuration values to JavaScript.
-   Mark UI state or component options.
-   Avoid adding non-standard custom attributes.

## Important security note

Data attributes are visible to users through browser developer tools and
can be modified. Never store passwords, API secrets, authorization
decisions, or other sensitive information in them. Always validate data
on the server when it affects a trusted operation.

### Interview-ready answer

Data attributes are custom HTML attributes that start with `data-`. They
store additional information on an element without displaying it.
JavaScript accesses them through `element.dataset`. For example,
`data-user-id="25"` can be read using `element.dataset.userId`. Their
values are strings and should never be treated as trusted or secret
data.

------------------------------------------------------------------------

# 6. What is accessibility in HTML? Explain aria-\*

## Definition

**Web accessibility (often abbreviated A11Y)** means designing websites
and applications so that people with different abilities can perceive,
understand, navigate, and interact with them.

This includes people who use:

-   Screen readers.
-   Keyboard-only navigation.
-   Screen magnification.
-   Voice control.
-   Switch devices or other assistive technologies.

Accessibility is not a separate HTML feature. It is a quality of the
whole user experience, supported by semantic HTML, CSS, JavaScript, and
good interaction design.

## Why is accessibility important?

1.  It makes websites usable by more people.
2.  It improves navigation and interaction for assistive-technology
    users.
3.  It encourages clear structure and meaningful controls.
4.  It helps users in different situations, including temporary injuries
    or difficult environments.
5.  It supports compliance with applicable accessibility standards and
    laws.

## Essential HTML accessibility practices

### 1. Use semantic HTML

Prefer:

``` html
<button type="button">Save</button>
```

Instead of:

``` html
<div onclick="saveData()">Save</div>
```

A native button already supports keyboard interaction, focus, and button
semantics. A clickable `div` does not automatically provide those
behaviors.

### 2. Provide image alternatives

``` html
<img src="team.jpg" alt="Three developers working at a desk">
```

For decorative images:

``` html
<img src="decorative-shape.svg" alt="">
```

### 3. Associate labels with form controls

``` html
<label for="email">Email address</label>
<input type="email" id="email" name="email">
```

### 4. Use a logical heading hierarchy

``` html
<h1>Web Development</h1>
<h2>HTML</h2>
<h3>Forms</h3>
<h2>CSS</h2>
```

### 5. Support keyboard navigation

Users should be able to reach and operate interactive controls using a
keyboard. Keep a visible focus indicator.

------------------------------------------------------------------------

## What is ARIA?

**ARIA** stands for **Accessible Rich Internet Applications**. It is a
set of attributes that adds accessibility information to HTML,
particularly for dynamic interfaces and custom widgets.

ARIA can communicate:

-   Accessible names.
-   Descriptions.
-   Roles.
-   States.
-   Relationships.
-   Live updates.

ARIA does not automatically add functionality, keyboard behavior, or
focus management.

## What does `aria-*` mean?

ARIA attributes are attributes whose names begin with `aria-`.

### Common ARIA attributes

  ----------------------------------------------------------------------------------
  Attribute               Purpose                 Example
  ----------------------- ----------------------- ----------------------------------
  `aria-label`            Gives an element an     `aria-label="Close"`
                          accessible name         

  `aria-labelledby`       Uses another element's  `aria-labelledby="dialog-title"`
                          text as the accessible  
                          name                    

  `aria-describedby`      Points to descriptive   `aria-describedby="help-text"`
                          text                    

  `aria-hidden`           Hides content from the  `aria-hidden="true"`
                          accessibility tree      

  `aria-expanded`         Reports whether a       `aria-expanded="false"`
                          disclosure control is   
                          expanded                

  `aria-controls`         Identifies the element  `aria-controls="menu"`
                          controlled by a control 

  `aria-live`             Announces dynamic       `aria-live="polite"`
                          updates to assistive    
                          technology              

  `aria-pressed`          Reports the pressed     `aria-pressed="true"`
                          state of a toggle       
                          button                  

  `aria-current`          Identifies the current  `aria-current="page"`
                          item in a related set   

  `aria-required`         Communicates required   `aria-required="true"`
                          state in certain custom 
                          widgets                 
  ----------------------------------------------------------------------------------

## Example 1: aria-label

A button that contains only an X symbol:

``` html
<button type="button" aria-label="Close dialog">
  ×
</button>
```

A screen reader can announce the accessible name "Close dialog" instead
of relying on the symbol.

If a visible text label already provides the correct accessible name, an
additional `aria-label` may not be necessary.

## Example 2: aria-labelledby

``` html
<h2 id="profile-heading">User Profile</h2>

<section aria-labelledby="profile-heading">
  <p>Name: Riyaz</p>
  <p>Role: Developer</p>
</section>
```

The section gets its accessible name from the heading.

## Example 3: aria-describedby

``` html
<label for="password">Password</label>

<input
  type="password"
  id="password"
  aria-describedby="password-help">

<p id="password-help">
  Use at least 8 characters.
</p>
```

The help text is programmatically associated with the input.

## Example 4: aria-expanded and aria-controls

``` html
<button
  type="button"
  aria-expanded="false"
  aria-controls="account-menu">
  Account menu
</button>

<ul id="account-menu" hidden>
  <li><a href="/profile">Profile</a></li>
  <li><a href="/settings">Settings</a></li>
</ul>
```

When JavaScript opens the menu, it must also update the state:

``` js
const button = document.querySelector("button[aria-controls]");
const menu = document.querySelector("#account-menu");

button.addEventListener("click", () => {
  const isExpanded = button.getAttribute("aria-expanded") === "true";

  button.setAttribute("aria-expanded", String(!isExpanded));
  menu.hidden = isExpanded;
});
```

ARIA state must match the actual UI state. This simple example
demonstrates state synchronization; a production menu also needs an
appropriate keyboard interaction model.

## Example 5: aria-live

Useful when content changes dynamically:

``` html
<p id="status" aria-live="polite"></p>

<script>
  document.querySelector("#status").textContent = "Profile saved successfully.";
</script>
```

The update can be announced by assistive technology without requiring
the user to move focus to the message.

## What is `role`?

The `role` attribute describes the semantic role of an element.

``` html
<div role="status">Your changes have been saved.</div>
```

However, use native HTML semantics whenever possible:

``` html
<button type="button">Save</button>
```

This is generally better than:

``` html
<div role="button" tabindex="0">Save</div>
```

The `div` version would still need JavaScript for keyboard activation
and other button behavior.

## Important ARIA rules

1.  **First rule of ARIA:** If a native HTML element already provides
    the semantics and behavior you need, use it.
2.  Do not add ARIA attributes without understanding their effect.
3.  Do not use `aria-hidden="true"` on a focusable element or an
    ancestor of a currently focused element.
4.  Keep ARIA states synchronized with the visible interface.
5.  ARIA does not replace keyboard support.
6.  Test with keyboard navigation and assistive technologies.

### Interview-ready answer

Accessibility means making websites usable by people with different
abilities and assistive technologies. HTML supports accessibility
through semantic elements, labels, alternative text, headings, and
keyboard-operable native controls. ARIA stands for Accessible Rich
Internet Applications. Its `aria-*` attributes provide accessible names,
descriptions, roles, states, and relationships when native HTML alone is
insufficient. I prefer semantic HTML first because ARIA does not
automatically provide behavior.

------------------------------------------------------------------------

# 7. What is the use of contenteditable?

## Definition

The `contenteditable` global HTML attribute makes the content of an
element editable by the user.

It is useful for simple inline editing, notes, and lightweight
content-editing interfaces.

## Basic example

``` html
<p contenteditable="true">
  You can edit this text directly in the browser.
</p>
```

The user can click the paragraph and modify its text.

## Values

  -----------------------------------------------------------------------
  Value                               Meaning
  ----------------------------------- -----------------------------------
  `true`                              Enables editing

  `false`                             Disables editing for the element

  `plaintext-only`                    Enables editing as plain text,
                                      without rich-text formatting where
                                      supported
  -----------------------------------------------------------------------

The attribute is enumerated, not a normal Boolean attribute. Use
explicit values such as `contenteditable="true"` and
`contenteditable="false"`.

## Example: editable profile

``` html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Editable Profile</title>
</head>
<body>
  <h1>My Profile</h1>

  <div contenteditable="true">
    <h2>Riyaz</h2>
    <p>I am a web developer.</p>
  </div>
</body>
</html>
```

The user can edit the heading and paragraph directly in the browser.

## Example: save edited text with JavaScript

``` html
<div id="editor" contenteditable="true">
  Write your notes here...
</div>

<button id="save-button" type="button">Save</button>

<script>
  const editor = document.querySelector("#editor");
  const saveButton = document.querySelector("#save-button");

  saveButton.addEventListener("click", () => {
    const content = editor.innerHTML;
    localStorage.setItem("my-notes", content);
    alert("Notes saved in this browser.");
  });

  const savedContent = localStorage.getItem("my-notes");

  if (savedContent !== null) {
    editor.innerHTML = savedContent;
  }
</script>
```

**Security warning:** This example is for demonstrating the API, not a
safe production editor. Assigning untrusted content to `innerHTML` can
create cross-site scripting (XSS) vulnerabilities. Sanitize HTML with a
suitable sanitizer or store and restore plain text using `textContent`
when rich formatting is not required. Server-side validation is also
important.

## Use cases

-   Inline profile editing.
-   Simple note-taking interfaces.
-   Lightweight content management tools.
-   Editable descriptions or labels.
-   Rich-text editor prototypes.

## Limitations

-   It does not automatically save content.
-   It does not provide a complete rich-text editor.
-   It does not handle collaboration or version history.
-   It does not provide application-level validation.
-   Pasted content and generated markup need careful handling.
-   Keyboard and screen-reader behavior should be tested.

### Interview-ready answer

The `contenteditable` attribute makes an HTML element editable directly
in the browser. For example, `<p contenteditable="true">Edit me</p>`
lets the user modify the paragraph. It is useful for inline editing and
simple notes, but saving, validation, sanitization, and advanced editing
features must be implemented separately.

------------------------------------------------------------------------

# 8. What does the picture tag do?

## Definition

The `<picture>` element provides multiple image sources so that the
browser can select an appropriate image based on conditions such as:

-   Screen or viewport size.
-   Image format support.
-   Art direction (different image crops or compositions).

It is especially useful for responsive images and image-format
fallbacks.

## Basic syntax

``` html
<picture>
  <source media="(max-width: 600px)" srcset="mobile.jpg">
  <source media="(min-width: 601px)" srcset="desktop.jpg">
  <img src="desktop.jpg" alt="A mountain landscape">
</picture>
```

The browser evaluates the `<source>` elements in order and uses a
matching supported source. The `<img>` element is required and provides
the fallback image and alternative text.

## Example 1: different images for mobile and desktop

``` html
<picture>
  <source
    media="(max-width: 600px)"
    srcset="images/banner-mobile.jpg">

  <source
    media="(min-width: 601px)"
    srcset="images/banner-desktop.jpg">

  <img
    src="images/banner-desktop.jpg"
    alt="A team working together"
    width="1200"
    height="600">
</picture>
```

Here:

-   On smaller viewports, the browser can select the mobile image.
-   On larger viewports, it can select the desktop image.
-   If no source matches, the browser uses the `img` fallback.

## Example 2: modern image formats with fallback

``` html
<picture>
  <source
    type="image/avif"
    srcset="images/photo.avif">

  <source
    type="image/webp"
    srcset="images/photo.webp">

  <img
    src="images/photo.jpg"
    alt="A lake surrounded by mountains"
    width="1200"
    height="800">
</picture>
```

The browser selects a supported source format, falling back to the JPEG
`img` source when necessary.

## What is the difference between picture and img?

  -----------------------------------------------------------------------
  `<img>`                             `<picture>`
  ----------------------------------- -----------------------------------
  Displays an image resource          Provides alternative image sources

  Uses `src` and can also use         Uses one or more `source` elements
  `srcset` and `sizes`                plus a required `img`

  Suitable for ordinary images        Useful for art direction and format
                                      selection

  Provides the image's `alt` text     The nested `img` provides the `alt`
                                      text
  -----------------------------------------------------------------------

## What are `srcset` and `sizes`?

Use `srcset` and `sizes` on `img` when the image is essentially the same
but available at different resolutions or widths.

``` html
<img
  src="photo-800.jpg"
  srcset="
    photo-400.jpg 400w,
    photo-800.jpg 800w,
    photo-1200.jpg 1200w"
  sizes="(max-width: 600px) 100vw, 50vw"
  alt="A mountain lake"
  width="1200"
  height="800">
```

-   `srcset` lists available image candidates.
-   `sizes` describes the expected rendered slot width at different
    viewport conditions.
-   The browser uses these hints and device characteristics to choose a
    candidate.

### When should you use picture?

Use `<picture>` when you need different crops for different layouts or
want to offer format alternatives. Use `srcset` and `sizes` when you
need resolution selection for the same image composition.

### Interview-ready answer

The `<picture>` element allows the browser to choose between multiple
image sources based on media conditions or supported formats. It is
useful for responsive images, art direction, and modern image formats
such as AVIF and WebP. It contains `source` elements and a required
`img` fallback, where the alternative text is defined.

------------------------------------------------------------------------

# 9. Explain Web Components in detail

## 9.1 What are Web Components?

**Web Components** are a set of browser technologies that allow
developers to create reusable custom HTML elements with encapsulated
structure, styling, and behavior.

For example, instead of repeatedly writing the same profile-card markup,
we can define a custom element:

``` html
<user-card name="Riyaz" role="Frontend Developer"></user-card>
```

The browser can render this element using the behavior defined by the
developer.

Web Components are based on three main technologies:

1.  **Custom Elements**
2.  **Shadow DOM**
3.  **HTML Templates and Slots**

They can be used with plain JavaScript and can also coexist with
frameworks such as React, Angular, and Vue.

------------------------------------------------------------------------

## 9.2 Custom Elements

Custom Elements allow developers to define their own HTML tags and
behavior.

A custom element name must contain a hyphen, such as:

-   `user-card`
-   `product-card`
-   `app-header`
-   `rating-stars`

### Example: create a custom element

``` html
<user-card></user-card>

<script>
  class UserCard extends HTMLElement {
    connectedCallback() {
      this.innerHTML = `
        <div>
          <h2>Riyaz</h2>
          <p>Frontend Developer</p>
        </div>
      `;
    }
  }

  customElements.define("user-card", UserCard);
</script>
```

### Explanation

**Step 1: Create a class**

``` js
class UserCard extends HTMLElement {
}
```

The class extends `HTMLElement`, which gives it the standard element
APIs.

**Step 2: Implement behavior**

``` js
connectedCallback() {
  this.innerHTML = "<h2>Riyaz</h2>";
}
```

`connectedCallback()` runs when the element is connected to the
document.

**Step 3: Register the element**

``` js
customElements.define("user-card", UserCard);
```

The browser now recognizes `<user-card>`.

**Step 4: Use it in HTML**

``` html
<user-card></user-card>
```

------------------------------------------------------------------------

## 9.3 Custom Element lifecycle callbacks

Custom Elements provide lifecycle callbacks so the component can respond
to changes in its position or attributes.

  -----------------------------------------------------------------------
  Callback                            When it runs
  ----------------------------------- -----------------------------------
  `constructor()`                     When an instance is created;
                                      initialize internal state here

  `connectedCallback()`               When the element is connected to
                                      the document

  `disconnectedCallback()`            When the element is disconnected
                                      from the document

  `attributeChangedCallback()`        When an observed attribute is
                                      added, changed, or removed

  `adoptedCallback()`                 When the element is adopted into a
                                      different document
  -----------------------------------------------------------------------

A modern platform also defines `connectedMoveCallback()` for
state-preserving moves performed with `Element.moveBefore()` where
supported.

### Example: observe an attribute

``` html
<user-badge name="Riyaz"></user-badge>

<script>
  class UserBadge extends HTMLElement {
    static observedAttributes = ["name"];

    connectedCallback() {
      this.render();
    }

    attributeChangedCallback(name, oldValue, newValue) {
      if (oldValue !== newValue) {
        this.render();
      }
    }

    render() {
      const name = this.getAttribute("name") || "Guest";
      this.textContent = `Hello, ${name}`;
    }
  }

  customElements.define("user-badge", UserBadge);
</script>
```

When the observed `name` attribute changes, `attributeChangedCallback()`
runs and the component updates.

In production components, avoid repeatedly overwriting light-DOM
children if consumers are expected to provide their own markup. Shadow
DOM and slots are often a better fit for encapsulated components.

------------------------------------------------------------------------

## 9.4 Shadow DOM

Shadow DOM provides an encapsulated DOM tree attached to an element.

It helps isolate a component's internal markup and styles from the
surrounding document.

### Why is Shadow DOM useful?

Without style encapsulation, CSS selectors from the page can
unintentionally affect component internals, and component styles can
leak out.

Shadow DOM provides a boundary for much of this styling and DOM
structure.

### Example

``` html
<user-card></user-card>

<script>
  class UserCard extends HTMLElement {
    constructor() {
      super();

      const shadow = this.attachShadow({ mode: "open" });

      shadow.innerHTML = `
        <style>
          .card {
            padding: 16px;
            border: 1px solid #ccc;
            border-radius: 8px;
            background: #f5f5f5;
          }

          h2 {
            color: darkblue;
          }
        </style>

        <div class="card">
          <h2>Riyaz</h2>
          <p>Frontend Developer</p>
        </div>
      `;
    }
  }

  customElements.define("user-card", UserCard);
</script>
```

### `open` vs `closed`

``` js
this.attachShadow({ mode: "open" });
```

-   **Open:** JavaScript can access the shadow root through
    `element.shadowRoot`.
-   **Closed:** `element.shadowRoot` returns `null` from ordinary page
    JavaScript.

Closed mode is not a security boundary. It should not be used to protect
secrets.

### Important distinction

Shadow DOM encapsulates DOM and styling behavior, but it does not make
the component's content inherently secure or inaccessible to the user.
It is an encapsulation mechanism, not an authorization system.

------------------------------------------------------------------------

## 9.5 HTML Templates

The `<template>` element stores HTML that is not rendered when the page
initially loads. JavaScript can clone its contents and insert them
later.

``` html
<template id="card-template">
  <article class="card">
    <h2 class="title"></h2>
    <p class="description"></p>
  </article>
</template>
```

The template's content is inert until it is instantiated.

Example of cloning:

``` js
const template = document.querySelector("#card-template");
const clone = template.content.cloneNode(true);

clone.querySelector(".title").textContent = "HTML";
clone.querySelector(".description").textContent =
  "Learn the structure of web pages.";

document.body.append(clone);
```

------------------------------------------------------------------------

## 9.6 Slots

A `<slot>` is a placeholder inside a component's Shadow DOM. It allows
the component user to provide content that is rendered in the component.

### Example

``` html
<user-card>
  <h2 slot="name">Riyaz</h2>
  <p slot="role">Frontend Developer</p>
</user-card>
```

Component implementation:

``` html
<script>
  class UserCard extends HTMLElement {
    constructor() {
      super();

      const shadow = this.attachShadow({ mode: "open" });

      shadow.innerHTML = `
        <style>
          .card {
            border: 1px solid #ccc;
            padding: 16px;
            border-radius: 8px;
          }
        </style>

        <div class="card">
          <slot name="name"></slot>
          <slot name="role"></slot>
        </div>
      `;
    }
  }

  customElements.define("user-card", UserCard);
</script>
```

The `slot="name"` attribute on the supplied heading matches
`<slot name="name">` inside the shadow tree.

A default slot can be written as:

``` html
<slot></slot>
```

It receives content that does not specify a named slot.

------------------------------------------------------------------------

## 9.7 Complete Web Component example

This example combines Custom Elements, Shadow DOM, attributes, slots,
and component styling.

``` html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Web Component Example</title>
</head>
<body>

  <user-card name="Riyaz" role="Frontend Developer">
    <p slot="description">
      Learning HTML, CSS, JavaScript, and modern web development.
    </p>
  </user-card>

  <script>
    class UserCard extends HTMLElement {
      static observedAttributes = ["name", "role"];

      constructor() {
        super();

        this.attachShadow({ mode: "open" });
      }

      connectedCallback() {
        this.render();
      }

      attributeChangedCallback(name, oldValue, newValue) {
        if (oldValue !== newValue && this.isConnected) {
          this.render();
        }
      }

      render() {
        const name = this.getAttribute("name") || "Guest";
        const role = this.getAttribute("role") || "Member";

        this.shadowRoot.innerHTML = `
          <style>
            .card {
              max-width: 320px;
              padding: 20px;
              border: 1px solid #ddd;
              border-radius: 12px;
              font-family: Arial, sans-serif;
            }

            h2 {
              margin: 0 0 8px;
              color: #174ea6;
            }

            .role {
              color: #555;
            }
          </style>

          <article class="card">
            <h2></h2>
            <p class="role"></p>
            <slot name="description"></slot>
          </article>
        `;

        // Use textContent for attribute values rather than interpolating
        // untrusted values into an HTML string.
        this.shadowRoot.querySelector("h2").textContent = name;
        this.shadowRoot.querySelector(".role").textContent = role;
      }
    }

    customElements.define("user-card", UserCard);
  </script>

</body>
</html>
```

In this example:

-   `<user-card>` is a custom element.
-   `name` and `role` are observed attributes.
-   `connectedCallback()` renders the component.
-   `attributeChangedCallback()` updates it when an observed attribute
    changes.
-   Shadow DOM encapsulates the card's internal structure and styles.
-   `<slot>` displays content supplied by the page.

For a production component, consider preserving existing shadow-root
nodes rather than replacing the entire shadow tree on every update, and
add tests for lifecycle, accessibility, and dynamic updates.

## 9.8 Advantages of Web Components

1.  **Reusability:** use the same component in multiple places.
2.  **Encapsulation:** keep internal DOM and styles separate.
3.  **Native browser technology:** no framework is required.
4.  **Interoperability:** custom elements can be used by many frameworks
    and plain HTML pages.
5.  **Maintainability:** component behavior and structure can be
    organized in one reusable unit.
6.  **Consistency:** shared UI components can provide consistent
    behavior across pages.

## 9.9 Limitations and considerations

-   Developers must design component APIs, events, attributes, and
    accessibility behavior.
-   Shadow DOM styling and theming require deliberate design.
-   Server-side rendering and hydration need additional consideration
    depending on the application.
-   Framework integration details vary.
-   Custom elements should have meaningful accessible names, keyboard
    behavior, and appropriate semantics.
-   Avoid creating custom elements when a native HTML element already
    solves the problem.

## Web Components vs React components

  -----------------------------------------------------------------------
  Web Components                      React components
  ----------------------------------- -----------------------------------
  Browser platform standard           UI library

  Custom Elements, Shadow DOM,        React component model, JSX, props,
  templates/slots                     state

  Can be used without React           Requires React runtime

  Can be consumed by different        Primarily designed for React
  frameworks                          applications

  Native browser integration          Rich ecosystem for application UI
  -----------------------------------------------------------------------

They are not direct replacements for one another. A React application
can use Web Components, and Web Components can be used without React.

### Interview-ready answer

Web Components are browser technologies for creating reusable custom
HTML elements. They consist mainly of Custom Elements, Shadow DOM, and
HTML Templates with Slots. Custom Elements define the component and its
lifecycle, Shadow DOM encapsulates internal DOM and styles, and
templates and slots provide reusable markup and content insertion
points. They allow reusable UI components to work across different
frameworks and plain JavaScript applications.

------------------------------------------------------------------------

# 10. What are Core Web Vitals? Explain in depth

## 10.1 Definition

**Core Web Vitals** are Google's user-experience metrics that measure
three important aspects of a web page:

1.  **Loading performance**
2.  **Interactivity / responsiveness**
3.  **Visual stability**

The current Core Web Vitals are:

-   LCP --- Largest Contentful Paint
-   INP --- Interaction to Next Paint
-   CLS --- Cumulative Layout Shift

They are based on real-user experience, not simply whether the HTML is
valid.

## 10.2 Current recommended thresholds

  Metric              Good        Needs improvement           Poor
  -------- --------------- ------------------------ --------------
  LCP        ≤ 2.5 seconds       \> 2.5 s and ≤ 4 s   \> 4 seconds
  INP             ≤ 200 ms   \> 200 ms and ≤ 500 ms      \> 500 ms
  CLS                ≤ 0.1        \> 0.1 and ≤ 0.25        \> 0.25

For Core Web Vitals assessment, the 75th percentile is used. This means
performance should be good for at least 75% of page visits, considered
separately for mobile and desktop.

------------------------------------------------------------------------

## 10.3 LCP --- Largest Contentful Paint

### What is LCP?

LCP measures how quickly the largest eligible content element visible in
the viewport is rendered.

It is a measure of perceived loading performance: when does the main
content appear to the user?

Potential LCP elements include:

-   A large hero image.
-   A large video poster image.
-   A large block of text.
-   A background image in certain cases.

### Example

Imagine a homepage containing:

-   A small logo.
-   A navigation bar.
-   A large hero image.
-   A heading and paragraph.

If the hero image is the largest eligible visible element, its rendering
may determine the page's LCP.

### LCP target

**Good LCP: 2.5 seconds or less.**

### Common causes of poor LCP

1.  Slow server response.
2.  Large, unoptimized images.
3.  Render-blocking CSS.
4.  JavaScript that delays rendering.
5.  Slow resource discovery.
6.  Poor caching or delivery infrastructure.
7.  A hero image that is loaded too late.

### How to improve LCP

**1. Optimize images**

-   Use suitable formats such as WebP or AVIF where appropriate.
-   Compress images.
-   Serve responsive image sizes with `srcset` and `sizes`.
-   Avoid sending a huge desktop image to a small mobile screen.

**2. Do not lazy-load the LCP image**

An important above-the-fold hero image should generally be discovered
and loaded early.

``` html
<img
  src="hero.webp"
  alt="Product dashboard"
  width="1200"
  height="600"
  fetchpriority="high">
```

Use `fetchpriority="high"` selectively for the likely LCP resource, not
on every image.

**3. Improve server response**

-   Use caching.
-   Reduce backend processing time.
-   Use a CDN where appropriate.
-   Optimize database and API response times.

**4. Reduce render-blocking resources**

-   Remove unused CSS.
-   Minimize unnecessary JavaScript.
-   Load scripts with appropriate `defer`, `async`, or module behavior.
-   Avoid delaying critical content behind unnecessary client-side work.

### How to investigate LCP

Find the actual LCP element in a field or lab report. Determine whether
the delay comes from:

-   Time to first byte (TTFB).
-   Resource load delay.
-   Resource load duration.
-   Element render delay.

This helps identify whether the problem is server delivery, resource
discovery, resource size, or rendering.

------------------------------------------------------------------------

## 10.4 INP --- Interaction to Next Paint

### What is INP?

INP measures the responsiveness of a page to user interactions
throughout a visit.

It considers interactions such as:

-   Clicking a button.
-   Tapping a menu.
-   Typing into an input.
-   Selecting an option.
-   Triggering an interface update.

INP looks at the time from an interaction until the next visual update
is presented.

### INP target

**Good INP: 200 milliseconds or less.**

### Example

Imagine a user clicks a "Save" button.

-   The user clicks the button.
-   JavaScript performs validation and processing.
-   The browser updates the interface to show "Saved".

If the page takes a long time to respond visually, the interaction feels
slow.

### What contributes to INP?

An interaction's latency can be understood in three parts:

1.  **Input delay:** time between the user action and the start of
    event-handler processing.
2.  **Processing duration:** time spent running event callbacks.
3.  **Presentation delay:** time between the completion of event
    handlers and the next frame being presented.

### Common causes of poor INP

1.  Long-running JavaScript tasks.
2.  Too much work inside click or input event handlers.
3.  Large DOM updates.
4.  Expensive style recalculation and layout.
5.  Heavy third-party scripts.
6.  Excessive main-thread work.

### How to improve INP

**1. Break up long tasks**

Avoid running large amounts of synchronous JavaScript in one event
handler. Split non-urgent work into smaller tasks.

**2. Keep event handlers lightweight**

``` js
button.addEventListener("click", () => {
  showLoadingState();

  setTimeout(() => {
    performNonUrgentWork();
  }, 0);
});
```

This is only a simple illustration of yielding work; it is not a
complete scheduling strategy. Real applications may use task scheduling,
workers, or other techniques.

**3. Avoid unnecessary DOM updates**

Update only the elements that need to change.

**4. Reduce JavaScript**

-   Remove unused dependencies.
-   Code-split large application features.
-   Defer non-critical scripts.
-   Avoid excessive hydration and rendering work.

**5. Use Web Workers for suitable heavy computations**

Web Workers can move certain computations away from the main thread.
They cannot directly manipulate the page DOM.

### How to investigate INP

Use interaction performance tools and browser profiling to identify:

-   Which interaction is slow.
-   Whether input delay is high.
-   Which event handlers take too long.
-   Whether layout, rendering, or third-party code is responsible.

------------------------------------------------------------------------

## 10.5 CLS --- Cumulative Layout Shift

### What is CLS?

CLS measures unexpected visual movement of page content.

A layout shift occurs when a visible element changes its position
between rendered frames without a user-expected cause.

### Example

Imagine a user is reading a paragraph. Suddenly, an advertisement loads
above it and pushes the paragraph down.

The content moves unexpectedly. This is a poor experience and can cause
accidental clicks.

### CLS target

**Good CLS: 0.1 or less.**

### Common causes of poor CLS

1.  Images without reserved dimensions.
2.  Advertisements or embeds inserted without reserved space.
3.  Web fonts causing text reflow.
4.  Dynamically injected content above existing content.
5.  Components changing size after initial rendering.
6.  Animations that change layout properties.

### How to improve CLS

**1. Set image dimensions**

``` html
<img
  src="product.jpg"
  alt="Product"
  width="800"
  height="600">
```

The browser can reserve the correct aspect ratio before the image loads.

**2. Reserve space for ads and embeds**

``` css
.ad-container {
  min-height: 250px;
}
```

Use a size appropriate to the actual ad or embed slot.

**3. Avoid inserting content above existing content unexpectedly**

If new content must appear, reserve space or make the change in response
to a clear user action.

**4. Use stable font loading strategies**

Choose suitable fallback fonts and consider font metric overrides where
appropriate.

**5. Prefer transform-based animations**

Animations using `transform` and `opacity` generally avoid layout
changes, unlike animations that change dimensions or positioning in
normal flow.

### How is CLS calculated?

CLS is based on layout-shift scores. A layout-shift score uses:

-   **Impact fraction:** the portion of the viewport affected by the
    shift.
-   **Distance fraction:** how far the affected content moves relative
    to the viewport.

A simplified representation of an individual shift score is:

``` text
Layout shift score = Impact fraction × Distance fraction
```

CLS is calculated using session windows of layout shifts, rather than
simply adding every shift over an unlimited page lifetime. A session
window groups shifts that occur close together, with limits on the gap
and total duration; the largest session-window score is used.

This is why a single unexpected movement can affect CLS even if the page
eventually settles.

------------------------------------------------------------------------

## 10.6 FCP vs LCP

These metrics are related but measure different milestones.

  -----------------------------------------------------------------------
  FCP                                 LCP
  ----------------------------------- -----------------------------------
  First Contentful Paint              Largest Contentful Paint

  Measures when the first text,       Measures when the largest eligible
  image, or other content is rendered visible content is rendered

  Indicates when something first      Better indicates when the main
  appears                             content appears

  Not one of the three Core Web       One of the three Core Web Vitals
  Vitals                              
  -----------------------------------------------------------------------

FCP is useful for diagnosing loading performance, but it is not
currently a Core Web Vital.

## 10.7 TTFB vs FCP vs LCP

  -----------------------------------------------------------------------
  Metric                              Meaning
  ----------------------------------- -----------------------------------
  TTFB                                Time to First Byte: how long it
                                      takes for the browser to receive
                                      the first byte of the response

  FCP                                 First Contentful Paint: when the
                                      first content is rendered

  LCP                                 Largest Contentful Paint: when the
                                      largest eligible visible content is
                                      rendered
  -----------------------------------------------------------------------

These metrics help diagnose different stages of the loading process.

## 10.8 How to measure Core Web Vitals

### 1. Google PageSpeed Insights

Provides lab diagnostics and, when available, field data from the Chrome
UX Report.

### 2. Lighthouse

Runs a controlled lab audit and provides performance diagnostics. A
Lighthouse score is not the same thing as real-user Core Web Vitals.

### 3. Chrome DevTools

Useful for investigating loading, rendering, layout shifts, and
interaction performance.

### 4. Google Search Console

The Core Web Vitals report groups URLs according to field data and
performance status.

### 5. Real User Monitoring (RUM)

A RUM solution collects performance measurements from actual visitors.
It helps teams understand performance across real devices, networks, and
usage patterns.

## 10.9 Lab data vs field data

  -----------------------------------------------------------------------
  Lab data                            Field data
  ----------------------------------- -----------------------------------
  Collected in a controlled test      Collected from real users
  environment                         

  Useful for reproducing and          Shows actual visitor experience
  debugging issues                    

  Can be run on demand                Depends on real-user traffic and
                                      data availability

  Conditions are simulated            Devices, networks, and user
                                      behavior vary
  -----------------------------------------------------------------------

Use lab data to investigate problems and field data to understand
whether users are actually experiencing them.

## 10.10 Practical HTML/CSS habits that support Core Web Vitals

``` html
<!-- Reserve image space to reduce layout shifts -->
<img
  src="hero.webp"
  alt="Product dashboard"
  width="1200"
  height="600"
  fetchpriority="high">

<!-- Lazy-load below-the-fold images -->
<img
  src="gallery.webp"
  alt="Product gallery"
  width="800"
  height="600"
  loading="lazy">
```

``` html
<!-- Defer a classic external script when appropriate -->
<script src="/js/app.js" defer></script>
```

``` css
/* Reserve space for an embedded video */
.video {
  width: 100%;
  aspect-ratio: 16 / 9;
}
```

Remember: Core Web Vitals depend on the whole application---server
performance, images, CSS, JavaScript, third-party scripts, and user
conditions---not HTML alone.

### Interview-ready answer

Core Web Vitals are Google's user-experience metrics for loading,
responsiveness, and visual stability. The three current metrics are LCP,
INP, and CLS. Good targets are LCP at or below 2.5 seconds, INP at or
below 200 milliseconds, and CLS at or below 0.1. I improve them by
optimizing critical images and server response, reducing main-thread
JavaScript work, and reserving space for images, ads, and embeds. I use
field data to understand real users and lab tools to diagnose issues.

------------------------------------------------------------------------

# 11. Why is HTML so important?

HTML is the foundation of the web because it defines the structure and
meaning of web content.

## 1. It provides the structure of every web page

Without HTML, the browser would not have a standard document structure
for headings, paragraphs, forms, links, images, and other content.

``` html
<h1>Welcome</h1>
<p>This is my website.</p>
<a href="/about">About us</a>
```

## 2. It works with CSS and JavaScript

The three technologies have different responsibilities:

  Technology   Responsibility
  ------------ ----------------------------
  HTML         Structure and meaning
  CSS          Styling and layout
  JavaScript   Behavior and interactivity

Example:

``` html
<button id="hello-button" type="button">Click me</button>

<script>
  document
    .querySelector("#hello-button")
    .addEventListener("click", () => {
      alert("Hello!");
    });
</script>
```

HTML creates the button, and JavaScript adds its behavior. CSS can style
it.

## 3. It supports accessibility

Semantic elements, headings, labels, and alternative text help assistive
technologies interpret and navigate content.

## 4. It supports SEO and content understanding

Meaningful document titles, headings, links, metadata, and semantic
structure help search engines understand a page. HTML alone does not
guarantee search rankings.

## 5. It provides native browser functionality

HTML includes built-in elements for:

-   Forms and validation.
-   Audio and video.
-   Tables and lists.
-   Navigation and links.
-   Dialogs and disclosure widgets.
-   Responsive image source selection.

## 6. It is the foundation of frontend frameworks

React, Angular, Vue, and other frontend tools ultimately produce or
manipulate browser DOM structures. Understanding HTML helps developers
write accessible, valid, and maintainable UI code.

## 7. It is relatively easy to learn and widely supported

HTML is declarative and is supported by modern browsers across desktop
and mobile platforms.

### Interview-ready answer

HTML is important because it is the foundation of web development. It
defines the structure and meaning of a web page, while CSS handles
presentation and JavaScript handles behavior. HTML also provides
semantic structure, accessibility support, native forms and media, and
the document model used by frontend frameworks. A strong understanding
of HTML helps developers build maintainable, accessible, and
search-friendly websites.

------------------------------------------------------------------------

# 12. Quick interview revision

  -----------------------------------------------------------------------
  Question                            Key points to remember
  ----------------------------------- -----------------------------------
  HTML vs HTML5                       HTML is the markup language; HTML5
                                      was a major evolution, while modern
                                      HTML follows a Living Standard

  Semantic HTML                       Elements describe meaning:
                                      `header`, `nav`, `main`, `article`,
                                      `section`, `footer`

  Block                               Starts on a new line in normal
                                      flow; width and height are
                                      respected

  Inline                              Flows with text; width and height
                                      generally do not apply to
                                      non-replaced inline boxes

  Inline-block                        Flows inline but accepts width and
                                      height

  iframe                              Embeds another document in a nested
                                      browsing context

  Data attributes                     Custom `data-*` values accessed
                                      through `element.dataset`

  Accessibility                       Makes websites usable by people
                                      with different abilities

  ARIA                                Adds accessible names,
                                      descriptions, states, roles, and
                                      relationships

  contenteditable                     Makes an element's content editable

  picture                             Offers alternative image sources
                                      for media conditions or formats

  Web Components                      Custom Elements + Shadow DOM +
                                      Templates/Slots

  LCP                                 Main visible content loading; good
                                      ≤ 2.5 s

  INP                                 Interaction responsiveness; good ≤
                                      200 ms

  CLS                                 Unexpected layout movement; good ≤
                                      0.1

  HTML importance                     Foundation for page structure,
                                      semantics, accessibility, and
                                      browser UI
  -----------------------------------------------------------------------

## Core Web Vitals memory trick

  Metric   Remember it as             Good target
  -------- ---------------- ---------------------
  LCP      Loading            2.5 seconds or less
  INP      Interaction             200 ms or less
  CLS      Stability                  0.1 or less

------------------------------------------------------------------------

# 13. Official references

Use these references when preparing for interviews or checking browser
behavior.

1.  [MDN --- HTML: HyperText Markup
    Language](https://developer.mozilla.org/en-US/docs/Web/HTML)
2.  [WHATWG --- HTML Living Standard](https://html.spec.whatwg.org/)
3.  [MDN --- HTML element
    reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)
4.  [MDN --- CSS display
    property](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/display)
5.  [MDN --- iframe
    element](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/iframe)
6.  [MDN --- Web
    Components](https://developer.mozilla.org/en-US/docs/Web/API/Web_components)
7.  [MDN --- Using custom
    elements](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_custom_elements)
8.  [MDN --- Using templates and
    slots](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_templates_and_slots)
9.  [WAI --- ARIA Authoring Practices
    Guide](https://www.w3.org/WAI/ARIA/apg/)
10. [web.dev --- Web Vitals](https://web.dev/articles/vitals)
11. [web.dev --- Core Web Vitals
    thresholds](https://web.dev/articles/defining-core-web-vitals-thresholds)
12. [Google Search Console --- Core Web Vitals
    report](https://support.google.com/webmasters/answer/9205520)

------------------------------------------------------------------------

## Final preparation advice

For each question, prepare two versions of your answer:

1.  **Short answer:** Explain the concept in 2--4 sentences.
2.  **Practical explanation:** Show a small code example and explain
    when you would use it.

For advanced questions such as Web Components and Core Web Vitals, be
ready to explain the underlying mechanism, practical use cases,
limitations, and common mistakes---not just the definition.

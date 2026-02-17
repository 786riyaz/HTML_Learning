# HTML Revision Notes

---

## Basic HTML File Structure

```html
<!DOCTYPE html>         <!-- Defines the HTML Version -->
<html lang="en">        <!-- Parent of all HTML Tags / Root Element -->
<head>                  <!-- Parent of meta data tags -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>         <!-- Title of the web page -->
</head>
<body>                  <!-- Parent of content tags -->
    <h1>Hello, World!</h1>      <!-- Heading tag -->
</body>
</html>
```

---

## File Extension

```
.html
.htm
```

---

## HTML Basics

* **Tag** ⇒ `<>`
* **Opening Tag** ⇒ `<p>`
* **Closing Tag** ⇒ `</p>`
* **Element** ⇒ `<p> Text </p>`
* Tags can contain content or other HTML tags.

---

## Emmet Shortcut

```
!
```

---

## MDN Documentation

```
https://developer.mozilla.org
```

---

## Comments

```html
<! Single Line Comment -->

<! Multi 
    Line 
    Comment
     -->
```

---

## Case Insensitivity

```html
<html> </HTML>
<p> </P>
<head> </HEAD>
<body> </BODY>
```

---

## Tag Attribute

```html
<tag attribute="value"> Text or Content </tag>
<p id="mainText"> Text </p>
```

---

## Heading Tag

`h1, h2, h3, h4, h5, h6`

```html
<h1> Heading Text </h1>
```

---

## Paragraph Tag

```html
<p> Simple Text </p>
```

---

## Span Tag

```html
<span> Simple Text </span>
```

---

## Break Tag

```html
<br>
<br/>
```

---

## Horizontal Rule Tag

```html
<hr>
<hr/>
```

---

## Image Tag

```html
<image scr="image.png" alt="AlterText" height="300px">
<img src="image.png"  loading="lazy">
```

---

## Video Tag

```html
<video src="video.mp4" height="330px" autoplay controls loop>
<video width="640px" autoplay loop>
    <source src="video.mp4" type="video/mp4">
        Your Browser does not support the video tag.
</video>
```

---

## Anchor Tag

```html
<a href="https://www.google.com" target="_blank"> Link Text </a>
<a href="#homeID"> Home </a>
```

---

## Text Formatting Tags

**Bold**

```html
<b> Bold Text </b>
```

**Italic**

```html
<i> Italic Text </i>
```

**Underline**

```html
<u> Underline Text </u>
```

**Strike Through**

```html
<s> Strike Through Text </s>
```

---

## Preformatted Text

```html
<pre> Here     is the 
            pre formatted Text......       ! </pre>
```

---

## Big Tag

```html
<big> Big Text </big>
```

---

## Small Tag

```html
<small> Small Text </small>
```

---

## Superscript Tag

```html
(a+b)<sup>2</sup>=a<sup>2</sup>+2ab+b<sup>2</sup>
```

---

## Subscript Tag

```html
H<sub>2</sub>O
```

---

## Character Entities

```
&nbsp;
&euro;
&copy;
&reg;
&Delta;
&lt;
&gt;
&amp;
&quot;
&apos;
```

---

## Division Tag

```html
<div> Container for other tags and content </div>
```

---

## Browser Tools

1. **View Page Source**

   * View all page content
   * Shortcut: `Ctrl + U`

2. **Inspect Element**

   * View selected element with applied styling
   * Can live edit HTML, CSS, and JS

---

## Responsive Design

* Adapts layout for different screen sizes
* Flexible layouts
* Enhances user experience on mobile and desktop

---

## HTML Validation

* Modern browsers support code completion for HTML
* Validate using:

```
validator.w3.org
```

---

## Semantic Tags (Better for SEO)

```
header
footer
article
section
nav
main
figure
aside
details
summary
```

---

## Block Elements

```
div, p, h1, ul, li
```

---

## Inline Elements

```
span, em, img...
```

```
display: inline
display: block
display: inline-block
```

---

## Ordered List

**Type:** `1, A, a, i, I`

```html
<ol>
    <li>First</li>
    <li>Second</li>
    <li>Third</li>
</ol>
```

---

## Unordered List

**Type:** `disc`

```html
<ul>
    <li>Home</li>
    <li>About</li>
    <li>Dashboard</li>
</ul>
```

---

## Table Tag

Tags:

```
table, thead, tbody, tfoot, tr, th, caption, colspan, rowspan
```

```html
<table style="width:100%; border:1px solid black;">
    <caption>Employee Information</caption>
    <thead>
        <tr>
            <th style="border:1px solid black;">ID</th>
            <th style="border:1px solid black;">Name</th>
            <th style="border:1px solid black;">Salary</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border:1px solid black;">1<td>
            <td style="border:1px solid black;">Riyaz<td>
            <td style="border:1px solid black;">100<td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td style="border:1px solid black;"><td>
            <td style="border:1px solid black;">Total<td>
            <td style="border:1px solid black;">100<td>
        </tr>
    </tfoot>
</table>
```

---

## Form Tag

```html
<form action="/submit.php" method="post">
```

### Input Tag

```html
<input type="text" placeholder="Enter Name">
```

### Submit Button

```html
<input type="submit" value="Submit">
```

### Name and Value

```html
<input type="text" name="username" value="Default" id="username">
```

### Label

```html
<label for="username"> UserName : </label>
```

### Radio

```html
<input type="radio" id="male" name="gender" value="Male">
<input type="radio" id="female" name="gender" value="Female">
```

### Checkbox

```html
<input type="checkbox" id="cherry" name="fruit" value="Banana">
```

### Select

```html
<select id="fruits" name="fruits">
    <option value="apple"> Apple </option>
    <option value="Banana"> Banana </option>
    <option value="Cherry"> Cherry </option>
</select>
```

### Text Area

```html
<textarea rows="4" cols="40">Default Text here </textarea>
```

### Input Types

```
text
password
date
file
color
range
button
radio
select
checkbox
time
month
week
tel
hidden
url
```

---

## iFrame

Allows embedding another webpage.

```html
<iframe width="300" height="200" src="https://en.wikipedia/org/wiki/Main_Page"></iframe>
```

---

## SEO (Search Engine Optimization)

* Title Tag
* Meta Description
* URL Slug
* Meta Author Tag
* Favicon
* Image Optimization
* Semantic HTML

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="">
<meta name="author" content="">
```

---

## Core Web Vitals (CWV)

* **LCP** ⇒ Largest Contentful Paint ⇒ `2.5 seconds`
* **INP** ⇒ Interaction to Next Paint ⇒ `200 milliseconds`
* **CLS** ⇒ Cumulative Layout Shift ⇒ `0.1`
* **FCP** ⇒ First Contentful Paint

---
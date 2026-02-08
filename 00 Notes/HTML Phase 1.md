# 📘 HTML PHASE 1 – BASICS (COMPLETE GUIDE)

![Image](https://www.tutorialspoint.com/assets/questions/images/146383-1516362370.jpg)

![Image](https://files.codingninjas.in/article_images/difference-between-html-elements-and-tags-0-1729838840.webp)

![Image](https://img.uxcel.com/cdn-cgi/image/format%3Dauto/practices/the-heading-tags-h1-to-h6-1615535492158/a-1702048418566-2x.jpg)

![Image](https://www.w3docs.com/uploads/media/default/0001/01/ad7f83563a7009977279a2aea4695d5b7d7e7847.png)

![Image](https://cdn.sanity.io/images/tkl0o0xu/production/22b1647082b7d4620aa653e3e0419aa6d3a7ba65-1200x630.png?fit=min\&fm=jpg\&h=629\&q=95\&w=1200)

![Image](https://dmguru.in/pages/default/assets/images/heading-tags.jpg)

---

## 1️⃣ What is HTML?

**HTML (HyperText Markup Language)** is the **standard language used to create web pages**.

* HTML **does NOT style** the page → CSS does that
* HTML **does NOT add logic** → JavaScript does that
* HTML **defines structure & content**

📌 Example:

* Text
* Images
* Links
* Headings
* Lists

---

## 2️⃣ How HTML Works (Very Important)

HTML works using **tags**.

### HTML Tag Structure

```html
<tagname>Content</tagname>
```

### Example

```html
<p>Hello World</p>
```

* `<p>` → opening tag
* `</p>` → closing tag
* `Hello World` → content

Some tags **do not need closing**:

```html
<br>
<hr>
<img>
```

---

## 3️⃣ Basic HTML Document Structure

Every HTML file must have this structure:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My First Page</title>
</head>
<body>

  <h1>Hello HTML</h1>
  <p>This is my first web page.</p>

</body>
</html>
```

### Explanation (Line by Line)

* `<!DOCTYPE html>`
  ➜ Tells browser this is **HTML5**
* `<html>`
  ➜ Root element (wraps everything)
* `<head>`
  ➜ Meta info (not visible)
* `<title>`
  ➜ Page title (browser tab)
* `<body>`
  ➜ Visible content

⚠️ **Never skip this structure**

---

## 4️⃣ Headings (h1 – h6)

HTML has **6 heading levels**.

```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Section</h3>
<h4>Sub Section</h4>
<h5>Small Heading</h5>
<h6>Very Small</h6>
```

### Rules

* Use **only ONE `<h1>` per page**
* Headings are for **structure**, not size
* Important for **SEO**

---

## 5️⃣ Paragraphs & Text Tags

### Paragraph

```html
<p>This is a paragraph.</p>
```

### Line Break

```html
Hello<br>World
```

### Horizontal Line

```html
<hr>
```

---

## 6️⃣ Text Formatting Tags

```html
<b>Bold</b>
<strong>Important</strong>

<i>Italic</i>
<em>Emphasis</em>

<u>Underline</u>
<mark>Highlighted</mark>

<small>Small text</small>
```

### Difference You Must Know

* `<b>` → visual bold
* `<strong>` → **semantic importance** (SEO & accessibility)

Same for:

* `<i>` vs `<em>`

---

## 7️⃣ HTML Comments

Comments are **not shown** in browser.

```html
<!-- This is a comment -->
```

Used for:

* Notes
* Temporarily disabling code
* Documentation

---

## 8️⃣ Links (Anchor Tag)

```html
<a href="https://google.com">Go to Google</a>
```

### Open Link in New Tab

```html
<a href="https://google.com" target="_blank">Google</a>
```

### Relative vs Absolute Links

**Absolute**

```html
<a href="https://example.com/about">About</a>
```

**Relative**

```html
<a href="about.html">About</a>
```

---

## 9️⃣ Images (`img` tag)

```html
<img src="image.jpg" alt="My image">
```

### Important Attributes

* `src` → image path
* `alt` → text if image fails (VERY IMPORTANT for accessibility)

Example:

```html
<img src="logo.png" alt="Company Logo">
```

---

## 🔟 Lists

### Unordered List (Bullets)

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
  <li>Mango</li>
</ul>
```

### Ordered List (Numbers)

```html
<ol>
  <li>Step One</li>
  <li>Step Two</li>
</ol>
```

### Nested List

```html
<ul>
  <li>Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
    </ul>
  </li>
</ul>
```

---

## 1️⃣1️⃣ HTML Attributes

Attributes give **extra information** to tags.

### Syntax

```html
<tag attribute="value">
```

### Examples

```html
<img src="img.png" alt="Image">
<a href="page.html">Link</a>
```

---

## 1️⃣2️⃣ File Naming & Best Practices

✔ Use lowercase file names
✔ Use `.html` extension
✔ No spaces → use `-`

Example:

```
index.html
about-us.html
contact.html
```

---

## 1️⃣3️⃣ First Practice Task (MANDATORY)

Create a file **`index.html`** with:

✔ Page title
✔ One `<h1>`
✔ Two paragraphs
✔ One image
✔ One link
✔ One list

Example starter:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My First HTML Page</title>
</head>
<body>

  <h1>Welcome</h1>
  <p>This is my first HTML page.</p>
  <p>I am learning HTML.</p>

</body>
</html>
```

---

## ✅ Phase 1 Completion Checklist

✔ HTML structure
✔ Tags & elements
✔ Headings
✔ Paragraphs
✔ Links
✔ Images
✔ Lists
✔ Attributes

If you understand **90% of this**, you are **ready for Phase 2**.

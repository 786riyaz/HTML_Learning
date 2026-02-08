# 📘 HTML PHASE 4 – ADVANCED HTML (HTML5 FEATURES)

![Image](https://www.gwtproject.org/doc/latest/images/localStorage.png)

![Image](https://www.c-sharpcorner.com/UploadFile/75a48f/html5-contenteditable-attribute/Images/Example2.PNG)

![Image](https://addyosmani.com/assets/images/loading-attribute%402x.png)

![Image](https://web.dev/static/articles/browser-level-image-lazy-loading/image/the-and-improved-thresho-a20c669983f73.png)

![Image](https://www.debugbear.com/dimg/eb63fd53d8917de507d8363a96483876.png)

---

## 1️⃣ Native Form Validation (HTML5)

HTML can validate forms **without JavaScript**.

### Required Fields

```html
<input type="text" required>
```

### Pattern Validation

```html
<input type="text" pattern="[A-Za-z]{3,}">
```

✔ Minimum 3 letters
✔ No numbers allowed

---

### Min & Max

```html
<input type="number" min="1" max="10">
```

---

### Email Validation

```html
<input type="email">
```

Browser automatically checks:

* `@`
* domain format

---

## 2️⃣ `contenteditable` Attribute

Allows user to edit text directly.

```html
<p contenteditable="true">Edit me</p>
```

Use cases:

* CMS systems
* Inline editors
* Notes apps

📌 Interview tip:

> Contenteditable makes any element user-editable without JS.

---

## 3️⃣ Lazy Loading Images (Performance)

```html
<img src="photo.jpg" loading="lazy" alt="Photo">
```

✔ Images load **only when needed**
✔ Improves page speed
✔ SEO friendly

---

## 4️⃣ Responsive Images – `<picture>`

Used to load different images for different screens.

```html
<picture>
  <source media="(max-width: 600px)" srcset="mobile.jpg">
  <source media="(min-width: 601px)" srcset="desktop.jpg">
  <img src="desktop.jpg" alt="Responsive image">
</picture>
```

📌 Browser selects best image automatically.

---

## 5️⃣ `srcset` Attribute (Image Optimization)

```html
<img
  src="small.jpg"
  srcset="small.jpg 480w, medium.jpg 768w, large.jpg 1200w"
  sizes="(max-width: 600px) 100vw, 50vw"
  alt="Sample image">
```

✔ Improves loading
✔ Saves bandwidth

---

## 6️⃣ Local Storage (HTML5 API – Intro)

Stores data in browser.

```html
<script>
  localStorage.setItem("name", "Riyaz");
  localStorage.getItem("name");
</script>
```

📌 Key points:

* Data persists after refresh
* Storage is per domain
* Size ~5MB

---

## 7️⃣ Session Storage

```html
sessionStorage.setItem("token", "123");
```

✔ Data cleared when tab closes

---

## 8️⃣ `<details>` & `<summary>`

Creates expandable content.

```html
<details>
  <summary>Read more</summary>
  <p>This is hidden content.</p>
</details>
```

✔ No JS required
✔ Accessible by default

---

## 9️⃣ `<progress>` & `<meter>`

### Progress Bar

```html
<progress value="70" max="100"></progress>
```

### Meter

```html
<meter value="0.6"></meter>
```

---

## 🔟 `<template>` Tag (Concept)

```html
<template id="card">
  <div class="card">
    <h3>Title</h3>
  </div>
</template>
```

✔ Not rendered
✔ Used by JavaScript later

---

## 1️⃣1️⃣ `<noscript>` Tag

Shown when JavaScript is disabled.

```html
<noscript>
  Please enable JavaScript
</noscript>
```

---

## 1️⃣2️⃣ HTML Performance Best Practices

✔ Use semantic tags
✔ Lazy load images
✔ Use `alt` text
✔ Avoid deep nesting
✔ Minimize unused markup

---

## 🧪 Final HTML Project (MANDATORY)

### Build a **Blog Website (HTML Only)**

Must include:

* Semantic layout
* At least 2 articles
* Navigation
* Images with lazy loading
* Responsive image using `<picture>`
* Form with validation
* Footer

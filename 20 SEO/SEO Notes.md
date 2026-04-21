#  SEO

We will focus only on the **HTML standpoint of SEO**.
We will not be looking into **keyword building** and **content optimization** aspects of SEO.

---

## 🔹 Types of SEO

* **On-page SEO** (This can be done by HTML developers)
* **Off-page SEO**

---

## 🔹 HTML SEO

HTML developers can implement SEO using the following techniques:

### 1. Title Tag

Set a clear and descriptive `<title>` tag that accurately reflects the content of the page.

---

### 2. Meta Description

Provide a concise summary of the page content using the `<meta>` tag.

```html
<meta name="description" content="Your page description here">
```

---

### 3. URL Slug

Use a clean and readable URL structure that includes relevant keywords.

Example:

```
https://example.com/seo-guide
```

---

### 4. Meta Author Tag

Optionally include the author information in a `<meta>` tag.

```html
<meta name="author" content="Author Name">
```

---

### 5. Favicon

Use a favicon to enhance brand recognition and usability.

```html
<link rel="icon" href="favicon.ico">
```

---

### 6. Image Optimization

* Compress images to improve page load time
* Use descriptive `alt` attributes

```html
<img src="image.jpg" alt="SEO optimized image description">
```

---

### 7. Optimize Resources

* Remove unused HTML, CSS, and JavaScript files
* Minify and compress files to reduce load time

---

### 8. Semantic HTML

Use appropriate HTML tags to structure content logically. This improves accessibility and helps search engines understand your content.

Examples:

```html
<header></header>
<nav></nav>
<article></article>
<footer></footer>
```

---

## 🔹 Example HTML SEO Setup

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <!-- Responsive Design -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- SEO Meta Tags -->
    <meta name="description" content="Learn how to install VS Code on Android easily">
    <meta name="author" content="video editor">

    <!-- Title -->
    <title>How to Install VS Code on Android - Video Editor</title>

    <!-- Favicon -->
    <link rel="icon" href="favicon.ico">
</head>

<body>
    <header>
        <h1>Welcome to SEO Guide</h1>
    </header>
</body>
</html>
```

---

## ✅ Summary

HTML SEO focuses on:

* Proper metadata (`title`, `description`, `author`)
* Clean URLs
* Optimized images
* Fast loading resources
* Semantic structure
# 📘 HTML PHASE 3 – SEMANTIC, SEO & ACCESSIBILITY

![Image](https://images.openai.com/static-rsc-3/SIRdSa9erE-WxLbTWOJEMK6LuoyU3tFNgWhr0rRYJQjr-elrF_q5-WhVp2drmFzjI5E3HaHbfpcpjqIbjWJT3nMxI0fZ73vVdtOUCXz4sns?purpose=fullsize\&v=1)

![Image](https://www.w3schools.com/html/img_sem_elements.gif)

![Image](https://web.dev/static/articles/aria-labels-and-relationships/image/using-aria-label-identif-89ed5dcc8c595.jpg)

![Image](https://media2.dev.to/dynamic/image/width%3D1080%2Cheight%3D1080%2Cfit%3Dcover%2Cgravity%3Dauto%2Cformat%3Dauto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F0v383znjoqnb7yqkcrxk.png)

![Image](https://web.dev/static/learn/accessibility/aria-html/image/the-aria-augmented-access-70b111217be0f.jpg)

---

## 1️⃣ What is Semantic HTML?

**Semantic HTML** means using tags that **clearly describe their meaning**.

❌ Non-semantic:

```html
<div class="header"></div>
<div class="menu"></div>
<div class="footer"></div>
```

✅ Semantic:

```html
<header></header>
<nav></nav>
<footer></footer>
```

📌 Browsers, search engines, and screen readers **understand semantics**.

---

## 2️⃣ Important Semantic Tags (MUST KNOW)

| Tag         | Purpose                          |
| ----------- | -------------------------------- |
| `<header>`  | Top section of page/section      |
| `<nav>`     | Navigation links                 |
| `<main>`    | Main content (only one per page) |
| `<section>` | Logical section                  |
| `<article>` | Independent content              |
| `<aside>`   | Sidebar / related content        |
| `<footer>`  | Bottom section                   |

---

## 3️⃣ Real Page Layout Using Semantic HTML

```html
<!DOCTYPE html>
<html>
<head>
  <title>Semantic Page</title>
</head>
<body>

<header>
  <h1>My Website</h1>
</header>

<nav>
  <a href="#">Home</a>
  <a href="#">About</a>
</nav>

<main>
  <section>
    <h2>Blog</h2>
    <article>
      <h3>Post Title</h3>
      <p>Post content...</p>
    </article>
  </section>

  <aside>
    <p>Related links</p>
  </aside>
</main>

<footer>
  <p>© 2026</p>
</footer>

</body>
</html>
```

---

## 4️⃣ SEO Basics Using HTML

### Heading Hierarchy

✔ Only one `<h1>`
✔ Do not skip levels

❌ Wrong:

```html
<h1>Title</h1>
<h4>Subtitle</h4>
```

✅ Correct:

```html
<h1>Title</h1>
<h2>Subtitle</h2>
```

---

### Meta Description

```html
<meta name="description" content="Learn HTML step by step from basics to advanced.">
```

📌 Improves **search preview**

---

## 5️⃣ Accessibility (A11Y) – MUST KNOW

### Images with alt text

```html
<img src="team.jpg" alt="Our development team">
```

### Form labels (Already learned)

```html
<label for="email">Email</label>
<input id="email">
```

---

## 6️⃣ ARIA Attributes (Intro Level)

ARIA helps screen readers.

```html
<button aria-label="Close Menu">X</button>
```

Common ARIA:

* `aria-label`
* `aria-hidden="true"`
* `role="button"`

📌 Use **only when semantic HTML is not enough**

---

## 7️⃣ Accessible Navigation Example

```html
<nav aria-label="Main navigation">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
  </ul>
</nav>
```

---

## 8️⃣ Data Attributes (`data-*`)

Used to store **custom data**.

```html
<button data-id="101">Buy</button>
```

Access later via JavaScript:

```js
element.dataset.id
```

---

## 9️⃣ `<main>` Rules (INTERVIEW QUESTION)

✔ Only **one `<main>` per page**
✔ Should NOT be inside `header`, `nav`, `footer`

---

## 🔟 `<article>` vs `<section>` (CONFUSING BUT IMPORTANT)

### `<article>`

* Independent
* Reusable
* Example: blog post, news item

### `<section>`

* Logical grouping
* Depends on context

📌 Interview answer:

> Use `<article>` when content can stand alone.

---

## 1️⃣1️⃣ `<div>` vs Semantic Tags

✔ Use semantic tags when possible
✔ Use `<div>` only when **no semantic tag fits**

---

## 🧪 Practice Tasks (MANDATORY)

### Task 1

Convert this:

```html
<div class="header"></div>
<div class="content"></div>
<div class="footer"></div>
```

Into **semantic HTML**

---

### Task 2

Create a **blog page** using:

* header
* nav
* main
* section
* article
* footer

---

## ✅ Phase 3 Completion Checklist

✔ Semantic tags
✔ SEO basics
✔ Accessibility basics
✔ ARIA intro
✔ Data attributes

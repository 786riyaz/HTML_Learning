# Block vs Inline Elements in HTML

---

## Block Elements

### Characteristics
- **New Line** → Always start on a new line  
- **Full Width** → Occupy the entire horizontal width available  
- **Styling** → Support margins and padding  
- **Size Control** → Width and height can be explicitly set  

### Key Points
- A block-level element always starts on a new line  
- It stretches fully from left to right  
- Has both **top and bottom margins**  

### Examples
- Common:
  - `<div>`, `<p>`, `<h1>`–`<h6>`, `<ul>`, `<li>`

- Extended List:
```

  <address> <article> <aside> <blockquote> <canvas> <dd> <div> <dl> <dt>
  <fieldset> <figcaption> <figure> <footer> <form> <header>
  <hr> <li> <main> <nav> <noscript> <ol> <p> <pre> <section>
  <table> <tfoot> <ul> <video>
  ```

---

## Inline Elements

### Characteristics

* **Inline Flow** → Stay within the same line as surrounding text
* **Content Width** → Only take up as much width as needed
* **No Line Break** → Do not start on a new line
* **Limited Styling** → Width/height typically cannot be set directly

### Key Points

* An inline element does not start on a new line
* Occupies only the required space
* Does not support vertical margins like block elements

### Examples

* Common:

  * `<span>`, `<em>`, `<img>`

* Extended List:

  ```
  <a> <abbr> <acronym> <b> <bdo> <big> <br> <button> <cite> <code>
  <dfn> <em> <i> <img> <input> <kbd> <label> <map> <object> <output>
  <q> <samp> <script> <select> <small> <span> <strong> <sub> <sup>
  <textarea> <time> <tt> <var>
  ```

---

## Summary

| Feature          | Block Elements                 | Inline Elements          |
| ---------------- | ------------------------------ | ------------------------ |
| Line Break       | Starts on new line             | No new line              |
| Width            | Full width                     | Content-based width      |
| Height/Width Set | Yes                            | Limited                  |
| Margin Support   | Top & Bottom margins supported | Limited vertical margins |
| Usage            | Layout & structure             | Text-level styling       |

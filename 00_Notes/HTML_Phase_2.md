# 📘 HTML PHASE 2 – INTERMEDIATE (COMPLETE GUIDE)

![Image](https://myschoolhouse.in/admin-panel/assets/upload-images/HTML-Tables5428-D-11-04-2024-T-05-37-32am.jpg)

![Image](https://daily-dev-tips.com/images/12-05-2020.jpg)

![Image](https://cdn.jim-nielsen.com/blog/2021/select-highlight-color.png)

![Image](https://i.sstatic.net/Hc7O5.png)

![Image](https://www.simplilearn.com/ice9/free_resources_article_thumb/html-select-tag.PNG)

---

## 1️⃣ HTML Tables (Structured Data)

Tables are used for **tabular data** (not layout).

### Basic Table Structure

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Riyaz</td>
    <td>25</td>
  </tr>
</table>
```

### Table Tags Explained

* `<table>` → table container
* `<tr>` → table row
* `<th>` → table heading (bold + semantic)
* `<td>` → table data cell

---

### Proper Table Structure (Best Practice)

```html
<table>
  <thead>
    <tr>
      <th>Product</th>
      <th>Price</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Laptop</td>
      <td>₹60,000</td>
    </tr>
  </tbody>
</table>
```

📌 `thead` & `tbody` improve **readability & accessibility**

---

## 2️⃣ HTML Forms (VERY IMPORTANT)

Forms collect **user input**.

### Basic Form

```html
<form>
  <label>Name:</label>
  <input type="text">
</form>
```

---

## 3️⃣ Input Types (Must Know)

```html
<input type="text">
<input type="email">
<input type="password">
<input type="number">
<input type="date">
<input type="file">
```

📌 Browser gives **automatic validation** for `email`, `number`, etc.

---

## 4️⃣ Labels (Accessibility Rule)

### ❌ Wrong

```html
<input type="text">
```

### ✅ Correct

```html
<label for="username">Username</label>
<input type="text" id="username">
```

✔ Clicking label focuses input
✔ Screen readers work correctly

---

## 5️⃣ Radio Buttons & Checkboxes

### Radio (Select ONE)

```html
<input type="radio" name="gender"> Male
<input type="radio" name="gender"> Female
```

📌 Same `name` → only one selectable

### Checkbox (Select MANY)

```html
<input type="checkbox"> HTML
<input type="checkbox"> CSS
```

---

## 6️⃣ Select Dropdown

```html
<select>
  <option>India</option>
  <option>USA</option>
  <option>UK</option>
</select>
```

With label:

```html
<label>Country</label>
<select>
  <option value="in">India</option>
  <option value="us">USA</option>
</select>
```

---

## 7️⃣ Textarea (Multi-line Input)

```html
<textarea rows="4" cols="30"></textarea>
```

Used for:

* Address
* Feedback
* Comments

---

## 8️⃣ Button Types

```html
<button>Click Me</button>
<button type="submit">Submit</button>
<button type="reset">Reset</button>
```

---

## 9️⃣ Form Attributes (INTERVIEW IMPORTANT)

```html
<input type="text" required>
<input type="email" placeholder="Enter email">
<input type="text" readonly>
<input type="text" disabled>
```

### Meaning

* `required` → cannot submit empty
* `placeholder` → hint text
* `readonly` → editable ❌, submit ✔
* `disabled` → editable ❌, submit ❌

---

## 🔟 Audio & Video

### Audio

```html
<audio controls>
  <source src="song.mp3">
</audio>
```

### Video

```html
<video width="300" controls>
  <source src="movie.mp4">
</video>
```

---

## 1️⃣1️⃣ iframe (Embedding Content)

```html
<iframe src="https://example.com"></iframe>
```

Used for:

* Maps
* Videos
* External pages

---

## 1️⃣2️⃣ Meta Tags (Inside `<head>`)

### Charset

```html
<meta charset="UTF-8">
```

### Responsive Viewport (VERY IMPORTANT)

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

📌 Without this → mobile layout breaks

---

## 1️⃣3️⃣ HTML Entities

Used for **special characters**.

```html
&lt;   → <
&gt;   → >
&amp;  → &
&nbsp; → space
```

Example:

```html
<p>5 &lt; 10</p>
```

---

## 1️⃣4️⃣ Complete Form Example (REAL WORLD)

```html
<form>
  <label>Name</label><br>
  <input type="text" required><br><br>

  <label>Email</label><br>
  <input type="email" required><br><br>

  <label>Gender</label><br>
  <input type="radio" name="g"> Male
  <input type="radio" name="g"> Female<br><br>

  <label>Message</label><br>
  <textarea></textarea><br><br>

  <button type="submit">Send</button>
</form>
```

---

## 🧪 Practice Tasks (MANDATORY)

### Task 1

✔ Create a **student registration form**

Must include:

* Text
* Email
* Radio
* Checkbox
* Select
* Submit button

### Task 2

✔ Create a **table** with:

* 3 columns
* 5 rows
* `thead` & `tbody`

---

## ✅ Phase 2 Completion Checklist

✔ Tables
✔ Forms
✔ Input types
✔ Labels & accessibility
✔ Media tags
✔ Meta viewport
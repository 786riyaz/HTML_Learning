# HTML Form Input Elements

---

## `<input>` Tag

### Purpose
- Used inside a `<form>` to **collect user input**

### Key Features
- **Self-Closing** → `<input>` does not require a closing tag  
- **Attributes** → Common attributes:
  - `name`
  - `value`
  - `placeholder`
  - `required`

---

## Input Types

Common `type` values for `<input>`:

- `text` → Single-line text input  
- `password` → Hidden text input  
- `date` → Date picker  
- `color` → Color picker  
- `file` → File upload  
- `range` → Slider input  
- `button` → Clickable button  
- `radio` → Select one option  
- `checkbox` → Select multiple options  
- `email` → Email input with validation  
- `number` → Numeric input  
- `time` → Time picker  
- `month` → Month selector  
- `week` → Week selector  
- `tel` → Telephone number  
- `url` → URL input  
- `image` → Image submit button  
- `hidden` → Hidden data field  
- `reset` → Reset form  
- `submit` → Submit form  

> Note: `<select>` and `<textarea>` are form elements but **not input types**

---

## Example: Input Fields

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="username" placeholder="Enter your name" required>

  <br><br>

  <label for="password">Password:</label>
  <input type="password" id="password" name="password">

  <br><br>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <br><br>

  <label>Gender:</label>
  <input type="radio" name="gender" value="male"> Male
  <input type="radio" name="gender" value="female"> Female

  <br><br>

  <label>Hobbies:</label>
  <input type="checkbox" name="hobby" value="reading"> Reading
  <input type="checkbox" name="hobby" value="sports"> Sports

  <br><br>

  <input type="submit" value="Submit">
  <input type="reset" value="Reset">
</form>
````

---

## `action` Attribute

### Purpose

* Specifies the **URL where form data is sent** after submission

### Key Points

* **Default** → Submits to the same page if not specified
* **Server-Side Handling** → Usually points to backend scripts (PHP, Python, Node.js, etc.)

### Example

```html
<form action="/submit-form">
  <input type="text" name="username">
  <input type="submit">
</form>
```

---

## `name` and `value` Properties

### `name` Property

* Acts as an **identifier for form data**
* Used when sending data to the server
* Should be **unique for clarity**

### `value` Property

* Sets the **default value** of an input
* This is the **actual data sent to the server**

### Example

```html
<input type="text" name="username" value="Riyaz">
```

---

## `<label>` Tag

### Purpose

* Provides a **text description** for form elements

### Key Features

* **`for` Attribute** → Links label with input using `id`
* **Accessibility** → Improves usability for screen readers
* **Readability** → Makes forms easier to understand

### Example

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```

---

## Special Attributes

### `disabled`

* Disables the input field
* User cannot interact with it

```html
<input type="text" disabled value="Disabled Field">
```

---

### `readonly`

* Makes input **read-only** (cannot edit, but value is still submitted)

```html
<input type="text" value="Read Only Value" readonly>
```

---

### `submit`

* Used to **submit the form**

```html
<input type="submit" value="Submit Form">
```

---

### `reset`

* Resets all form fields to default values

```html
<input type="reset" value="Reset Form">
```

---

## Additional Form Elements

### `<textarea>`

* Used for **multi-line input**
* Row Property :: Speciafies the visible number of lines in the textarea.
* Cols Property :: Sets the visible width measured in average characters width.
* Resizable :: Some browsers allow users to manually resize the textarea.

```html
<textarea name="message" rows="4" cols="30"></textarea>
```

---

### `<select>`

* Used for **dropdown lists**

```html
<select name="country">
  <option value="india">India</option>
  <option value="usa">USA</option>
</select>
```

---

## Summary

| Feature        | Description            |
| -------------- | ---------------------- |
| `<input>`      | Collects user input    |
| `type`         | Defines input behavior |
| `action`       | URL where data is sent |
| `name`         | Identifies form data   |
| `value`        | Default/sent value     |
| `<label>`      | Improves accessibility |
| `disabled`     | Disables input         |
| `readonly`     | Read-only input        |
| `submit/reset` | Form controls          |

---
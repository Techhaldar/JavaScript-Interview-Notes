# What is the DOM and how does JavaScript interact with it?

---

## ✅ Explanation

The **DOM (Document Object Model)** is a **programming interface** provided by browsers.

It represents the structure of a web page as a **tree of nodes (objects)**.  
Each element (HTML tag), attribute, and piece of text in the document becomes a **node** in this tree.

JavaScript uses the DOM API to:

- Access elements
- Modify content
- Change styles
- Handle events dynamically

---

## 🌳 DOM Tree Example

Given this HTML:

```html
<html>
  <body>
    <h1>Hello World</h1>
    <p>Welcome to JavaScript DOM!</p>
  </body>
</html>
```

## The DOM tree looks like:

```css
Document
 └── html
      ├── body
      │     ├── h1 (Hello World)
      │     └── p (Welcome to JavaScript DOM!)

```

## 🔥 JavaScript Interacting with DOM

---

### 1️⃣ Selecting Elements

```javascript
// By ID
const heading = document.getElementById("myHeading");

// By Class
const items = document.getElementsByClassName("item");

// By Tag Name
const paragraphs = document.getElementsByTagName("p");

// Modern Selector
const firstItem = document.querySelector(".item");
const allItems = document.querySelectorAll(".item");
```

### 2️⃣ Modifying Content

```javascript
heading.textContent = "Updated Heading!";
paragraphs[0].innerHTML = "<strong>Bold text</strong>";
```

### 3️⃣ Changing Styles

```javascript
heading.style.color = "blue";
heading.style.fontSize = "2em";
```

### 4️⃣ Adding Event Listeners

```javascript
heading.addEventListener("click", () => {
  alert("Heading clicked!");
});
```

## 💡 Key Points

```text
✅ The DOM is not part of JavaScript; it’s a browser feature.

✅ Provides methods like getElementById, querySelector, etc.

✅ Enables dynamic changes to HTML and CSS without reloading the page.

✅ Events (clicks, inputs, etc.) are handled via the DOM.
```

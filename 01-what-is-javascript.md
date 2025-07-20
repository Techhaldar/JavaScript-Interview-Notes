# What is JavaScript and what are its key features?.

## ✅ Explanation

JavaScript (JS) is a **high-level**, **interpreted**, and **lightweight programming language** that is one of the core technologies of the web, alongside HTML and CSS. It was created in 1995 by Brendan Eich and has become the most widely used language for adding interactivity to websites.

Originally designed for client-side scripting (running in browsers), JavaScript is now also used for server-side development (thanks to Node.js).

JavaScript is an **object-oriented**, **prototype-based**, and **multi-paradigm language**, supporting:

- Imperative programming
- Functional programming
- Event-driven programming

It runs in web browsers (via JavaScript engines like Chrome’s V8) and allows developers to build interactive web applications.

---

## 💡 Key Features of JavaScript

- **Lightweight and Interpreted**
  - Runs directly in browsers without prior compilation.
- **Dynamic Typing**
  - Variables are not bound to a specific data type. Example:
    ```javascript
    let x = 10; // number
    x = "Hello"; // string
    ```
- **Prototype-Based Inheritance**
  - Objects can inherit from other objects.
- **First-Class Functions**
  - Functions are treated like any other variable (can be passed as arguments, returned, etc.).
- **Asynchronous Programming**
  - Handles tasks like API calls using callbacks, promises, and async/await.
- **Platform Independence**
  - Works across all major browsers and operating systems.
- **Rich APIs**
  - Provides APIs for DOM manipulation, event handling, and AJAX.

---

## 🔥 Example: Simple JavaScript in HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>JavaScript Example</title>
  </head>
  <body>
    <h1 id="greeting">Hello, World!</h1>
    <button onclick="changeText()">Click Me</button>

    <script>
      function changeText() {
        document.getElementById("greeting").innerHTML = "Hello, JavaScript!";
      }
    </script>
  </body>
</html>
```

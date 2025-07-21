---

## 📁 `07-this-keyword.md`

```markdown
# What is the `this` keyword in JavaScript?

---

## ✅ Explanation

The `this` keyword refers to the **context** in which a function is called. Its value depends on **how the function is invoked**:

---

### 🟢 1. Global Context

In browsers, `this` refers to the `window` object.

```javascript
console.log(this); // window
```

### 🟠 2. Object Method

In an object, `this` refers to the object itself.

```javascript
const obj = {
  name: "JS",
  greet() {
    console.log(this.name); // "JS"
  },
};
obj.greet();
```

### 🔴 3. Standalone Function (non-strict mode)

`this` points to `window`

```javascript
function show() {
  console.log(this);
}
show(); // window
```

### 🔵 4. In Strict Mode

`this` is `undefined`

```javascript
"use strict";
function show() {
  console.log(this);
}
show(); // undefined
```

### 🟣 5. Arrow Functions

Arrow functions do not bind their own `this`. They inherit it from their parent scope

```javascript
const obj = {
  value: 10,
  arrow: () => {
    console.log(this.value);
  },
};
obj.arrow(); // undefined
```

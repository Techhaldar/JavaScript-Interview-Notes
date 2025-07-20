## 📁 `04-hoisting.md`

````markdown
# What is hoisting in JavaScript?

## ✅ Explanation

Hoisting is a JavaScript behavior where **variable and function declarations** are moved to the **top of their scope** before code execution.

This means you can use a variable or function **before declaring it**, but there are important differences between `var`, `let`, `const`, and functions:

---

### 🔥 How it Works

- `var` declarations are **hoisted and initialized** as `undefined`.
- `let` and `const` declarations are **hoisted but not initialized** (Temporal Dead Zone).
- Function declarations are **fully hoisted**.
- Function expressions are **not fully hoisted**.

---

## 💡 Key Points

- ✅ Only declarations are hoisted, **not initializations**.
- ✅ Accessing `let`/`const` before declaration → ReferenceError.
- ✅ Function declarations are hoisted above code.

---

## 🔥 Example

```javascript
console.log(a); // undefined (var hoisted)
var a = 5;

console.log(b); // ReferenceError (let not initialized)
let b = 10;

hoistedFunc(); // "I am hoisted!"
function hoistedFunc() {
  console.log("I am hoisted!");
}

nonHoistedFunc(); // TypeError
var nonHoistedFunc = function () {
  console.log("Not hoisted!");
};
```
````

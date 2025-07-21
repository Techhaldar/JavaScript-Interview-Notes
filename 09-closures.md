# What are Closures in JavaScript?

---

## ✅ Explanation

A **closure** is created when a function "remembers" the variables from its outer scope, even after the outer function has finished executing.

Closures allow:

- Data privacy (encapsulation)
- Maintaining state in asynchronous operations

---

## 💡 Key Points

- Inner functions **keep access** to outer function variables.
- Used in callbacks, event handlers, and functional programming.

---

## 🔥 Example

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  };
}

const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2
```

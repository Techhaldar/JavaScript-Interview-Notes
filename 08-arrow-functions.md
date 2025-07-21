# What are Arrow Functions and how do they differ from regular functions?

---

## ✅ Explanation

Arrow functions are a **short syntax** for writing functions, introduced in ES6.  
They **do not have their own `this`, arguments, or super**, making them ideal for callbacks.

---

### 🆚 Differences from Regular Functions

| Feature            | Arrow Function         | Regular Function          |
| ------------------ | ---------------------- | ------------------------- |
| `this` binding     | Lexical (parent scope) | Dynamic (depends on call) |
| `arguments` object | Not available          | Available                 |
| Syntax             | Concise                | Verbose                   |

---

## 🔥 Example

```javascript
// Regular Function
function sum(a, b) {
  return a + b;
}

// Arrow Function
const sumArrow = (a, b) => a + b;

console.log(sum(5, 10)); // 15
console.log(sumArrow(5, 10)); // 15
```

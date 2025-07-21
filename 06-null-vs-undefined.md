# What is the difference between null and undefined?

---

## ✅ Explanation

Both `null` and `undefined` represent **absence of value** in JavaScript, but they are used differently:

- **`undefined`**: A variable is declared but **not assigned** a value.
- **`null`**: A variable is explicitly assigned "no value."

---

## 💡 Key Differences

| Feature            | `undefined`                     | `null`                 |
| ------------------ | ------------------------------- | ---------------------- |
| Meaning            | Variable declared, not assigned | Explicitly no value    |
| Type               | `undefined`                     | `object` (weird quirk) |
| Default assignment | Automatic by JS                 | Must assign manually   |

---

## 🔥 Example

```javascript
let a;
console.log(a); // undefined (not assigned)

let b = null;
console.log(b); // null (assigned no value)

console.log(typeof a); // "undefined"
console.log(typeof b); // "object" (legacy quirk)
```

# What is the difference between == and === in JavaScript?

---

## ✅ Explanation

JavaScript provides two equality operators:

- `==` (loose equality): compares values **after type coercion**.
- `===` (strict equality): compares **values and types** without coercion.

---

## 💡 Key Points

| Operator | Compares       | Type Coercion? | Example             |
| -------- | -------------- | -------------- | ------------------- |
| `==`     | Value only     | Yes            | `"5" == 5` → true   |
| `===`    | Value and Type | No             | `"5" === 5` → false |

---

## 🔥 Example

```javascript
console.log(5 == "5"); // true (coerced)
console.log(5 === "5"); // false (different types)

console.log(null == undefined); // true
console.log(null === undefined); // false
```

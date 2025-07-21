# What are the different data types in JavaScript?

---

## ✅ Explanation

JavaScript has a total of **8 data types** as of ES6, divided into **primitive** and **non-primitive (reference)** types.

---

### 🟢 1. Primitive Data Types

Primitive types are immutable and stored directly in memory.

| Data Type   | Description                        | Example                               |
| ----------- | ---------------------------------- | ------------------------------------- |
| `Number`    | Represents numeric values          | `let a = 42;`                         |
| `String`    | Sequence of characters             | `let str = "Hello";`                  |
| `Boolean`   | True or False                      | `let isTrue = true;`                  |
| `Undefined` | Variable declared but not assigned | `let x; console.log(x); // undefined` |
| `Null`      | Represents intentional "no value"  | `let y = null;`                       |
| `BigInt`    | For large integers beyond `Number` | `let big = 123n;`                     |
| `Symbol`    | Unique and immutable identifier    | `let sym = Symbol('id');`             |

---

### 🟣 2. Non-Primitive Data Type (Reference Type)

| Data Type | Description                   | Example                      |
| --------- | ----------------------------- | ---------------------------- |
| `Object`  | Collection of key-value pairs | `let obj = {name: "Ratin"};` |

---

## 🔥 Example: Checking Data Types

```javascript
let a = 123; // Number
let b = "JavaScript"; // String
let c = true; // Boolean
let d; // Undefined
let e = null; // Null
let f = 1234567890123456789n; // BigInt
let g = Symbol("id"); // Symbol
let h = { lang: "JS" }; // Object

console.log(typeof a); // number
console.log(typeof b); // string
console.log(typeof c); // boolean
console.log(typeof d); // undefined
console.log(typeof e); // object (quirk: historical bug)
console.log(typeof f); // bigint
console.log(typeof g); // symbol
console.log(typeof h); // object
```

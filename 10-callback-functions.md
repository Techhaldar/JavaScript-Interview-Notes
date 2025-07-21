# What is a Callback Function in JavaScript?

---

## ✅ Explanation

A **callback function** is a function passed as an argument to another function, which is then **executed later** (after an operation completes).

They are widely used in:

- Event handling
- Asynchronous programming
- Functional programming

---

## 💡 Key Points

- Functions are first-class citizens in JavaScript.
- Callbacks enable **non-blocking code**.

---

## 🔥 Example: Asynchronous Callback

```javascript
function greet(name, callback) {
  console.log("Hi, " + name);
  callback();
}

function sayBye() {
  console.log("Bye!");
}

greet("Ratin", sayBye);
```

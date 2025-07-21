# What are Promises in JavaScript?

---

## ✅ Explanation

A **Promise** in JavaScript is an object that represents the **eventual completion or failure** of an asynchronous operation.

It acts as a placeholder for a value that might not be available yet but will be resolved in the future.

---

### 📦 Why Promises?

Before promises, JavaScript developers used **callbacks** for async operations, which often led to "callback hell" (nested callbacks that are hard to manage).  
Promises solve this by providing a **cleaner and more readable approach**.

---

### 📖 States of a Promise

A Promise can be in one of three states:

1. **Pending**: Initial state, neither fulfilled nor rejected.
2. **Fulfilled**: Operation completed successfully.
3. **Rejected**: Operation failed.

---

## 🔥 Example: Creating and Using a Promise

```javascript
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    let success = true; // Change to false to see rejection
    if (success) {
      resolve("✅ Promise fulfilled!");
    } else {
      reject("❌ Promise rejected!");
    }
  }, 2000);
});

// Consuming the Promise
myPromise
  .then((message) => {
    console.log(message); // Runs if resolved
  })
  .catch((error) => {
    console.error(error); // Runs if rejected
  })
  .finally(() => {
    console.log("Promise settled (either fulfilled or rejected)");
  });
```

## 🟢 Example: Chaining Promises

---

```javascript
fetch("https://api.example.com/data")
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((err) => console.error("Error fetching data:", err));
```

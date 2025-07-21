# What is async/await in JavaScript?

---

## ✅ Explanation

`async` and `await` are **syntactic sugar** introduced in ES2017 (ES8) to make working with Promises easier and code more **readable**.

They allow you to write asynchronous code that looks synchronous, avoiding the "callback hell" or chaining `.then()` in Promises.

---

### 🟢 What is `async`?

- A function declared with `async` always returns a **Promise**.
- If a non-promise value is returned, JavaScript automatically wraps it in a Promise.

```javascript
async function greet() {
  return "Hello!";
}

greet().then(console.log); // Output: Hello!
```

### 🟣 What is `await`?

```text
`await` pauses the execution of an `async` function until the Promise settles (fulfilled or rejected).

It can only be used inside async functions.
```

### 🔥 Example: Using async/await

```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("✅ Data fetched successfully!");
    }, 2000);
  });
}

async function getData() {
  console.log("Fetching data...");
  const result = await fetchData();
  console.log(result);
}

getData();
```

```javascript
Fetching data...
✅ Data fetched successfully!
```

### 💡 Key Points

```text
✅ `async` functions always return Promises.

✅ `await` can only be used in `async` functions.

✅ Makes asynchronous code easier to read and maintain.

✅ Errors can be handled using `try...catch`.


```

### 🔥 Example: Error Handling

```javascript
async function fetchWithError() {
  try {
    let response = await Promise.reject("❌ Failed to fetch data!");
    console.log(response);
  } catch (error) {
    console.error("Error:", error);
  }
}

fetchWithError();
```

```javascript
Error: ❌ Failed to fetch data!
```

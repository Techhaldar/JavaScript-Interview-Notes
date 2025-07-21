# What is the Event Loop in JavaScript?

---

## ✅ Explanation

JavaScript is a **single-threaded** language, meaning it can only execute one task at a time. But it needs to handle **asynchronous operations** like API calls, timers, and DOM events without blocking the main thread.

This is where the **Event Loop** comes in.

The Event Loop allows JavaScript to:

- Execute synchronous code first.
- Handle asynchronous callbacks after the main stack is clear.

Think of it as a **traffic controller** for your code.

---

### 🌀 How It Works

1. **Call Stack**
   - Holds all the functions to be executed.
2. **Web APIs**
   - Browser-provided APIs (like `setTimeout`, `fetch`) handle async tasks outside JS.
3. **Callback Queue (Task Queue)**
   - When async tasks are complete, their callbacks are queued here.
4. **Event Loop**
   - Continuously checks: If the Call Stack is empty, it pushes queued callbacks to the stack.

---

### 🖇 Visual Flow

```text
Call Stack ⇆ Event Loop ⇆ Callback Queue
          ⇅            ↑
       Web APIs (Async Tasks)
```

## 🔥 Example: Event Loop in Action

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Inside setTimeout");
}, 0);

console.log("End");
```

# Is JavaScript a compiled or interpreted language?

---

## ✅ Explanation

Traditionally, JavaScript has been considered an **interpreted language** because it was executed line by line by the browser’s JavaScript engine. Early JavaScript engines would directly interpret the source code without any prior compilation step.

However, **modern JavaScript engines** (like Google Chrome’s V8, Firefox’s SpiderMonkey, and Safari’s JavaScriptCore) now use a technique called **Just-In-Time (JIT) Compilation**. This means JavaScript is:

➡️ **Not purely interpreted**  
➡️ **Not purely compiled**  
It’s a **hybrid** of both.

---

### 🔥 How Does It Work? (JIT Compilation)

1. The **JavaScript engine** first parses the source code and creates an Abstract Syntax Tree (AST).
2. It converts the AST into **bytecode** using an interpreter.
3. Frequently executed code (hot code) is detected and optimized into **machine code** using a JIT compiler for faster execution.

This approach allows:
✅ Faster startup (thanks to interpretation)  
✅ Faster execution over time (thanks to compilation)

---

## 💡 Key Points

- ✅ **Old engines** → Purely interpreted (line by line).
- ✅ **Modern engines** → Use JIT compilation for performance.
- ✅ **JIT (Just-In-Time)** → Compiles code _at runtime_ to machine code.
- ✅ JavaScript is still considered a **high-level scripting language**.

---

## 🔥 Example: Why Compilation Matters

Modern browsers optimize repeated tasks:

```javascript
function sum(a, b) {
  return a + b;
}

for (let i = 0; i < 1_000_000; i++) {
  sum(5, 10); // This gets optimized after being run many times
}
```

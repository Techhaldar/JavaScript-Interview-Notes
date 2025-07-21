## ✅ Explanation

In JavaScript, `var`, `let`, and `const` are used to declare variables. They differ in **scope**, **hoisting**, and **mutability**:

### 1️⃣ `var`

- Declared variables are **function-scoped** (visible throughout the function).
- Hoisted to the top of their scope but initialized as `undefined`.
- Can be redeclared and reassigned.

### 2️⃣ `let`

- Introduced in ES6.
- **Block-scoped** (visible only within `{}` block).
- Hoisted but not initialized (Temporal Dead Zone).
- Can be reassigned but **cannot be redeclared** in the same scope.

### 3️⃣ `const`

- Like `let`, **block-scoped**.
- Must be **initialized at declaration**.
- Cannot be reassigned (but object contents can change).

---

## 💡 Key Points

| Feature       | `var`           | `let`     | `const`   |
| ------------- | --------------- | --------- | --------- |
| Scope         | Function        | Block     | Block     |
| Hoisting      | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |
| Redeclaration | Yes             | No        | No        |
| Reassignment  | Yes             | Yes       | No        |

---

## 🔥 Example

```javascript
function testVarLetConst() {
  if (true) {
    var x = 10;
    let y = 20;
    const z = 30;
  }
  console.log(x); // 10 (function-scoped)
  console.log(y); // ReferenceError (block-scoped)
  console.log(z); // ReferenceError (block-scoped)
}
testVarLetConst();
```

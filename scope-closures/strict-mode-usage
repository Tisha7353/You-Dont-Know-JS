# JavaScript Strict Mode

`"use strict"` in JavaScript is like turning on **“safety mode”** for your code. It enforces stricter parsing and error-checking to prevent common mistakes.

---

## 1️⃣ Prevents Accidental Globals

Without strict mode:

```javascript
function foo() {
    x = 10; // Oops! Creates a global variable
}
foo();
console.log(x); // 10 (accidental global)
```

With strict mode:

```javascript
"use strict";
function foo() {
    x = 10; // ReferenceError: x is not defined
}
```

✅ Forces you to declare variables (`let`, `const`, or `var`).

---

## 2️⃣ Throws Errors for Silent Failures

Strict mode converts some silent errors into **throwing errors**. Examples:

* Assigning to **read-only properties**:

```javascript
"use strict";
const obj = {};
Object.defineProperty(obj, "x", { value: 10, writable: false });
obj.x = 20; // TypeError
```

* Deleting **undeletable properties**:

```javascript
"use strict";
delete Object.prototype; // TypeError
```

* Assigning to **non-existing variables**:

```javascript
"use strict";
y = 10; // ReferenceError
```

---

## 3️⃣ Disallows Duplicate Parameter Names

Without strict mode, JS allows duplicate parameter names:

```javascript
function sum(a, a, c) { // allowed in non-strict
    return a + a + c;
}
```

With strict mode:

```javascript
"use strict";
function sum(a, a, c) { // SyntaxError
    return a + a + c;
}
```

✅ Helps avoid **confusing bugs**.

---

## 4️⃣ Makes `this` in Functions Safer

Non-strict mode:

```javascript
function foo() {
    console.log(this);
}
foo(); // window (global object)
```

Strict mode:

```javascript
"use strict";
function foo() {
    console.log(this);
}
foo(); // undefined
```

✅ Prevents accidental modification of the global object.

---

## 5️⃣ Eliminates `with` Statement

```javascript
with (obj) {
    x = 10; // ambiguous
}
```

Strict mode **disallows `with`**, improving clarity and performance.

---

## 6️⃣ Reserved Future Keywords

```javascript
"use strict";
let public = 10;  // SyntaxError
let private = 20; // SyntaxError
```

✅ Ensures your code is future-proof.

---

## 7️⃣ Easier Debugging

* Errors are thrown **immediately** instead of failing silently.
* Makes your code **predictable** and **safer to maintain**.

---

## 8️⃣ Makes Code Optimization Better

Strict mode allows JS engines to **optimize code better** by removing ambiguities like accidental globals or `with` statements.

---

## ✅ Summary Table

| Feature                             | Non-Strict Mode | Strict Mode    |
| ----------------------------------- | --------------- | -------------- |
| Undeclared variable assignment      | Creates global  | ReferenceError |
| Duplicate parameters                | Allowed         | SyntaxError    |
| `this` in functions                 | Global object   | undefined      |
| Silent failures (read-only, delete) | Ignored         | Throws Error   |
| `with` statement                    | Allowed         | Disallowed     |
| Reserved keywords                   | Ignored         | SyntaxError    |

---

## 💡 Recommendation

Always start your JS files or functions with:

```javascript
"use strict";
```

It’s especially useful in **large projects, libraries, or when you want fewer bugs**.

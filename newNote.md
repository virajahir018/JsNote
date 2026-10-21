# JavaScript Variables: `var`, `let`, and `const`

## Table of Contents

* [1. Introduction](#1-introduction)
* [2. Core Differences](#2-core-differences-var-let-and-const)

  * [2.1 Scope](#21-scope)
  * [2.2 Redeclaration and Re-assignment](#22-redeclaration-and-re-assignment)
  * [2.3 Hoisting](#23-hoisting)
* [3. Real-World Examples](#3-real-world-examples-and-use-cases)
* [4. Objects and Arrays with `const`](#4-special-case-objects-and-arrays-with-const)
* [5. Function Scope vs. Block Scope](#5-function-scope-vs-block-scope)
* [6. Quick Revision](#6-quick-revision)

---

## 1. Introduction

JavaScript mein variables ko data store karne wale containers ki tarah samajh sakte hain.

ES5, yaani purane JavaScript mein, variable declare karne ka main tareeqa `var` keyword tha. Lekin 2015 mein ES6 (ECMAScript 2015) introduce hua, jismein do naye keywords aaye: `let` aur `const`.

Modern JavaScript development mein in teeno keywords ka sahi use karna important hai, kyunki isse code readable, predictable aur bugs se bachne mein madad milti hai.

## 2. Core Differences: `var`, `let`, and `const`

In teeno keywords ke beech differences ko mainly teen parameters se samajh sakte hain:

1. Scope
2. Redeclaration and Re-assignment
3. Hoisting

### 2.1 Scope

**Scope** ka matlab hai ki code ke kis hisse se kisi variable ko access kiya ja sakta hai.

* **`var` — Function-scoped:** Agar `var` ko function ke andar declare kiya jaye, to woh us function ke andar accessible hota hai. `if` ya loop jaise block ke andar declare karne par bhi woh block ke bahar accessible ho sakta hai.
* **`let` and `const` — Block-scoped:** Agar inhein `{}` block, jaise `if` ya `for` loop ke andar declare kiya jaye, to ye us block ke bahar accessible nahi hote.

**Example:**

```js
if (true) {
  var a = 10;
  let b = 20;
  const c = 30;
}

console.log(a); // 10

// console.log(b); // ReferenceError
// console.log(c); // ReferenceError
```

### 2.2 Redeclaration and Re-assignment

| Feature                        | `var`    | `let`       | `const`     |
| ------------------------------ | -------- | ----------- | ----------- |
| Same scope mein redeclare      | Allowed  | Not allowed | Not allowed |
| Value re-assign karna          | Allowed  | Allowed     | Not allowed |
| Declaration ke waqt value dena | Optional | Optional    | Required    |

**Example:**

```js
// var
var score = 10;
var score = 20; // Allowed
score = 30;     // Allowed

// let
let age = 18;
// let age = 19; // SyntaxError
age = 19;        // Allowed

// const
const country = "India";
// country = "USA"; // TypeError
```

`const` ko declare karte waqt initialize karna zaroori hai.

```js
const city = "Ahmedabad"; // Correct

// const state; // SyntaxError
```

### 2.3 Hoisting

JavaScript mein declarations execution se pehle process hoti hain. Is behavior ko **hoisting** kaha jata hai.

* **`var`:** Hoist hota hai aur `undefined` se initialize hota hai.
* **`let` and `const`:** Hoist hote hain, lekin declaration se pehle initialize nahi hote. Declaration se peh

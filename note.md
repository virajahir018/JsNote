# JavaScript Revision Notes

## 1. What is JavaScript?

### English

JavaScript is a **high-level, dynamically typed programming language** mainly used to make web applications interactive. It can run in browsers and also outside browsers using runtimes such as Node.js.

### Hindi

JavaScript ek programming language hai jo websites aur web applications ko **interactive aur dynamic** banane ke liye use hoti hai.

Example:

```js
console.log("Hello JavaScript");
```

---

# 2. Variables

### English

Variables are used to store data values in a program.

JavaScript provides three ways to declare variables:

* `var`
* `let`
* `const`

### Hindi

Variable ka use data ko store karne ke liye hota hai.

```js
let name = "Viraj Ahir";
const age = 22;
var city = "Gujarat";
```

---

# 3. `var`, `let`, and `const`

| Keyword | Reassign | Redeclare | Scope    |
| ------- | -------- | --------- | -------- |
| `var`   | Yes      | Yes       | Function |
| `let`   | Yes      | No        | Block    |
| `const` | No       | No        | Block    |

### English

`let` and `const` are generally preferred in modern JavaScript because they provide block scope.

### Hindi

Modern JavaScript me generally `let` aur `const` use kiye jate hain.

---

# 4. Data Types

### English

JavaScript has primitive and non-primitive/reference data types.

### Primitive Types

```text
String
Number
Boolean
Undefined
Null
BigInt
Symbol
```

### Reference Types

```text
Object
Array
Function
```

### Example

```js
let name = "Viraj Ahir"; // String
let age = 22;            // Number
let isAdmin = false;     // Boolean
let value;               // Undefined
let data = null;         // Null

let user = {
  name: "Viraj Ahir"
};                       // Object
```

### Hindi

Data type batata hai ki variable me kis type ka data store hai.

---

# 5. String

### English

A String is a sequence of characters used to represent text.

```js
let name = "Viraj Ahir";
```

### Hindi

String ka use text store karne ke liye hota hai.

---

# 6. Number

### English

The Number type represents numeric values, including integers and floating-point numbers.

```js
let age = 22;
let price = 599.99;
```

### Hindi

Number ka use numerical values ke liye hota hai.

---

# 7. Boolean

### English

Boolean has only two values:

```js
true
false
```

Example:

```js
let isLoggedIn = true;
```

### Hindi

Boolean ka use yes/no ya true/false type values ke liye hota hai.

---

# 8. Undefined

### English

A variable has the value `undefined` when it has been declared but no value has been assigned.

```js
let name;

console.log(name);
```

Output:

```text
undefined
```

### Hindi

Jab variable declare ho lekin usme value assign na ho, to uski value `undefined` hoti hai.

---

# 9. Null

### English

`null` represents an intentional absence of a value.

```js
let user = null;
```

### Hindi

`null` ka matlab hai intentionally koi value nahi hai.

---

# 10. Object

### English

An object is a collection of properties stored as key-value pairs.

```js
const user = {
  name: "Viraj Ahir",
  age: 22
};
```

### Hindi

Object me data **key-value pair** ke form me store hota hai.

---

# 11. Array

### English

An array is an ordered collection of values.

```js
const fruits = ["Apple", "Mango", "Banana"];
```

### Hindi

Array me multiple values ko ek variable me store kar sakte hain.

---

# 12. Function

### English

A function is a reusable block of code designed to perform a specific task.

```js
function add(a, b) {
  return a + b;
}

console.log(add(10, 20));
```

### Hindi

Function reusable code ka block hota hai jo ek specific task perform karta hai.

---

# 13. Arrow Function

### English

An arrow function is a shorter syntax for writing functions.

```js
const add = (a, b) => {
  return a + b;
};
```

Short form:

```js
const add = (a, b) => a + b;
```

### Hindi

Arrow function function likhne ka short aur modern syntax hai.

---

# 14. Parameters and Arguments

### English

Parameters are variables defined in a function declaration.

Arguments are the actual values passed when calling the function.

```js
function greet(name) {
  console.log(name);
}

greet("Viraj");
```

Here:

* `name` → Parameter
* `"Viraj"` → Argument

### Hindi

Function banate waqt jo variable dete hain wo **parameter** hota hai.

Function call karte waqt jo actual value dete hain wo **argument** hoti hai.

---

# 15. Return

### English

The `return` statement sends a value back from a function.

```js
function add(a, b) {
  return a + b;
}
```

### Hindi

`return` function se value bahar bhejne ke liye use hota hai.

---

# 16. Operators

### Arithmetic Operators

```text
+   Addition
-   Subtraction
*   Multiplication
/   Division
%   Remainder
**  Exponentiation
```

### Comparison Operators

```text
== 
===
!=
!==
>
<
>=
<=
```

### Logical Operators

```text
&&  AND
||  OR
!   NOT
```

---

# 17. `==` vs `===`

### English

`==` performs loose equality comparison and may perform type conversion.

`===` performs strict equality comparison and checks both value and type.

```js
5 == "5";   // true
5 === "5";  // false
```

### Hindi

`==` value compare karta hai aur type conversion kar sakta hai.

`===` value aur data type dono check karta hai.

**Modern JavaScript me generally `===` prefer kiya jata hai.**

---

# 18. Conditional Statements

### English

Conditional statements execute different code depending on a condition.

```js
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

### Hindi

Condition ke basis par different code execute karne ke liye `if`, `else if`, aur `else` use hote hain.

---

# 19. Ternary Operator

### English

The ternary operator is a short way to write a simple `if...else`.

```js
let result = age >= 18 ? "Adult" : "Minor";
```

### Hindi

Simple condition ke liye ternary operator `if...else` ka short form hai.

---

# 20. Switch

### English

`switch` is used when we need to compare one value against multiple possible cases.

```js
switch (day) {
  case "Monday":
    console.log("Start");
    break;

  case "Sunday":
    console.log("Holiday");
    break;

  default:
    console.log("Other day");
}
```

### Hindi

Ek value ko multiple possible cases ke saath compare karne ke liye `switch` use hota hai.

---

# 21. Loops

### English

Loops are used to execute a block of code repeatedly.

Common loops:

* `for`
* `while`
* `do...while`
* `for...of`
* `for...in`

### Example

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### Hindi

Same code ko repeatedly run karne ke liye loops use hote hain.

---

# 22. `for...of`

### English

`for...of` iterates over the values of an iterable such as an array.

```js
const fruits = ["Apple", "Mango"];

for (const fruit of fruits) {
  console.log(fruit);
}
```

### Hindi

Array ki values ko one-by-one access karne ke liye `for...of` useful hai.

---

# 23. `for...in`

### English

`for...in` iterates over enumerable property keys of an object.

```js
const user = {
  name: "Viraj",
  age: 22
};

for (const key in user) {
  console.log(key);
}
```

### Hindi

Object ki keys ko iterate karne ke liye `for...in` use kiya ja sakta hai.

---

# 24. Array Methods

Important array methods:

```text
map()
filter()
find()
findIndex()
forEach()
reduce()
some()
every()
includes()
push()
pop()
shift()
unshift()
slice()
splice()
```

---

# 25. `map()`

### English

`map()` creates a new array by transforming each element of the original array.

```js
const numbers = [1, 2, 3];

const result = numbers.map((num) => num * 2);

console.log(result);
```

Output:

```text
[2, 4, 6]
```

### Hindi

`map()` har element par operation perform karke **new array** return karta hai.

---

# 26. `filter()`

### English

`filter()` creates a new array containing elements that satisfy a condition.

```js
const numbers = [1, 2, 3, 4];

const result = numbers.filter((num) => num > 2);

console.log(result);
```

Output:

```text
[3, 4]
```

### Hindi

`filter()` condition ke according elements select karke new array return karta hai.

---

# 27. `find()`

### English

`find()` returns the first element that satisfies the condition.

```js
const users = [
  { id: 1, name: "A" },
  { id: 2, name: "B" }
];

const user = users.find((item) => item.id === 2);
```

### Hindi

`find()` condition satisfy karne wala **first element** return karta hai.

---

# 28. `forEach()`

### English

`forEach()` executes a function once for each array element.

```js
const numbers = [1, 2, 3];

numbers.forEach((num) => {
  console.log(num);
});
```

### Hindi

Array ke har element par function execute karne ke liye `forEach()` use hota hai.

> `forEach()` normally new array return nahi karta.

---

# 29. `reduce()`

### English

`reduce()` processes array elements and reduces them to a single accumulated result.

```js
const numbers = [10, 20, 30];

const total = numbers.reduce((sum, num) => {
  return sum + num;
}, 0);

console.log(total);
```

Output:

```text
60
```

### Hindi

`reduce()` multiple values ko process karke generally ek single result banane ke liye use hota hai.

---

# 30. Destructuring

### English

Destructuring allows us to extract values from arrays or properties from objects into variables.

### Object

```js
const user = {
  name: "Viraj",
  age: 22
};

const { name, age } = user;
```

### Array

```js
const colors = ["Red", "Blue"];

const [first, second] = colors;
```

### Hindi

Destructuring se object ki properties ya array ki values ko easily variables me extract kar sakte hain.

---

# 31. Spread Operator

### English

The spread operator `...` expands elements of an iterable or properties of an object.

```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];

console.log(arr2);
```

### Hindi

Spread operator `...` existing array/object ke elements ya properties ko expand/copy karne ke liye use hota hai.

---

# 32. Rest Parameter

### English

The rest parameter `...` collects multiple function arguments into an array.

```js
function add(...numbers) {
  return numbers;
}

console.log(add(10, 20, 30));
```

### Hindi

Rest parameter multiple arguments ko ek array me collect karta hai.

---

# 33. Template Literals

### English

Template literals use backticks and allow embedded expressions using `${}`.

```js
const name = "Viraj";
const age = 22;

console.log(`My name is ${name} and I am ${age} years old.`);
```

### Hindi

Template literals string ke andar variables ya expressions easily use karne dete hain.

---

# 34. Scope

### English

Scope determines where a variable can be accessed.

Main types:

* Global Scope
* Function Scope
* Block Scope

### Hindi

Scope batata hai ki variable ko program ke kis part me access kiya ja sakta hai.

---

# 35. Hoisting

### English

Hoisting is JavaScript's behavior where declarations are processed before the code in their scope is executed.

Example:

```js
console.log(a);

var a = 10;
```

`var` declaration is hoisted, but its value is assigned later.

### Important

`let` and `const` are also hoisted in a technical sense, but they cannot be accessed before their declaration because of the **Temporal Dead Zone (TDZ)**.

### Hindi

Hoisting me JavaScript declarations ko execution se pehle process karta hai.

---

# 36. Closure

### English

A closure occurs when a function remembers and can access variables from its outer lexical scope even after the outer function has finished executing.

```js
function outer() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const counter = outer();

console.log(counter());
console.log(counter());
```

Output:

```text
1
2
```

### Hindi

Closure me inner function apne outer function ke variables ko remember karta hai, even after outer function execute ho chuka ho.

---

# 37. Callback Function

### English

A callback is a function passed to another function to be called later.

```js
function greet(name, callback) {
  console.log("Hello " + name);
  callback();
}

greet("Viraj", () => {
  console.log("Welcome");
});
```

### Hindi

Jab ek function ko doosre function ke argument ke roop me pass karte hain aur baad me execute karte hain, use callback kehte hain.

---

# 38. Synchronous vs Asynchronous

### Synchronous

### English

Synchronous code executes operations sequentially and waits for the current operation to complete before moving forward.

### Hindi

Synchronous code me ek operation complete hone ke baad next operation execute hota hai.

### Asynchronous

### English

Asynchronous operations allow other JavaScript work to continue while waiting for an operation to complete.

### Hindi

Asynchronous operation ke wait ke time JavaScript other work continue kar sakti hai.

---

# 39. Promise

### English

A Promise represents the eventual completion or failure of an asynchronous operation.

Promise has three common states:

```text
Pending
Fulfilled
Rejected
```

Example:

```js
const promise = new Promise((resolve, reject) => {
  resolve("Success");
});
```

### Hindi

Promise asynchronous operation ke future result ko represent karta hai.

---

# 40. async / await

### English

`async/await` provides a cleaner syntax for working with Promises.

```js
async function getData() {
  const response = await fetch("https://example.com");
  const data = await response.json();

  console.log(data);
}
```

### Hindi

`async/await` Promise-based asynchronous code ko readable aur easy banata hai.

---

# 41. try...catch

### English

`try...catch` is used to handle errors.

```js
try {
  // risky code
} catch (error) {
  console.log(error);
}
```

### Hindi

Runtime errors ko handle karne ke liye `try...catch` use hota hai.

---

# 42. DOM

### English

DOM stands for **Document Object Model**. It represents an HTML document as a tree of objects that JavaScript can read and manipulate in the browser.

### Hindi

DOM browser ke HTML document ka object-based representation hai.

JavaScript se hum DOM ke through:

* HTML change
* CSS change
* Elements create/remove
* Events handle

kar sakte hain.

---

# 43. Event

### English

An event is an action or occurrence detected by the browser, such as a click, input, submit, or key press.

```js
button.addEventListener("click", () => {
  console.log("Button clicked");
});
```

### Hindi

Event user ya browser ki action hoti hai, jaise:

* Click
* Input
* Submit
* Key press

---

# 44. Event Listener

### English

`addEventListener()` attaches a function that runs when a specified event occurs.

```js
button.addEventListener("click", handleClick);
```

### Hindi

`addEventListener()` kisi element par event ko listen karne ke liye use hota hai.

---

# 45. Local Storage

### English

`localStorage` allows a browser to store string data that persists across browser sessions.

```js
localStorage.setItem("name", "Viraj");

const name = localStorage.getItem("name");
```

### Hindi

`localStorage` browser me data store karta hai aur normally browser sessions ke across data persist karta hai.

---

# 46. JSON

### English

JSON stands for **JavaScript Object Notation**. It is a text format commonly used for exchanging structured data.

### Object to JSON

```js
JSON.stringify(user);
```

### JSON to Object

```js
JSON.parse(data);
```

### Hindi

JSON ek text-based data format hai jo APIs me data exchange ke liye commonly use hota hai.

---

# 47. `typeof`

### English

`typeof` is an operator used to determine the type of a value.

```js
typeof "Hello"; // "string"
typeof 10;      // "number"
typeof true;    // "boolean"
```

### Hindi

`typeof` kisi value ka data type check karne ke liye use hota hai.

---

# 48. Optional Chaining `?.`

### English

Optional chaining allows us to safely access nested properties without throwing an error when an intermediate value is `null` or `undefined`.

```js
const city = user?.address?.city;
```

### Hindi

`?.` ka use nested property safely access karne ke liye hota hai.

---

# 49. Nullish Coalescing `??`

### English

The nullish coalescing operator returns the right-hand value only when the left-hand value is `null` or `undefined`.

```js
const name = userName ?? "Guest";
```

### Hindi

Agar left side ki value `null` ya `undefined` hai tab right side ki default value milegi.

---

# 50. Modules

### English

Modules allow JavaScript code to be divided into separate reusable files.

### CommonJS

```js
module.exports = user;
```

```js
const user = require("./user");
```

### ESM

```js
export default user;
```

```js
import user from "./user.js";
```

### Hindi

Modules code ko separate files me divide karke reusable aur maintainable banate hain.

---

# 51. `this` Keyword

### English

`this` refers to a context-dependent value determined by how a function is called.

Example:

```js
const user = {
  name: "Viraj",

  greet() {
    console.log(this.name);
  }
};

user.greet();
```

### Hindi

`this` ki value function ko kaise call kiya gaya hai, us context par depend karti hai.

---

# 52. Class

### English

A class is a syntax for creating objects and defining shared behavior.

```js
class User {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello ${this.name}`);
  }
}

const user = new User("Viraj");

user.greet();
```

### Hindi

Class objects create karne aur unka common structure/behavior define karne ka syntax hai.

---

# 53. Constructor

### English

A constructor is a special method in a class that runs when a new object is created.

```js
class User {
  constructor(name) {
    this.name = name;
  }
}
```

### Hindi

`constructor()` object create hote time automatically execute hota hai.

---

# 54. Error Handling

### English

JavaScript provides mechanisms such as `try...catch`, `throw`, and `finally` for handling errors.

```js
try {
  throw new Error("Something went wrong");
} catch (error) {
  console.log(error.message);
}
```

### Hindi

Errors ko handle karne ke liye `try`, `catch`, `throw`, aur `finally` use kar sakte hain.

---

# 55. `NaN`

### English

`NaN` stands for **Not-a-Number**. It represents a value that is not a valid numeric result.

```js
console.log(Number("hello"));
```

Output:

```text
NaN
```

Check:

```js
Number.isNaN(value);
```

### Hindi

`NaN` ka matlab **Not-a-Number** hai.

---

# 56. `Number.isInteger()`

### English

`Number.isInteger()` checks whether a value is an integer.

```js
Number.isInteger(10);   // true
Number.isInteger(10.5); // false
```

### Hindi

Ye check karta hai ki value integer hai ya nahi.

---

# 57. Truthy and Falsy

### English

In JavaScript, values are converted to boolean context as either truthy or falsy.

Common falsy values:

```text
false
0
-0
0n
""
null
undefined
NaN
```

Most other values are truthy.

### Hindi

Condition me kuch values `false` ki tarah behave karti hain, unhe falsy kehte hain.

---

# 58. `&&` and `||`

### AND `&&`

Both conditions need to be truthy.

```js
age >= 18 && isLoggedIn
```

### OR `||`

At least one condition needs to be truthy.

```js
isAdmin || isOwner
```

### Hindi

`&&` ka matlab **AND** aur `||` ka matlab **OR** hota hai.

---

# 59. Short-Circuiting

### English

Logical operators can stop evaluating as soon as the final result is known.

Example:

```js
const name = user && user.name;
```

Modern JavaScript often uses:

```js
const name = user?.name;
```

### Hindi

Logical operators condition ke result ke according unnecessary expression ko evaluate karna skip kar sakte hain.

---

# 60. Shallow Copy

### English

A shallow

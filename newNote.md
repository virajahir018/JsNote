# JavaScript: var, let, and const

## 1. Introduction & Hook (30–45 Seconds)

"Sir, JavaScript mein variables ko hum data store karne ke containers ki tarah dekhte hain. Agar hum ES5 yaani puraane JavaScript ki baat karein, to hamare paas variables declare karne ka sirf ek tareeqa tha—`var` keyword.

Lekin 2015 mein jab ES6 (ECMAScript 2015) introduce hua, to JavaScript ke scope aur memory management ko behtar banane ke liye do naye keywords laye gaye—`let` aur `const`. Aaj ke time par modern JavaScript development mein in teeno ka sahi use karna code ki efficiency aur bug-free execution ke liye bohot zaroori hai."

## 2. Core Comparison: The Three Pillars (2 Minutes)

"In teeno keywords ke beech ke differences ko hum mainly teen parameters par samajh sakte hain: Scope, Redeclaration & Re-assignment, aur Hoisting."

### Pillar 1: Scope (Kahan tak access kar sakte hain?)

- `var` Function-scoped hota hai. Iska matlab agar humne `var` ko kisi function ke andar declare kiya hai, to wo sirf us function mein chalega. Lekin agar use kisi `if` block ya loop ke andar declare kiya, to wo block ke bahar bhi access ho jata hai.
- Wahi dusri taraf, `let` aur `const` Block-scoped hote hain. Agar inhein kisi bhi curly braces `{}` (jaise loop ya if-else) ke andar likha jaye, to ye uske bahar access nahi kiye ja sakte. Yeh memory leak aur accidental variable override ko rokta hai.

### Pillar 2: Redeclaration & Re-assignment (Kya hum badal sakte hain?)

- `var` bohot zyada flexible hai—ise aap ek hi scope mein re-declare bhi kar sakte hain aur value re-assign bhi kar sakte hain. Is wajah se purani scripts mein bade bugs aate the.
- `let` mein aap value to badal (re-assign) sakte hain, lekin use dobara re-declare nahi kar sakte.
- `const` ka matlab hai Constant. Ismein na to aap re-declare kar sakte hain aur na hi value ko re-assign kar sakte hain. Isko declare karte waqt hi value dena compulsory hota hai.

### Pillar 3: Hoisting (Execution se pehle kya hota hai?)

- JavaScript mein hoisting ke dauran teeno keywords top par chale jaate hain, lekin unka behavior alag hota hai.
- `var` variables hoisted hote hain aur `undefined` se initialize ho jaate hain. Isliye agar aap declare karne se pehle unhein use karein, to error nahi aata, sirf `undefined` milta hai.
- `let` aur `const` bhi hoist hote hain, lekin wo initialize nahi hote. Wo ek Temporal Dead Zone (TDZ) mein chale jaate hain. Agar aap inhein declaration se pehle access karne ki koshish karenge, to JavaScript aapko ek `ReferenceError` dega, jo ki safe coding ke liye bohot achha hai.

## 3. Real-world Examples & Use Cases (1 Minute)

"Agar hum inke practical application ki baat karein, to real-world development mein hamari basic approach badal chuki hai:

- **`const` ka use:** Hum un values ke liye karte hain jo kabhi change nahi honi chahiye, jaise kisi API ka base URL (`const API_URL = '[https://example.com](https://example.com)'`), ya configuration settings, ya functions aur arrays ke references.
- **`let` ka use:** Hum tab karte hain jab humein pata ho ki variable ki value aage chalkar badlegi, jaise kisi `for` loop ka counter variable (`let i = 0`) ya fir kisi shopping cart ka total price jo product add hone par change hoga.
- **`var` ka use:** Aaj ke modern standard mein `var` ka use completely avoid kiya jata hai kyunki block scope na hone ki wajah se ye global window object ko pollute kar deta hai aur unexpected bugs create karta hai."

## 4. Special Edge Case: Objects and Arrays with Const (30 Seconds)

"Yahan par ek bohot interesting point aur interview ka favourite question aata hai—`const` ke sath Objects aur Arrays ka behavior.

Jab hum `const` se koi array ya object banate hain, to uska reference block ho jata hai, yaani hum use naya object re-assign nahi kar sakte. Lekin, hum us object ke andar ke properties ko ya array ke elements ko mutate (change/modify) kar sakte hain. Jaise `const user = { name: 'Amit' };` mein hum `user.name = 'Rahul';` bilkul kar sakte hain."

---

# What Is the Difference Between Function Scope and Block Scope?

## 1. Introduction & Hook (45 Seconds)

"Sir, JavaScript mein 'Scope' ka matlab hota hai Visibility and Accessibility of variables—yaani code ke kis hisse se hum kis variable ko access kar sakte hain aur kahan se nahi.

Agar hum JavaScript ki history ko dekhein, to ES5 tak JavaScript ke paas majorly sirf ek hi functional scope tha jise hum Function Scope kehte hain, jo ki `var` keyword se handle hota tha. Lekin modern JS framework aur complex applications mein variable leaks ko rokne ke liye, ES6 (2015) mein Block Scope introduce kiya gaya, jise handle karne ke liye `let` aur `const` keywords laye gaye. In dono ke beech ke difference ko samajhna clean aur bug-free code likhne ke liye bohot zaroori hai."

## 2. Core Differences: Deep Dive (2 Minutes)

"In dono scopes ko hum unke behavior, rules aur boundaries ke basis par differentiate kar sakte hain:"

### Concept 1: Function Scope (The Boundary of a Function)

- **Definition:** Jab bhi aap koi variable ek function ke andar declare karte hain, to wo variable us function ka local variable ban jata hai. Us variable ki life aur boundary sirf us function ke curly braces `{}` tak hi limited hoti hai.
- **Keyword:** Keyword `var` hamesha function scope ko follow karta hai.
- **Behavior:** Agar aapne ek function ke andar `var x = 10;` likha, to aap use function ke andar kahin bhi access kar sakte hain—chahe wo kisi conditional statement ke andar ho ya loop ke andar. Lekin jaise hi function khatam hota hai, wo variable memory se wipe out ho jata hai aur function ke bahar se access karne par `ReferenceError` deta hai.

### Concept 2: Block Scope (The Boundary of a Pair of Braces)

- **Definition:** JavaScript mein ek 'Block' ka matlab hota hai koi bhi code jo ek pair of curly braces `{}` ke andar likha ho. Jaise `if-else` statements, `for` loops, `while` loops, ya fir standalone curly braces.
- **Keywords:** Modern keywords `let` aur `const` strict block scope ko follow karte hain.
- **Behavior:** Agar aapne kisi `if` condition ya `for` loop ke andar `let y = 20;` declare kiya hai, to us `y` ki accessibility sirf aur sirf usi block ke andar rahegi. Jaise hi execution us block ke closing brace `}` ke bahar aayega, wo variable memory mein exist nahi karega.

## 3. The Big Catch: "Variable Bleeding / Leaking" (1 Minute)

"In dono ka sabse bada conflict tab aata hai jab hum ek block ke andar `var` ka use karte hain. Ise hum Variable Bleeding kehte hain.

Imagine kariye ek scenario: Humne ek function likha aur uske andar ek `if` block banaya. Agar hum us `if` block ke andar `var` variable declare karte hain, to chunki `var` block ko nahi pehchanta, wo us `if` block se leak (bleed) hokar pure function mein upar tak access ho jata hai.

Lekin agar hum usi `if` block ke andar `let` ya `const` use karenge, to wo block se bahar leak nahi hoga.

**Real-world disaster:** Puraane JavaScript mein jab hum `for (var i = 0; i < 5; i++)` likhte the, to loop khatam hone ke baad bhi `i` ki value loop ke bahar access ho jati thi, jo ki global memory ko pollute karti thi aur asynchronous code (jaise `setTimeout`) mein bade bugs create karti thi. Modern JS mein `let` use karne se yeh problem solve ho gayi hai."

# Variable Shadowing in JavaScript

## 1. Explain the Concept of Variable Shadowing with Examples

### Reason kya hai?

"Chunki `var` block scope ko nahi manta, isliye wo is block se leak hokar pure outer scope mein same variable point ko re-declare karne ki koshish karta hai. Lekin outer scope mein pehle se hi `let point` maujood hai, aur `let` strict re-declaration allow nahi karta. Is wajah se yeh illegal shadowing ho jati hai.

**Note:** Iska bilkul ulta allowed hai—yaani aap ek outer `var` variable ko inner `let` se bilkul shadow kar sakte hain, wo legally perfectly valid hai."

## 2. Matrix Summary for Quick Reference

Interviewer ke saamne clarity banaye rakhne ke liye:

| Outer Variable Type | Inner Variable Type | Status  | Result                                     |
| ------------------- | ------------------- | ------- | ------------------------------------------ |
| `let` / `const`     | `let` / `const`     | Legal   | Clean Shadowing works.                     |
| `var`               | `let` / `const`     | Legal   | Inner variable shadows outer `var`.        |
| `let` / `const`     | `var`               | Illegal | ❌ SyntaxError (Variable Leaking conflict). |

---

# What Is the Temporal Dead Zone (TDZ) and Which Variable Declarations Are Affected by It?

## 1. Example

```javascript
// ---- SCOPE STARTS HERE ----
// 1. Yeh 'age' variable ka Temporal Dead Zone (TDZ) hai.

console.log(name); // Output: undefined (Kyunki var par TDZ nahi lagta)
console.log(age);  // ❌ Throws: ReferenceError: Cannot access 'age' before initialization

// 2. TDZ ENDS HERE FOR 'age'
let age = 25;

console.log(age);  // Output: 25 (TDZ se bahar aa chuka hai)
```

> Use code with caution.

"Is example mein dikhta hai ki chunki `let age` line number 7 par declare hua hai, to scope ke start se lekar line 7 tak ka jo area tha, wo `age` ke liye dead zone tha. Isliye line 5 par strict error aaya."

## 2. An Interesting Interview Trick: Why the Word "Temporal"?

"Interviewers kabhi-kabhi fasaane ke liye puchte hain ki iska naam 'Temporal' (Time-based) kyun hai, 'Spatial' (Space-based) kyun nahi?

Iska jawab yeh hai ki TDZ variable ke position (line number) par nahi, balki execution ke time par depend karta hai. Agar ek function variable declaration ke upar likha hai par wo call declaration ke baad hota hai, to error nahi aayega kyunki call hote waqt tak variable ka TDZ time khatam ho chuka hota hai."

## 3. Summary Matrix

Aap is structure ko dimaag mein rakh sakte hain:

| Declaration Type | Hoisted? | Initial Value in Memory | Affected by TDZ? | Error Type if Accessed Early   |
| ---------------- | -------- | ----------------------- | ---------------- | ------------------------------ |
| `var`            | Yes      | `undefined`             | ❌ No             | No Error (Returns `undefined`) |
| `let`            | Yes      | Uninitialized           | Yes              | `ReferenceError`               |
| `const`          | Yes      | Uninitialized           | Yes              | `ReferenceError`               |
| `class`          | Yes      | Uninitialized           | Yes              | `ReferenceError`               |

---

## 4. Why Did JavaScript Introduce TDZ? / Conclusion (30 Seconds)

"To conclude, TDZ ko introduce karne ka main reason tha Code Predictability aur Runtime Safety.

Puraane JavaScript mein variables ko declare karne se pehle use karna ek kharab practice thi, par `var` use allow kar deta tha jisse bohot se silent bugs aate the. TDZ hamen majboor karta hai ki hum pehle variables ko properly declare karein aur phir use karein. Yeh development ke waqt hi bugs ko catch karne mein bohot madad karta hai."

---

# What Happens When You Try to Access a Variable Before It's Declared Using Different Declaration Methods?

| Declaration Method        | Hoisted? | Memory Initialization | Early Access Outcome | Error Type (If Any) |
| ------------------------- | -------- | --------------------- | -------------------- | ------------------- |
| `var` variable            | Yes      | `undefined`           | Returns `undefined`  | No Error            |
| `let` / `const` variable  | Yes      | Uninitialized (TDZ)   | Code Crashes         | ❌ `ReferenceError`  |
| Function Declaration      | Yes      | Actual Function Body  | Works Perfectly      | No Error            |
| `var` Function Expression | Yes      | `undefined`           | Code Crashes         | ❌ `TypeError`       |

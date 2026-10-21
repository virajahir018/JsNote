
1. Introduction & Hook (30-45 Seconds)

"Sir, JavaScript mein variables ko hum data store karne ke containers ki tarah dekhte hain. Agar hum ES5 yaani puraane JavaScript ki baat karein, to hamare paas variables declare karne ka sirf ek tareeqa tha—var keyword.
Lekin 2015 mein jab ES6 (ECMAScript 2015) introduce hua, to JavaScript ke scope aur memory management ko behtar banane ke liye do naye keywords laye gaye—let aur const. Aaj ke time par modern JavaScript development mein in teeno ka sahi use karna code ki efficiency aur bug-free execution ke liye bohot zaroori hai."

2. Core Comparison: The Three Pillars (2 Minutes)

"In teeno keywords ke beech ke differences ko hum mainly teen parameters par samajh sakte hain: Scope, Redeclaration & Re-assignment, aur Hoisting."

Pillar 1: Scope (Kahan tak access kar sakte hain?)

• "var Function-scoped hota hai. Iska matlab agar humne var ko kisi function ke andar declare kiya hai, to wo sirf us function mein chalega. Lekin agar use kisi if block ya loop ke andar declare kiya, to wo block ke bahar bhi access ho jata hai.
• Wahi dusri taraf, let aur const Block-scoped hote hain. Agar inhein kisi bhi curly braces {} (jaise loop ya if-else) ke andar likha jaye, to ye uske bahar access nahi kiye ja sakte. Yeh memory leak aur accidental variable override ko rokta hai."

Pillar 2: Redeclaration & Re-assignment (Kya hum badal sakte hain?)

• "var bohot zyada flexible hai—ise aap ek hi scope mein re-declare bhi kar sakte hain aur value re-assign bhi kar sakte hain. Is wajah se purani scripts mein bade bugs aate the.
• let mein aap value to badal (re-assign) sakte hain, lekin use dobara re-declare nahi kar sakte.
• const ka matlab hai Constant. Ismein na to aap re-declare kar sakte hain aur na hi value ko re-assign kar sakte hain. Isko declare karte waqt hi value dena compulsory hota hai."

Pillar 3: Hoisting (Execution se pehle kya hota hai?)

• "JavaScript mein hoisting ke dauran teeno keywords top par chale jaate hain, lekin unka behavior alag hota hai.
• var variables hoisted hote hain aur undefined se initialize ho jaate hain. Isliye agar aap declare karne se pehle unhein use karein, to error nahi aata, sirf undefined milta hai.
• let aur const bhi hoist hote hain, lekin wo initialize nahi hote. Wo ek Temporal Dead Zone (TDZ) mein chale jaate hain. Agar aap inhein declaration se pehle access karne ki koshish karenge, to JavaScript aapko ek ReferenceError dega, jo ki safe coding ke liye bohot achha hai."


Real-world Examples & Use Cases (1 Minute)

"Agar hum inke practical application ki baat karein, to real-world development mein hamari basic approach badal chuki hai:
• const ka use: Hum un values ke liye karte hain jo kabhi change nahi honi chahiye, jaise kisi API ka base URL (const API_URL = 'https://example.com'), ya configuration settings, ya functions aur arrays ke references.
• let ka use: Hum tab karte hain jab humein pata ho ki variable ki value aage chalkar badlegi, jaise kisi for loop ka counter variable (let i = 0) ya fir kisi shopping cart ka total price jo product add hone par change hoga.
• var ka use: Aaj ke modern standard mein var ka use completely avoid kiya jata hai kyunki block scope na hone ki wajah se ye global window object ko pollute kar deta hai aur unexpected bugs create karta hai."

4. Special Edge Case: Objects and Arrays with Const (30 Seconds)

"Yahan par ek bohot interesting point aur interview ka favourite question aata hai—const ke sath Objects aur Arrays ka behavior.
Jab hum const se koi array ya object banate hain, to uska reference block ho jata hai, yaani hum use naya object re-assign nahi kar sakte. Lekin, hum us object ke andar ke properties ko ya array ke elements ko mutate (change/modify) kar sakte hain. Jaise const user = { name: 'Amit' }; mein hum user.name = 'Rahul'; bilkul kar sakte hain."
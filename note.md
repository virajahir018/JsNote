# What is Javascript

  JavaScript ek programming language hai jo websites ko interactive banati hai.
  HTML structure deta hai, CSS design deta hai, aur JavaScript website ko “zinda” banata hai 😄

  # Example:

  Button click karna
  Form validate karna
  Game banana
  Animation
  API se data lana
  Mobile apps aur backend banana
  

  1. # What is Variable 
     
    JavaScript me Variables ka use data store karne ke liye hota hai.
    Jaise kisi box me cheeze rakhte ho, waise variable me value store hoti hai.

    # JS me 3 types ke variable keywords hote hain

    1. let :

    Value change ho sakti hai.

    2. const :
    
    Value change nahi kar sakte.

    3. var :
    
    Purana method hai. Aajkal mostly let aur const use karte hain.

    let vs const


    Feature	              var            let	      const      

    Value change	        ✅             ✅	         ❌
    Reassign	            ✅             ✅	         ❌
    Redeclare             ✅             ❌          ❌
    Block Scope           ❌             ✅          ✅


  2. # Data Types

    Data Type ka matlab hota hai → variable me kis type ka data store hai.

    1. Primitive Data Types

       Ye basic/simple data types hote hain.

       Types:

       String
       Number
       Boolean
       Undefined
       Null
       BigInt
       Symbol


    2. Non-Primitive Data Types

       Ye complex data store karte hain.

       Mainly:

       Object
       Array
       Function


  # Functions

    Function = reusable code block
    Matlab ek baar code likho aur baar-baar use karo

    Function Kyun Use Karte Hain?

    Agar same kaam multiple baar karna ho to function helpful hota hai.
    
    # Parameters :

      Parameters function ko data receive karne ke liye use hote hai.

      <!-- function greet(name) {
      console.log("Hello " + name);
      }

      greet("Viraj");        -->

      name → parameter hai
      "Viraj" → argument hai (actual value)

      # Parameters vs Arguments
      
        Term	                                                Meaning

        Parameter	                                  Function banate time variable
        Argument	                                  Function call karte time actual value


      # Simple Return

      <!-- 
        function add(a, b) {
        return a + b;
      }

      let result = add(10, 20);

      console.log(result); -->

      # Without Return

      <!-- 
      function add(a, b) {
      a + b;
      }

      console.log(add(2, 3)); 
      
      Output :
      undefined
      -->


    # Function Expression :

      JavaScript me function ko variable ke andar store karna
      Function Expression kehlata hai.

      <!-- 
      const variableName = function() {
            // code
      }; -->


    # Anonymous Function :

      Jis function ka naam nahi hota usse anonymous function bolte hai.

      <!-- 
      hello();

      const hello = function() {
          console.log("Hi");
      }; 
      
      Output : 

      Error
      -->
      Anonymous function hoisting me thoda different behave karta hai.
      Kyuki variable baad me initialize hua.

      Kyuki JavaScript ko nahi pata function ka use kaha hoga.

      Isliye anonymous function mostly:
      variable me store hota hai
      callback me use hota hai



    # Arrow Function :
      
      Arrow Function ES6 me introduce hua tha.
      Ye function likhne ka short aur modern way hai.

      <!-- 
      const functionName = () => {
          // code
      }; -->

      # Single Parameter :

        Agar sirf ek parameter ho to () optional hai.

      <!-- 
        const square = n => {
            return n * n;
        };

        console.log(square(5)); -->

      # Short Return :

        Single line me return likhne ki zarurat nahi.

      <!-- 
        const multiply = (a, b) => a * b;

        console.log(multiply(2, 3));       -->

      # Important Points

        Short syntax
        ES6 feature
        Single line me automatic return
        One parameter me () optional
        Mostly modern JavaScript me use hota hai
        this alag behave karta hai


    # Default Parameters :

      Agar function call karte time koi value pass nahi karo,
      to function automatically default value use karega.

      <!-- 
      function greet(name = "Guest") {
      console.log("Hello " + name);
      }

      greet();
      greet("Viraj"); -->

      <!-- 
      Output  
      
      Hello Guest
      Hello Viraj
      -->

      Agar name na mile to "Guest" use hoga

      # Important Points :
       
        ES6 feature hai
        Missing values ke liye useful hai
        Errors kam hote hai
        Multiple default parameters use kar sakte ho
        Arrow function me bhi kaam karta hai

    
    # Function Scope :

      Variable kaha tak accessible hai.

      Function ke andar banaya gaya variable
      irf us function ke andar hi use hota hai.

      Isko Function Scope bolte hai. 

      <!-- 
      function test() {
      let message = "Hello";
    
      console.log(message);
      }

      test();     -->

    # Global Scope :

      Global variable har jagah accessible hota hai.

      <!-- 
      let city = "Rajkot";

      function test() {
          console.log(city);
      }

      test();
      console.log(city); -->

      # Important Difference :
        
        Keyword	                       Scope

        var	                           Function Scope
        let	                           Block Scope
        const	                         Block Scope

      <!-- 
        function test() {

        if (true) {
            var a = 10;
            let b = 20;
        }

        console.log(a);
        console.log(b);
        }

        test(); -->
        
      <!-- Output 

        10
        Error
      -->

    # Nested Function Scope :

      Inner function outer variable access kar sakta hai.

      <!--      

      Inner function outer variable access kar sakta hai.

      function outer() {

          let name = "Viraj";

          function inner() {
              console.log(name);
          }

          inner();
      }

      outer(); -->

      # Important Points :

        Function ke andar ka variable bahar access nahi hota
        Global variable har jagah use ho sakta hai
        var → function scoped
        let & const → block scoped
        Inner function outer variables access kar sakta hai

      
    # Callback Function :

      Ek function ko dusre function ke andar argument ki tarah pass karna.
      Aur baad me us function ko call karna.

      # Why Use Callback Functions? 

        Async tasks
        Reusable code
        Event handling
        Timers
        API calls
        Array methods (map, filter, forEach)

      # Async tasks :
        
      <!-- 
        function fetchData(callback) {
            setTimeout(() => {
                callback("Data loaded");
            }, 2000);
        }

        fetchData((data) => {
            console.log(data);
        }); -->
      
      # IIFE (Immediately Invoked Function Expression) :
        
        Function banao aur turant execute karo.

       # Normal Function :
      <!--          
         (function () {
         console.log("Hello");
         })(); -->

         ();

         Ye us function ko immediately call karta hai.

       # Arrow Function :

      <!-- 
         const student = ((name) => {
         console.log("Name :", name)
         })("Viraj"); -->

  # Hoisting :

    JavaScript execution se pehle
    declarations ko memory me store karta hai.

    <!-- 
    console.log(age);
    var age = 20; -->

    # Hoisting in Functions :

      Function declaration ko code execute hone se pehle memory me store kar diya jata hai.
      Isliye function ko declaration se pehle bhi call kar sakte ho.

      Function declaration fully hoist hota hai.

      hello();


    # Function Expression Hoisting :

      Const :  
      <!-- 
      hello()

      const hello = function() {
      console.log("Hello");
      }; 
      
      Output :
      Error
      -->
 
      var :
      <!-- 
      hello();

      var hello = function() {
          console.log("Hello");
      }; 
      
      Output :
      TypeError
      -->

      Function Expression / Arrow Function :

      ❌ Before declaration call nahi kar sakte


      # Important Points :

      Function declarations fully hoist hote hai
      Function expressions variable rules follow karte hai
      Arrow functions bhi variable rules follow karte hai
      var → undefined
      let & const → Temporal Dead Zo      


  # Conditions :

    Conditions ka use decision lene ke liye hota hai.

    Agar condition true ho → ek code chalega
    Agar false ho → dusra code chalega
    
    # == :

      Sirf value compare karta hai.

    # === :

      Value + type dono compare karta hai.

    # Ternary Operator :

      Short form of if else

      <!-- 
      condition ? trueCode : falseCode -->

      <!-- 
      let age = 18;

      let result = age >= 18 ? "Adult" : "Minor";

      console.log(result); -->

    # Truthy and Falsy Values :

      Falsy values
      Ye false behave karte hain :

      false
      0
      ""
      null
      undefined
      NaN

 
  # DOM (Document Object Model) :

    DOM ki help se JavaScript :

    HTML ko change kar sakta hai
    CSS change kar sakta hai
    Button click handle kar sakta hai
    Text update kar sakta hai
    Elements add/remove kar sakta hai

    1. getElementById()
       ID se element pakadta hai.

    2. getElementsByClassName()
       Class se elements select karta hai.

    3. getElementsByTagName()
       Tag name se select karta hai.

    4. querySelector()
       Sabse pehla matching element select karta hai.

    5. querySelectorAll()
       Sab matching elements select karta hai.

    # innerText :
      Sirf visible text change karta hai.

      <!-- 
      let title = document.getElementById("title");
      title.innerText = "Welcome"; 
      -->

    # innerHTML :
      HTML bhi insert kar sakta hai.

      <!-- 
      title.innerHTML = "<i>Hello</i>"; 
      -->

    # Style Change Karna :

      <!--       
      let title = document.getElementById("title");

      title.style.color = "red";
      title.style.backgroundColor = "yellow"; 
      -->

    # Attribute Change Karna :

      getAttribute() :
      <!-- 
      let link = document.getElementById("link");

      console.log(link.getAttribute("href")); 
      -->

      setAttribute() :
      <!-- 
      link.setAttribute("href", "https://youtube.com"); 
      -->

      Create New Element :
      <!-- 
      let newElement = document.createElement("h1");
      newElement.innerText = "New Heading"; 
      -->

      Add Element :
      <!-- 
      document.body.appendChild(newElement); 
      -->

      Remove Element :
      <!-- 
      newElement.remove(); 
      -->


   # DOM Traversing :
     Element ke relatives access karna.

     Property	                               Meaning

     parentElement	                         parent
     children	                               child elements
     firstElementChild	                     first child
     lastElementChild	                       last child

     <!-- 
     let parent = document.getElementById("box");
     console.log(parent.children); 
     -->

      # classList :
      Class add/remove karne ke liye.

      <!-- 
      element.classList.add("active"); 
      -->

      <!-- 
      element.classList.remove("active"); 
      -->

      <!-- 
      element.classList.toggle("dark"); 
      -->


  # JavaScript Loops :
    Loop ka use repeated kaam ko baar-baar chalane ke liye hota hai.

    Matlab:
    Same code multiple times likhne ki zarurat nahi.

    1. for Loop :
       Sabse common loop.

       # Syntax : 

       <!-- 
       for(initialization; condition; update) {

       }
       Example
       for(let i = 1; i <= 5; i++) {
          console.log(i);
       } 
       -->

    2. while Loop :
       Jab tak condition true hai tab tak loop chalega.

       # Syntax :
       
         <!-- 
         let i = 1;

         while(i <= 5) {
            console.log(i);

            i++;
         } 

         i++ nahi diya → loop kabhi band nahi hoga.
         -->

    3. do while Loop :
       Pehle code chalega, phir condition check hogi.

       <!-- 
       let i = 1;

       do {
          console.log(i);
          i++;
       }
       while(i <= 5); 
       -->

    4. for...of Loop :
       Arrays aur iterable values ke liye.


       <!-- let fruits = ["Apple", "Banana", "Mango"];

       for(let fruit of fruits) {
          console.log(fruit);
       } 
          Output:
          Apple
          Banana
          Mango
       --> 


    5. for...in Loop :
       Objects ke liye.

        
       <!-- 
       let student = {
          name: "Viraj",
          age: 18
       };

       for(let key in student) {
          console.log(key);
       }

          Output:
          name
          age 
       -->

      # Object Values Access :
        <!-- 
        for(let key in student) {
           console.log(student[key]);
        }\

        Output:
        Viraj
        18 
        -->

        # break Statement :
          Loop ko turant stop karta hai.

          <!-- 
          for(let i = 1; i <= 10; i++) {

              if(i === 5) {
                  break;
              }

            console.log(i);
          }        
          -->

        # continue Statement :
          Current iteration skip karta hai.

          <!-- 
          for(let i = 1; i <= 5; i++) {

             if(i === 3) {
                continue;
             }

             console.log(i);
          }

              Output:

                1
                2
                4
                5 
          -->

        # Nested Loop :
          Loop ke andar loop.

          <!-- 
          for(let i = 1; i <= 3; i++) {

             for(let j = 1; j <= 2; j++) {

                console.log(i, j);

             }

          } 
          -->


  # Arrays :
    Array ka use multiple values ko ek variable me store karne ke liye hota hai.

    <!-- 
    let data = [
        "Viraj",
        18,
        true
    ]; 
    -->
    JavaScript arrays mixed values store kar sakte hain.

    Array indexing 0 se start hoti hai.

    # Change Array Value :
      <!-- 
      fruits[1] = "Orange";
      console.log(fruits); 
      -->

    # Array Length
      <!-- 
      let fruits = ["Apple", "Banana", "Mango"];
      console.log(fruits.length); 
      -->

    1. push() :
       End me value add karta hai.

       <!-- 
       fruits.push("Mango") 
       -->

    2. pop() :
       Last value remove karta hai.

    3. unshift() :
       Start me value add karta hai.

    4. shift() :
       First value remove karta hai.

    5. includes() :
       Check karta hai value exist karti hai ya nahi.

       <!-- 
       let fruits = ["Apple", "Banana"];
       console.log(fruits.includes("Apple")); 
       -->

    6. indexOf() :
       Index batata hai.

    7. join() :
       Array ko string banata hai.

    8. reverse() :
       Array reverse karta hai.

       <!-- 
       fruits.reverse(); 
       -->

    9. sort() :
       Sort karta hai. / Ek Line me

    10. Array of Objects :
   
       <!-- 
        let students = [

           {name: "Viraj", age: 18},

           {name: "Rahul", age: 20}

        ];

        console.log(students[0].name); -->

    11. Nested Arrays :
   
       <!-- 
        let data = [
            [1,2],
            [3,4]
        ];

        console.log(data[0][1]); -->

    # Important Array Methods (Modern JS) :

      1. map() :
         ek array method hai jo array ke har element par operation perform karta hai aur naya array return karta hai.
         Original array change nahi hota.

         <!-- 
         let nums = [1,2,3];

         let result = nums.map(num => num * 2);

         console.log(result); -->

      2. filter() :         
         Condition ke basis pe filter karta hai.

         <!-- 
         let nums = [1,2,3,4];

         let even = nums.filter(num => num % 2 === 0);

         console.log(even); -->

      3. find() :          
         First matching value return karta hai.

         <!-- 
         let users = [10,20,30];

         let result = users.find(num => num > 15);

         console.log(result); -->

      4. forEach()         
         Har element pe action perform karta hai.

         <!-- 
         let nums = [1,2,3];

         nums.forEach(num => {
            console.log(num);
         }); -->

      5. Spread Operator with Arrays :
         
         Spread Operator ka syntax : (...) 
         Ye array ke elements ko spread expand (faila) deta hai.

         let numbers = [1, 2, 3];

         <!-- console.log(...numbers); -->
         Output
         1 2 3

         ...numbers
         Array ko individual values me tod deta hai.

         Copy Array , Merge Arrays , Add New Elements , Add Elements at Start , Combine Multiple Arrays kar sakta hai 

         <!-- 
         let cartItems = ["Shoes", "Watch"];

         let updatedCart = [...cartItems, "T-shirt"];

         console.log(updatedCart);-->

         # Important Points

           ... spread operator hai
           Arrays copy kar sakte ho
           Arrays merge kar sakte ho
           New elements add kar sakte ho
           Function arguments me use hota hai
           ES6 feature hai

      6. Array.isArray() :
         Check karta hai value array hai ya nahi.
      
      7. concat() :
          2 arrays ko join karta hai.

          <!-- 
          let a = [1,2];
          let b = [3,4];

          let result = a.concat(b); -->

      8. slice() :
         array ka kuch part nikalne ke liye use hota hai.
         Original array change nahi karta.

         <!-- array.slice(start, end) -->

      9. splice() :
         Add/remove/change kar sakta hai.
         Original array change karta hai.

      10. flat() :
          Nested arrays ko simple banata hai.

          <!-- 
          let arr = [1, [2,3], [4,5]];
          console.log(arr.flat());

          Output:
          [1,2,3,4,5] -->

      11. some() :
          Agar koi ek element condition satisfy kare.

          <!-- 
          let nums = [1,2,3];

          let result = nums.some(num => num > 2);
          console.log(result);

          Output:
          true -->

      12. every() :
         Sab elements condition satisfy kare.

      13. reduce() :
          Single value return karta hai.

          <!-- 
          let nums = [1,2,3,4];

          let total = nums.reduce((acc, curr) => {
              return acc + curr;
          }, 0);

          console.log(total); -->

      14. Array.from() :
          kisi cheez ko array me convert karta hai.

  
  # synchronous :
    Code line by line execute hota hai.
    Ek kaam complete hone ke baad hi next kaam start hota hai.

    Synchronous code block karta hai.
    Agar ek task slow ho to next wait karega.

    JavaScript normally synchronous hoti hai.

  # Asynchronous :
    JavaScript kisi task ka wait nahi karta.
    Task background me chalta hai aur baaki code execute hota rehta hai.
  
  # Promise :
    Promise ek object hai jo future me :

    value de sakta hai
    error de sakta hai

    Promise asynchronous operations handle karne ke liye use hota hai.

    Promise States :

    State	          Meaning

    Pending	        Kaam chal raha hai
    Fulfilled	      Success
    Rejected	        Error

    <!-- let myPromise = new Promise((resolve, reject) => {

    let success = true;

    if(success) {
        resolve("Task Complete");
    } else {
        reject("Task Failed");
    }
    }); 

    console.log(myPromise);-->

    <!-- resolve() -->
    resolve("Task Complete");
    Promise successful.

    <!-- reject() -->
    reject("Task Failed");
    Promise failed.

    <!-- 
    let promise = new Promise((resolve, reject) => {

    resolve("Success");

    });

    promise
        .then(result => {
            console.log(result);
        })
        .catch(error => {
            console.log(error);
        });

        Output
        Success -->

       .then() :
       Success handle karta hai ✅

       .catch() :
       Errors handle karta hai ❌

       finally() :
       success ho ya error,
       HAR CASE me chalta hai.

       <!-- 
       fetch("https://jsonplaceholder.typicode.com/users")
          .then((res) => res.json())
          .then((data) => {
              console.log("Success");
          })
          .catch((err) => {
              console.log("Error");
          })
          .finally(() => {
              console.log("Done");
          }); -->

  # Async / Await :
    Promise handle karne ka modern easy way
    async/await ka use asynchronous code ko easy aur readable banane ke liye hota hai.

    Multiple .then() confusing ho sakte hain.
    Isliye async/await use karte hai

    async Keyword :
    Function ko asynchronous banata hai.
    Async function automatically Promise return karta hai.
 
    await Keyword :
    Promise complete hone tak wait karta hai.

    fetch() :
    server/API se data lane ke liye use hota hai.
    Ye Promise return karta hai.

    # Error Handling with try/catch 

      <!-- 
      async function getData() {

        try {
            let response = await fetch("wrong-url");
            let data = await response.json();
            console.log(data);
        }
        catch(error) {
            console.log("Error:", error);
        }
      }
      getData(); -->

      Why try/catch ?

      Agar error aaye : 
      app crash nahi karega
      error handle ho jayega

      # Promise.all() :
        Promise.all() multiple promises ko ek sath run karta hai.

        Sab promises successful hue to result deta hai
        Ek bhi fail hua to pura reject ho jata hai


  # Closure :
    Jab ek function apne outer function ke variables ko yaad rakhta hai, even outer function execute hone ke baad bhi, use Closure kehte hai.

  
  # localStorage :
    localStorage browser ka storage system hai jisme data permanently save hota hai.

    Page refresh ho
    Browser close ho
    PC restart ho
    tab bhi data save rehta hai

    localStorage kya store karta hai?
    String data

    Agar object/array store karna ho to:
    JSON.stringify()
    JSON.parse()
    use karna padta hai.

    setItem() :  Data save
    getItem() :  Data get
    removeItem() :  One item delete
    clear() :  Sab delete

  
  # Event Delegation :
    Event Delegation ek technique hai jisme:

    Parent element par event listener lagate hai
    Child elements ke events handle karte hai

    Ye possible hota hai because of:
    Event Bubbling

    <!-- 
    parent.addEventListener("click", function(event) {

    if(event.target.tagName === "BUTTON") {
      console.log(event.target.innerText);
    }

    }); -->
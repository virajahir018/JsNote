# Split() ?
- Ek string ko kisi particular character/word ke basis par todkar array banana
  - const name = "Viraj Ahir";
  - console.log(name.split(" "));
  
Output :
- ["Viraj", "Ahir"]
- ka matlab hai space ke jagah se string ko tod do.

# Optional Chaining ?. ?
- Kisi property ke na hone par error se bachata hai.

- const age = 20;
- const result = age >= 18 ? "Adult" : "Minor";
- console.log(result);
- 
- condition ? true wala : false wala

# .sort({ createdAt: -1 }) ?
- Latest order sabse upar dikhayega.

- -1 = descending order
-  1 = ascending order
-  

if (!getData.ok) {

ka simple meaning hai:

"Agar API request successful nahi hui, to ye code chalao."

Interview mein short answer:

response.ok batata hai ki fetch request successful hui hai ya nahi. true means HTTP status 200–299, aur false means error status.

 <h1>{product?.title}</h1>

 ?. isliye lagaya hai kyunki API response aane se pehle product null hai.

Ab ye implement karo. Agar product ka title screen par aa gaya → done bolo.
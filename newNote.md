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






L2: Secure Authentication & Subscription-Based Content Access with Token BlacklistingObjective:Build a secure authentication system with role-based access control (RBAC), subscription management, token blacklisting, and business logic around content access based on subscription plans.Problem StatementYou need to implement:1. User Authentication (Signup, Login, Logout, Token Management)Signup/Login: Users register with username, email, and password.Password hashing: Store securely.JWT Tokens: Generate access & refresh tokens on login.Token Blacklisting:Logout should invalidate the access & refresh tokens by blacklisting them.Blacklisted tokens should not be usable anymore.Role-Based Access:Users can manage their subscriptions & access content.Admins can create, update, or delete content & manage subscriptions.2. Subscription-Based Content Access (CRUD with Business Logic)Users can subscribe to a plan (free, premium, pro) to access content.Content is categorized into "Free" & "Premium".Access Rules Based on Subscription:Free users can only view free content.Premium users can access both free & premium content.Pro users get additional discounts on purchases (business logic).Dynamic Expiry: Subscriptions should expire 30 days after purchase.Auto-Downgrade:If a subscription expires, the user is automatically moved to "free" access.3. Token Expiry, Refresh, and BlacklistingAccess Token Expiry: 15 minutesRefresh Token Expiry: 7 days (optional)Token Blacklisting on Logout: (optional)Add access & refresh tokens to a blacklist DB.Blacklisted tokens should be checked on every request.Renewal Logic:Users can renew their subscription before expiry.If expired, they must buy a new subscription.API RequirementsAuthentication Routes:POST /signup → Register a user (password hashed)POST /login → Authenticate user & generate JWT tokensPOST /logout → Blacklist tokens & logout userPOST /refresh → Issue a new access token, reject if blacklistedSubscription Routes (Protected, Role-Based)POST /subscribe → Users buy a subscriptionGET /subscription-status → Check subscription validityPATCH /renew → Users can renew before expiryPOST /cancel-subscription → Users can cancel manuallyContent Routes (RBAC Protected)GET /content/free → All users can view free contentGET /content/premium → Only Premium/Pro users can accessPOST /content → Only admins can create new contentDELETE /content/:id → Only admins can delete contentExpected OutcomesSecure authentication with signup, login, logout, and token blacklistingSubscription-based access control with automatic expiry & renewalJWT token management (refresh, expiry, and blacklisting on logout)Admins can manage content, users can subscribe & access it based on plansProper role-based access control (RBAC) & API security measuresSubmission GuidelinesImplement secure authentication, RBAC, token management, and subscription business logicEnsure JWT token expiry, refresh, and blacklistingSubscription expiry should be auto-handledPush your code to the Masai repository for submission
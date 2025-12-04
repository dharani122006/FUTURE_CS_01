Task 1: Web Application Security Testing
✔ Objective

Perform security testing on a vulnerable web application and identify common web vulnerabilities such as:

SQL Injection

Cross-Site Scripting (XSS)

Authentication Bypass

✔ Tools Used

Burp Suite Community Edition

OWASP Juice Shop

Browser (Chrome)
✔ Vulnerabilities Identified
1️⃣ SQL Injection

Injection used:

' OR 1=1--


Result: Able to bypass login without valid credentials

Status: Successfully exploited

Evidence: Screenshots uploaded in the repo

2️⃣ XSS (Coming next)

Will be tested by injecting JavaScript alert into input fields.

3️⃣ Authentication Bypass (Coming next)

Will attempt to bypass login or access restricted pages.

✔ Screenshots

Screenshots are uploaded in this repository showing:

SQL Injection login attempt

Successful login using SQLi

🛡️ Task 2 – Cross-Site Scripting (XSS Attack)
🎯 Objective

To identify and exploit a stored XSS vulnerability in OWASP Juice Shop.

🧪 Steps Performed

Logged in to OWASP Juice Shop.

Navigated to the Search bar.

Injected the following payload:

"><svg/onload=alert('Dora')>


Pressed Enter.

The browser executed the JavaScript payload.

✅ Result

A popup alert box displayed the message “Dora”, confirming that the website is vulnerable to Stored XSS.

📸 Proof

Screenshots attached in repository:

Popup alert screenshot

Payload visible in search bar

🧠 Learning Outcome

I understood how user input, when not properly sanitized, can execute malicious JavaScript inside a website and affect users.
🔐 Task 3 – Broken Authentication (Admin Login Bypass)
🎯 Objective

To exploit a weak authentication mechanism and log in as admin without knowing the password.

🧪 Steps Performed

Opened Login page in OWASP Juice Shop.

Entered the following SQL Injection payload in the email field:

' OR 1=1--


Typed any value in the password field (e.g., 123).

Clicked Log in.

The login system executed the injected SQL query and authenticated me as admin.

✅ Result

Successfully logged in as admin@juice-sh.op
.

Full admin account access obtained without a password.

This confirms the application is vulnerable to SQL Injection authentication bypass.

📸 Proof

Screenshot showing admin logged in.

🧠 Learning Outcome

I learned how insecure SQL queries allow attackers to bypass login checks and gain unauthorized access.

✔ Intern: Dora
  

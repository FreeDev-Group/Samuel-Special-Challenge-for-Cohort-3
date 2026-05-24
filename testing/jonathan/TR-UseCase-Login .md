# TEST REPORT — Create Account Use Case

**Tester:** Jonathan Bitingingwa

**Date:**  18h May,2026

**Issue Reference:**  #3

**Use Case:**  Login Use Case

---

## What I am testing
I am testing Loging in with valid Student credentials and verifying redirection to the Student dashboard then evaluating error handling, security mechanisms and system responses to invalid login attempts.
This test confirms that a registered student can successfully authenticate and access the correct dashboard

## What I did (steps)

### Scenario 1 —
-I opened the application: https://student.michaelkentburns.com/
-I clicked on “User”
-I clicked on “Login”
-I was redirected to the login section
-I entered valid credentials:
Username: jonathantest
Password: (valid password created during registration)
I clicked “Login”

### Scenario 2 —
-I opened the application: https://student.michaelkentburns.com/
-I clicked on “User” - “Login”
-I entered:
Username: jonathantest
Password: jolva@1111
-I clicked “Login”

### Scenario 3 —
-I entered wrong password 3 consecutive times
-I attempted to log in again immediately

### Scenario 4 —  
-I entered wrong password 5 consecutive times  
-I attempted to log in again immediately

### Scenario 5 —  
-I opened the application  
-I clicked on “User” - “Login”  
-I entered:  
Email: jonates@email.com (unregistered)  
Password: valid password  
-I clicked “Login”  

---

## What I noticed
**Scenario 1 Result:**
I successfully logged in without any errors
I was redirected to the student dashboard (home section)

**Scenario 2 Result:**  
The system displayed: “The password you entered for the username jonathantest is incorrect. Lost your password?”  

**Scenario 3 Result:**    
The system allowed unlimited login attempts  
There was no lockout mechanism  
No warning or delay was applied

**Scenario 4 Result:**  
The system still allowed unlimited attempts  
No lockout, delay, or restriction observed

**Scenario 5 Result:**  
The system displayed: “Unknown email address. Check again or try your username.”

---

## What should have happened
Based on the use case:
-The system should authenticate valid credentials  
-Redirect the user to the Student dashboard  
-Display the correct student interface and welcome message  
-The system should deny access  
-Display a generic error message such as: “Invalid username or password”  
-After 3 failed attempts: Account should be temporarily locked (~1 minute)  
-System should display a message: “Too many failed attempts. Try again later.”  
-After 5 failed attempts:  
-Longer lockout (~3 minutes)  
-Clear warning message  
-The system should show a generic error message: “Invalid username or password”

---

## Is this a problem?

| # | Short Description | Type | Severity |
|---|-------------------|------|----------|
| 1 | NO Login flow works as expected|  Pass / Expected behavior| N/A|
| 2 |YES Error message reveals that the username exists|Security Issue / UX Issue| Medium–High|
| 3 |YES No lockout after multiple failed login attempts |Missing Feature|High|
| 4 |YES No escalation of security controls after repeated failed attempts|Missing Feature|High|
| 5 |YES System reveals that the email is not registered|Security Issue / UX Issue|Medium|

---

## Special Note
-Successful authentication confirms valid credential handling  
-Correct redirection to Student dashboard  
-No visible loading indicator during login (optional UX improvement)  
-No personalized message (e.g., username displayed)  
-System differentiates between valid username and wrong password  
-This behavior is not secure (information disclosure)  
-No rate limiting or protection observed  
-This is a critical security gap  
-Behavior is identical to Test Case 2 - no progressive protection  
-Indicates missing security implementation entirely  
-Error messages are inconsistent with security best practices  
-System exposes account existence
---

## Evidence
<img width="1322" height="597" alt="Image" src="https://github.com/user-attachments/assets/7d0ccd5f-5601-489d-854c-e6459eec81db" /> Screenshot of dashboard showing: “Welcome to the Student Survey App Platform”
<img width="1349" height="599" alt="Image" src="https://github.com/user-attachments/assets/4ab641b6-1c53-44d0-8dae-15d1a78cb11f" />
<img width="1349" height="599" alt="Image" src="https://github.com/user-attachments/assets/cc001891-2de9-4a54-91dd-8327640f9425" />
<img width="1337" height="588" alt="Image" src="https://github.com/user-attachments/assets/90f4cf5e-5fab-4be5-8b86-69966b8c8c69" />
<img width="1349" height="599" alt="Image" src="https://github.com/user-attachments/assets/cc001891-2de9-4a54-91dd-8327640f9425" />
<img width="1337" height="588" alt="Image" src="https://github.com/user-attachments/assets/90f4cf5e-5fab-4be5-8b86-69966b8c8c69" />

---

## My thoughts / questions
-What happens after session timeout?  
-Can I access this page directly without logging in?  
-Is role-based access strictly enforced?  
-ogin system correctly blocks invalid credentials  
Major Issues Found:  
-No account lockout mechanism  
-No rate limiting  
-Information disclosure through error messages  
-No progressive security controls  
-Overall Risk Assessment  
The system is functionally correct but NOT secure Vulnerable to brute-force attacks Vulnerable to user enumeration.

---

## Action taken
- [x] I created a sub-issue for the valid bug
- [x] I added the `bug` label on the sub-issue
- [x] I continued testing

Sub-issue links:

https://github.com/FreeDev-Group/Samuel-Special-Challenge-for-Cohort-3/issues/11


---

## Files
`/testing/[jonathan]/[TR-UseCase-Login].md`

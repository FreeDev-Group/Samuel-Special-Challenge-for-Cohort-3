# TEST REPORT — Create Account Use Case

**Tester:** Jonathan Bitingingwa

**Date:**  19h May,2026

**Issue Reference:**  #4

**Use Case:**  Password Recovery Use Case

---

## What I am testing
This test verifies that a registered student can successfully recover their account password using the “Lost your password?” feature and log in with the new password afterward, 
and verifie how the system handles password recovery attempts using an email address that does not exist in the system.

## What I did (steps)

### Scenario 1 —
-I opened the application: https://student.michaelkentburns.com/  
-I clicked on “User”  
-I clicked on “Login”  
-I navigated to the login page  
-I located and clicked the “Lost your password?” link  
-The system asked me to enter a Username or Email Address  
-I entered a valid registered email address  
-I clicked on “Get New Password”  
-I received the message: “Check your email for the confirmation link, then visit the login page.”  
-I immediately received an email containing:  
Site information    
Username  
Password reset link  
-I clicked on the reset link from the email  
-I was redirected to a page suggesting a strong password already filled in  
-I noticed another option allowing generation of a different password  
-I clicked on “Save Password”  
-I received the message: “Your password has been reset. Log in”  
-I clicked on the “Log in” link  
-I was redirected to the login page  
-I logged in successfully using the newly generated password

### Scenario 2 —
-I opened the application: https://student.michaelkentburns.com/  
-I clicked on “User”  
-I clicked on “Login”  
-I clicked on “Lost your password?”  
-The system requested a username or email address  
-I entered an unregistered email address  
-I clicked on “Get New Password”

---

## What I noticed
**Scenario 1 Result:**
- Positive observations:  
Password recovery flow worked successfully
Reset email was received immediately
Reset link worked correctly
Password reset form opened successfully
New password was accepted
Login with new password worked correctly

-Negative Observation:   
I did not receive a confirmation email after the password was successfully reset

**Scenario 2 Result:**
The system displayed the message: “Error: There is no account with that username or email address.”  
The system clearly revealed that the entered account does not exist.

---

## What should have happened
-Based on the use case:  
User should:  
-Receive password reset link  
-Successfully reset password  
-Be redirected to login page  
-Log in with new password  
-All of these steps worked correctly.  
-Additionally, from a security and usability perspective: A confirmation email after successful password reset could help notify users of account changes.  
-From a security perspective, the system should ideally display a generic response, such as: “If an account exists, a password reset email has been sent.” This prevents attackers from identifying whether an account is registered in the system.

---

## Is this a problem?

| # | Short Description | Type | Severity |
|---|-------------------|------|----------|
| 1 |Possibly (needs clarification)No confirmation email sent after password reset completion, Users are not notified that account credentials changed|Missing feature / Security enhancement consideration|Low–Medium|
| 2 |YES Password recovery reveals account existence through specific error message|Security Issue / Information Disclosure|High|

---

## Special Note
-Main password recovery functionality works correctly  
-Reset link is delivered and functional  
-New credentials authenticate successfully  
-Confirmation email after reset completion may not be implementedv  
-Need clarification whether post-reset confirmation email is part of system requirements  
-The password recovery process exposes account existence information  
-This behavior weakens authentication security  
-Generic recovery responses are recommended security best practice
---

## Evidence
<img width="1366" height="687" alt="Image" src="https://github.com/user-attachments/assets/09d29606-733c-4fc6-97a3-503cb86ddb57" /> Screenshot of password reset request page
<img width="1366" height="687" alt="Image" src="https://github.com/user-attachments/assets/e94fbb4b-16cd-48a5-8053-a8643a3b5f4c" /> Screenshot of received reset email
<img width="1366" height="670" alt="Image" src="https://github.com/user-attachments/assets/221ce08b-41b0-433e-9c7a-47a40ec74c87" /> Screenshot of successful reset confirmation
<img width="1366" height="687" alt="Image" src="https://github.com/user-attachments/assets/4e3d13f2-0e50-4a51-b910-9a44250d3340" /> Screenshot of successful login with new password
<img width="1366" height="691" alt="Image" src="https://github.com/user-attachments/assets/0695dc7c-b7db-420f-9807-0a9a9d0f7d32" /> Screenshot of entered unregistered email
<img width="1366" height="674" alt="Image" src="https://github.com/user-attachments/assets/11d5192f-7dcd-4c5f-ac8a-28f7618c87a5" /> Screenshot showing the error message

---

## My thoughts / questions
Is the absence of confirmation email intentional?  
Should users receive notification after password changes for security reasons?  
Does the reset link expire after use?  
Does the use case specify generic recovery messaging?  
Is this intentional behavior or missing security hardening?
---

## Action taken
- [x] Added observation regarding lack of post-reset confirmation email
- [x] Security issue identified
- [x] Sub-issue created for information disclosure vulnerability
- [x] I added the `bug` label on the sub-issue
- [x] I continued testing

Sub-issue links:

https://github.com/FreeDev-Group/Samuel-Special-Challenge-for-Cohort-3/issues/16


---

## Files
`/testing/[jonathan]/[TR-PasswordRecoveryUseCase].md`

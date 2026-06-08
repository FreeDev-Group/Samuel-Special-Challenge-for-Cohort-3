# TEST REPORT — Login Use Case

**Tester:** kamojosue09-blip

**Hour and Date:** 11h June 2026

**Issue Reference:** #23

**Use Case:** Login

## What I Tested

This test was conducted to verify that a registered student can successfully log into the application and access the Student Dashboard.

The test also verifies:

* Login with valid student credentials
* Login with an incorrect password
* Login with an unregistered username
* Account lockout behavior after 3 failed attempts
* Account lockout behavior after 5 failed attempts

---

## What I Did (Steps)

### Scenario 1 — Successful Student Login

* Opened the application: https://student.michaelkentburns.com/
* Clicked **User**
* Selected **Login**
* Entered a valid username
* Entered the correct password
* Clicked **Login**

### Scenario 2 — Incorrect Password

* Opened the Login page
* Entered a valid username
* Entered an incorrect password
* Clicked **Login**

### Scenario 3 — Unregistered Username

* Opened the Login page
* Entered an unregistered username
* Entered a password
* Clicked **Login**

### Scenario 4 — Three Consecutive Failed Login Attempts

* Entered the wrong password three consecutive times
* Attempted to log in again immediately

### Scenario 5 — Five Consecutive Failed Login Attempts

* Entered the wrong password five consecutive times
* Attempted to log in again immediately

---

## What I Observed

### Scenario 1 Result

The login process completed successfully.

The system:

* Authenticated the user successfully
* Redirected the user to the Student Dashboard
* Displayed the Student navigation menu:

  * Home
  * About
  * All Surveys
  * My Completed Surveys
  * Student

The login functionality worked as expected.

### Scenario 2 Result

The system displayed the following message:

> Error: The password you entered for the username josue_test2026 is incorrect. Lost your password?

The login attempt was rejected successfully.

### Scenario 3 Result

The system displayed the following message:

> Error: The username George is not registered on this site. If you are unsure of your username, try your email address instead.

The login attempt was rejected successfully.

### Scenario 4 Result

The system continued allowing login attempts after three consecutive failures.

No account lockout was observed.

No waiting period was enforced.

No security notification was displayed.

### Scenario 5 Result

The system continued allowing login attempts after five consecutive failures.

No account lockout was observed.

No restriction or temporary suspension was enforced.

No security alert was displayed.

---

## What Should Have Happened

According to the Login Use Case:

### Successful Login

* The system should authenticate valid credentials.
* The user should be redirected to the Student Dashboard.

### Incorrect Password

* The system should reject invalid credentials.

### After Three Failed Attempts

* The account should be temporarily locked for approximately one minute.
* The system should display a warning message.
* Additional security measures may be applied.

### After Five Failed Attempts

* The account should be locked for approximately three minutes.
* The system should display a security alert.
* Additional protection mechanisms should be triggered.

---

## Is This a Problem?

| # | Description                                          | Type                | Severity |
| - | ---------------------------------------------------- | ------------------- | -------- |
| 1 | Successful login works correctly                     | Expected Behavior   | N/A      |
| 2 | Error message reveals that the username exists       | Security / UX Issue | Medium   |
| 3 | No lockout after 3 failed attempts                   | Missing Feature     | High     |
| 4 | No lockout after 5 failed attempts                   | Missing Feature     | High     |
| 5 | Error message reveals that a username does not exist | Security / UX Issue | Medium   |

---

## Special Notes

The login functionality itself works correctly.

However, several documented security requirements from the Login Use Case were not observed:

* No lockout after 3 failed attempts.
* No lockout after 5 failed attempts.
* No escalation of security controls.
* No warning messages regarding excessive failed attempts.

The application also exposes account information through detailed error messages.

Instead of displaying a generic authentication error, the system reveals whether a username exists or not.

This behavior may increase the risk of user enumeration attacks.

---

## Evidence

## Evidence

### TC-09-Successful-to-access-for-home-page-after-login

Successful login and Student Dashboard access.

<img width="1355" height="699" alt="TC-09-Succefull to access for home page after password" src="https://github.com/user-attachments/assets/04dd0e2b-a251-488c-a265-abea4843b8e0" />



---

### TC-08-Password-Required

Incorrect password validation.

<img width="1366" height="768" alt="TC-08-Password-Required" src="https://github.com/user-attachments/assets/49f2827d-915c-4235-881c-028d7665e6ec" />

---

### TC-10-Unregistered-User-Login

Unregistered username validation.

<img width="1366" height="768" alt="TC-10-Unregistered-User-Login" src="https://github.com/user-attachments/assets/d728d378-6dce-481f-9522-9d447b9faeb1" />

---

## My Thoughts / Questions

* Is the account lockout feature planned but not yet implemented?
* Should the system display generic authentication errors instead of revealing account existence?
* Are additional security controls planned for future releases?
* Is brute-force protection currently implemented elsewhere?

---

## Action Taken

☑ Completed manual testing

☑ Documented findings

☑ Identified missing security functionality

☑ Continued reporting findings

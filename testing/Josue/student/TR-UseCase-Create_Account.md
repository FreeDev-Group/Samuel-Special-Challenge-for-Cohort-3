# TEST REPORT — Create Account Use Case

**Tester:** kamojosue09-blip

**Hour and date:** 11h June 2026

**Issue Reference:** #23

**Use Case:** Create Account

## What I Tested

This test was conducted to verify whether a student can successfully create an account, receive the registration email, create a password, and access the platform. The test also verifies whether the registration process follows the documented Create Account use case requirements.

---

## What I Did (Steps)

### Scenario 1 — Successful Student Registration

* Opened the application: https://student.michaelkentburns.com/
* Clicked **User**
* Selected **Register as Student**
* Entered a valid username and email address
* Submitted the registration form
* Received the message:

> Registration complete. Please check your email, then visit the login page.

* Opened the registration email
* Clicked the password creation link
* Created a password successfully
* Returned to the login page
* Logged into the application successfully

### Scenario 2 — Invalid Username Validation

* Opened the registration page
* Entered a username containing invalid characters and spaces
* Submitted the registration form

### Scenario 3 — Duplicate Email Validation

* Opened the registration page
* Entered a different username
* Entered an email address already registered in the system
* Submitted the form

---

## What I Observed

### Scenario 1 Result

The registration process completed successfully.

The system:

* Accepted the registration request
* Sent a registration email
* Allowed password creation through email
* Allowed immediate login after registration

However, several differences were observed compared to the documented use case:

* The system never requested Academic Level selection.
* The system never requested Programming Languages selection.
* No Pending Approval notification was displayed.
* No Administrator Approval workflow was observed.
* The account became active immediately after registration.

Additionally, the registration process uses an email password setup flow that is not described in the Create Account use case.

The overall process worked correctly but differs from the documented requirements.

### Scenario 2 Result

The system correctly rejected the invalid username and displayed the following validation message:

> Error: This username is invalid because it uses illegal characters. Please enter a valid username.

Validation worked as expected.

### Scenario 3 Result

The system correctly detected that the email address already existed and displayed the following message:

> Error: This email address is already registered. Log in with this address or choose another one.

Validation worked as expected.

---

## What Should Have Happened

According to the Create Account Use Case:

After selecting the Student role, the user should:

* Select Academic Level
* Select Programming Languages

After registration:

* Account information should be stored
* The account should enter a Pending Approval state
* An administrator should review the request
* The user should receive a Pending Approval notification
* Access should only be granted after approval

---

## Is This a Problem?

| # | Description                                | Type                | Severity |
| - | ------------------------------------------ | ------------------- | -------- |
| 1 | Academic Level selection is missing        | Missing Feature     | Medium   |
| 2 | Programming Languages selection is missing | Missing Feature     | Medium   |
| 3 | Pending Approval workflow is missing       | Missing Feature     | High     |
| 4 | Immediate login allowed after registration | Functional Mismatch | High     |

---

## Special Notes

The actual registration flow differs significantly from the documented Create Account use case.

The following documented requirements were not observed:

* Academic Level selection
* Programming Languages selection
* Pending Administrator Approval process

The account became active immediately after registration.

The registration process also relies on an email password setup flow rather than a direct password creation step described in the use case.

---

## Evidence

## Evidence

### TC-02-Illigall

Duplicate email validation.

<img width="1366" height="768" alt="TC-02-Illigall" src="https://github.com/user-attachments/assets/2cb7ec90-c3e9-4ca9-9704-9b72b55a0765" />

---

### TC-03-Register-Page

Student registration page.

<img width="1366" height="768" alt="TC-03-Register-Page" src="https://github.com/user-attachments/assets/7ee73356-38a2-4d54-9433-43e1d5e96aaa" />

---

### TC-04-Invalid-Username-Validation

Invalid username validation.

<img width="1366" height="768" alt="TC-04-Invalid-Username-Validation" src="https://github.com/user-attachments/assets/02e8bb47-9a60-4108-adea-603ff5bf4319" />

---

### TC-05-Registration-Success

Registration completed successfully.

<img width="1366" height="768" alt="TC-05-Registration-Success" src="https://github.com/user-attachments/assets/2cc5ff99-6f93-4d0f-9931-fd3f874b280a" />


---

### TC-06-Registration-Email

Registration email received.

<img width="1366" height="768" alt="TC-06-Registration-Email" src="https://github.com/user-attachments/assets/8d66c1ef-7056-429d-88bc-4dc9d2634a47" />


---

### TC-07-Password-Created

Password created successfully.

<img width="1366" height="768" alt="TC-07-Password-Created" src="https://github.com/user-attachments/assets/caed9500-c06f-49c5-8b98-45e1d3e057e0" />


---

## My Thoughts / Questions

* Is the Create Account use case outdated?
* Are Academic Level and Programming Languages planned for future implementation?
* Has the Administrator Approval process been intentionally removed?
* Should newly registered students be allowed immediate access to the platform?

---

## Action Taken

☑ Completed manual testing

☑ Documented findings

☑ Identified missing functionality

☑ Continued testing with the Login Use Case

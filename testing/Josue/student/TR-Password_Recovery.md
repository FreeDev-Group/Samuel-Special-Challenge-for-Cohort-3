# TEST REPORT — Password Recovery Use Case

**Tester:** kamojosue09-blip

**Hour and Date:** 17h June 2026

**Issue Reference:** #25

**Use Case:** Password Recovery

## What I Tested

This test verifies that a registered student can successfully recover access to their account using the password recovery workflow.

The test covers:

* Accessing the password recovery page
* Submitting a registered email address
* Receiving the password reset email
* Opening the reset link
* Creating a new password
* Logging in with the new password
* Handling an unregistered email address

---

## What I Did (Steps)

### Scenario 1 — Successful Password Recovery

1. Opened the application.
2. Clicked **User → Login**.
3. Clicked **Lost your password?**
4. Entered the registered email address.
5. Submitted the password recovery request.
6. Received a password reset email.
7. Opened the reset link from the email.
8. Entered a new password.
9. Submitted the new password.
10. Received a confirmation message.
11. Returned to the login page.
12. Logged in successfully using the new password.

### Scenario 2 — Unregistered Email Address

1. Opened the password recovery page.
2. Entered an email address that is not registered.
3. Submitted the request.
4. Observed the error message displayed by the system.

---

## What I Observed

### Scenario 1 Result

The password recovery workflow functioned correctly.

The system:

* Accepted the registered email address.
* Sent a password reset email.
* Provided a valid reset link.
* Displayed a password reset form.
* Allowed creation of a new password.
* Displayed a confirmation message.
* Allowed successful login using the newly created password.

### Scenario 2 Result

The system correctly rejected the unregistered email address.

Displayed message:

> Error: There is no account with that username or email address.

The system prevented the password recovery process from continuing.

---

## Expected Behavior

According to the Password Recovery Use Case:

* Users should be able to request a password reset.
* A reset link should be sent to registered email addresses.
* The reset form should open when the link is used.
* The password should be updated successfully.
* Users should be redirected to the login page.
* Unregistered email addresses should display an appropriate error message.

---

## Issues Identified

| # | Description                                            | Type                                    | Severity |
| - | ------------------------------------------------------ | --------------------------------------- | -------- |
| 1 | Error message differs from documented use case wording | Documentation Mismatch / UX Observation | Low      |

---

## Special Notes

The Password Recovery workflow is fully functional.

The complete Happy Path described in the use case is implemented and works correctly.

The only observed difference is the wording of the error message for unregistered email addresses.

Expected:

> No account found for this email.

Actual:

> There is no account with that username or email address.

Functionally, the behavior remains correct.

---

## Evidence

### TC-01-Lost-Password-Page

Password recovery page displayed successfully.

<img width="1366" height="768" alt="TC-01-Lost-Password-Page" src="https://github.com/user-attachments/assets/a35b1c18-d260-4b81-bd48-9a2d00aa4923" />

---

### TC-02-Reset-Link-Sent

Password reset request submitted successfully.

<img width="1366" height="768" alt="TC-02-Reset-Link-Sent" src="https://github.com/user-attachments/assets/1af70a39-8081-4e3a-a4f8-ff0267c14c42" />


---

### TC-03-Password-Recovery-Email

Password reset email received.

<img width="1366" height="768" alt="TC-03-Password-Recovery-Email" src="https://github.com/user-attachments/assets/124ef470-c4a0-4047-a892-e8d2ef8b15b5" />


---

### TC-04-Reset-Password-Form

Password reset form opened successfully.

<img width="1366" height="768" alt="TC-04-Reset-Password-Form" src="https://github.com/user-attachments/assets/48552e8a-04f6-454b-b802-d5aa2f5444e1" />

---

### TC-05-Password-Reset-Success

Password reset confirmation displayed.

<img width="1366" height="768" alt="TC-05-Password-Reset-Success" src="https://github.com/user-attachments/assets/7c927c20-5ac3-4501-9718-6092734b53f1" />


---

### TC-06-Login-With-New-Password

Successful login using the new password.

<img width="1366" height="768" alt="TC-06-Login-With-New-Password" src="https://github.com/user-attachments/assets/363e1c0d-d5cf-40e1-81f4-88e7cb698791" />


---

### TC-07-Unregistered-Email-Recovery

Validation of unregistered email address.

<img width="1366" height="768" alt="TC-07-Unregistered-Email-Recovery" src="https://github.com/user-attachments/assets/2e99fbc8-20cf-4ff5-ab9e-ff5357606b4a" />


---

## My Thoughts / Questions

* Should the documented error message be updated to match the actual implementation?
* Should the system display a more generic message to avoid account enumeration?
* Is there a reset-link expiration mechanism implemented as described in the use case?

---

## Action Taken

✅ Completed manual testing

✅ Verified Happy Path workflow

✅ Verified alternative scenario

✅ Documented findings

# TEST REPORT — Instructor Role: Create Account, Login & Password Recovery

**Tester:** Josué (@kamojosue09-blip)

**Hour and Date:** 1 PM June 2026

**Issue Reference:** #31

**Use Case:** Instructor Role – Create Account, Login & Password Recovery

## What I Tested

This test aimed to verify the Instructor workflows for:

* Account creation
* Login
* Password recovery

The observed behavior was compared with the Student workflows previously tested.

---

## What I Did (Steps)

### Scenario 1 — Instructor Account Registration

1. Opened the application.
2. Checked the main navigation menu.
3. Verified available registration options.
4. Opened the login page.
5. Opened the registration page through the Register link.
6. Created a new account using valid credentials.
7. Received the registration email.
8. Opened the password creation link.
9. Created a password.
10. Logged into the application.

### Scenario 2 — Instructor Login Verification

1. Logged in using the newly created account.
2. Verified the destination dashboard after login.
3. Checked available menu options.

### Scenario 3 — Instructor Password Recovery Verification

The registration workflow generated a password creation email using the same mechanism previously observed during Student testing.

The workflow successfully allowed password creation and login.

---

## What I Observed

### Registration

The application navigation provides:

* Login
* Register as Student

No visible option exists to register as an Instructor.

The registration page accessed from WordPress contains only:

* Username
* Email

No role selection is available.

### Login

After registration and login, the newly created account was redirected to:

* Home
* About
* All Surveys
* My Completed Surveys
* Student

The account appeared to behave as a Student account.

No Instructor dashboard was observed.

The profile menu only contained:

* Profile
* Logout

No Instructor-specific options were available.

### Password Recovery

The registration email contained a password creation link.

The workflow functioned successfully and behaved identically to the Student password recovery workflow previously tested.

---

## Expected Behavior

According to Issue #31:

* An Instructor registration workflow should be available.
* Instructor login should redirect to an Instructor dashboard.
* Instructor-specific behavior should be observable and testable.

---

## Is This a Problem?

| # | Description                                                    | Type                  | Severity |
| - | -------------------------------------------------------------- | --------------------- | -------- |
| 1 | No visible Instructor registration option exists               | Missing Functionality | High     |
| 2 | Registration form does not allow role selection                | Functional Limitation | High     |
| 3 | Newly created accounts are redirected to the Student dashboard | Functional Mismatch   | High     |
| 4 | No Instructor dashboard was accessible during testing          | Missing Functionality | High     |

---

## Special Notes

The application currently exposes only Student-facing functionality.

Although Issue #31 requires Instructor testing, no visible method was found to:

* Register as an Instructor
* Select the Instructor role
* Access an Instructor dashboard

All observed behavior matched the Student workflow previously tested.

---

## Evidence

<img width="1366" height="768" alt="TC-01-No-Instructor-Registration-Option" src="https://github.com/user-attachments/assets/bfcdaedd-9d10-4cfb-83bd-6a09640efe91" />


The homepage only displays:

* Login
* Register as Student

No visible Instructor registration option was found.

<img width="1366" height="768" alt="TC-02-Generic-Registration-Form" src="https://github.com/user-attachments/assets/2ea3f132-2d71-4f40-ae5f-da770a5639df" />


The registration form contains only:

* Username
* Email

No role selection (Student or Instructor) is available.

<img width="1366" height="768" alt="TC-03-Registration-Email-Received" src="https://github.com/user-attachments/assets/a52851fd-0031-495b-840e-e651b987bc1a" />


A registration email was successfully received after account creation.

<img width="1366" height="768" alt="TC-04-Password-Reset-Success" src="https://github.com/user-attachments/assets/a6d77208-76c9-413e-897e-6ce2fd26c7a3" />


The password creation/reset process completed successfully.

<img width="1366" height="768" alt="TC-05-Registration-Leads-To-Student-Dashboard" src="https://github.com/user-attachments/assets/599334ce-60ab-4dec-a736-b57a91509d02" />

After login, the newly created account was redirected to the Student dashboard instead of an Instructor dashboard.


---

## My Thoughts / Questions

* Is the Instructor registration workflow currently implemented?
* Should Instructor accounts be created through a different process?
* Are Instructor credentials provided separately for testing?
* Is the Instructor dashboard still under development?

---

## Action Taken

☑ Completed available testing

☑ Documented findings

☑ Compared behavior with Student workflows

☑ Reported missing Instructor functionality

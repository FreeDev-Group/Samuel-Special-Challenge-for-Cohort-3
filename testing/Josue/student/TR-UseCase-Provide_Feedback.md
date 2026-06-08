# TEST REPORT — Provide Feedback Use Case

**Tester:** kamojosue09-blip

**Hour and Date:** 15 June 2026

**Issue Reference:** #27

**Use Case:** Provide Feedback

---

# What I Tested

This test was conducted to verify that a student can access available surveys, complete and submit feedback successfully, receive confirmation of submission, and review completed surveys afterward.

The test also evaluated:

* Required field validation
* Survey submission confirmation
* Dashboard updates after submission
* Duplicate survey protection
* Auto-save and survey resume functionality

---

# What I Did (Steps)

## Scenario 1 — Complete and Submit a Survey

1. Logged into the Student Survey Application.
2. Navigated to **All Surveys**.
3. Verified that multiple surveys were available.
4. Opened the survey **Wise Test 2**.
5. Reviewed the survey questions.
6. Attempted to submit the survey without answering any questions.
7. Observed the validation behavior.
8. Completed all required fields.
9. Uploaded a file where required.
10. Submitted the survey.
11. Observed the confirmation message.
12. Navigated to **My Completed Surveys**.

### Evidence

**Available Surveys**

<img width="1366" height="768" alt="TC-01-Available-Surveys" src="https://github.com/user-attachments/assets/774b85c9-896f-46a7-a93a-0e6c762934ea" />

**Survey Opened**

<img width="1366" height="768" alt="TC-02-Survey-Opened" src="https://github.com/user-attachments/assets/a065bd29-16e6-4d8e-b104-6d3a2fdbd780" />

**Required Field Validation**

<img width="1366" height="768" alt="TC-03-Required-Field-Validation" src="https://github.com/user-attachments/assets/c46f22b9-3f0e-43ce-b6a6-83b0a71ccafa" />

**Survey Submitted Successfully**

<img width="1366" height="768" alt="TC-04-Survey-Submitted" src="https://github.com/user-attachments/assets/87147af5-1a6b-43b7-89d2-74f11343b85e" />

**Completed Surveys List**

<img width="1366" height="768" alt="TC-05-Completed-Surveys-List" src="https://github.com/user-attachments/assets/22d5950a-06a1-4884-9bbf-47749e63824e" />

---

## Scenario 2 — Duplicate Submission Protection

1. Attempted to open and complete the same survey again after submission.
2. Observed the system response.

### Evidence

**Duplicate Survey Protection**

<img width="1366" height="768" alt="TC-06-Duplicate-Survey-Protection" src="https://github.com/user-attachments/assets/b89620d5-cd3a-4d30-b375-4ff7a8a91ac0" />


---

## Scenario 3 — Auto-Save Verification

1. Opened another available survey.
2. Entered partial responses.
3. Left the survey before submission.
4. Returned to the survey afterward.
5. Checked for saved progress or resume notifications.

### Evidence

**No Auto-Save Observed**

<img width="1366" height="768" alt="TC-07-No-AutoSave-Observed" src="https://github.com/user-attachments/assets/85cda6b5-e11a-471a-b1f8-212f83a0f6f5" />

---

# What I Observed

## Scenario 1 Result

The survey workflow functioned successfully.

The system:

* Displayed available surveys.
* Opened the selected survey correctly.
* Prevented submission when required fields were empty.
* Accepted completed responses.
* Displayed the confirmation message:

> "You have already responded to this survey. Thank you!"

* Updated the student's completed survey history.
* Displayed the completed survey in **My Completed Surveys**.

---

## Scenario 2 Result

The system prevented duplicate survey submissions.

The following message was displayed:

> "You have already responded to this survey. Thank you!"

This behavior helps prevent duplicate feedback entries.

---

## Scenario 3 Result

No visible evidence of auto-save functionality was observed.

The use case specifies that:

> Student progress should be saved automatically and restored later.

During testing:

* No resume notification appeared.
* No incomplete survey warning appeared.
* No previously entered responses were visibly restored.

The feature may not be implemented or may not be functioning as described in the use case.

---

# Expected Behavior

According to the documented use case:

* Students should be able to access available surveys.
* Required questions should be validated before submission.
* Feedback should be securely stored.
* A confirmation message should be displayed after submission.
* Completed surveys should be reflected in the student's dashboard.
* Partial progress should be automatically saved.
* Students should be notified of incomplete surveys when returning.

---

# Is This a Problem?

| # | Description                                 | Type                             | Severity |
| - | ------------------------------------------- | -------------------------------- | -------- |
| 1 | Survey submission works correctly           | Expected Behavior                | N/A      |
| 2 | Required field validation works correctly   | Expected Behavior                | N/A      |
| 3 | Duplicate survey protection works correctly | Additional Positive Behavior     | Low      |
| 4 | Auto-save functionality was not observed    | Missing Feature / Functional Gap | Medium   |

---

# Special Notes

The core survey submission workflow operates correctly.

Positive findings:

* Survey listing works.
* Survey access works.
* Validation works.
* Submission works.
* Dashboard updates correctly.
* Duplicate survey submissions are prevented.

Potential issue:

* Auto-save functionality described in the use case could not be verified.
* No resume notification was observed.
* No incomplete survey restoration was observed.

---

# My Thoughts / Questions

* Is the auto-save functionality implemented but not visible to users?
* Should incomplete surveys generate a notification on the dashboard?
* Is there a separate workflow for restoring unfinished surveys?
* Should the use case documentation be updated if auto-save is no longer supported?

---

# Action Taken

☑ Completed manual testing

☑ Documented findings

☑ Verified survey submission workflow

☑ Verified duplicate submission protection

☑ Identified possible missing auto-save functionality

☑ Ready to continue with Review Past Feedback Use Case (#26)

# TEST REPORT — Review Past Feedback Use Case

**Tester:** kamojosue09-blip

**Hour and Date:** 9h June 2026

**Issue Reference:** #26

**Use Case:** Review Past Feedback

---

# What I Tested

This test was conducted to verify that a student can review previously submitted survey responses through the Student Survey Application.

The test focused on:

* Viewing completed surveys
* Accessing previously submitted feedback
* Reviewing response details
* Verifying visibility restrictions
* Evaluating filter functionality
* Testing alternative scenarios described in the use case

---

# What I Did (Steps)

## Scenario 1 — Review Previously Submitted Feedback

1. Logged into the Student Survey Application as a student.
2. Navigated to **My Completed Surveys**.
3. Verified that completed surveys were displayed.
4. Selected the completed survey **Wise Test 2**.
5. Opened the survey details page.
6. Reviewed the previously submitted responses.

### Evidence

**Completed Surveys Displayed**

<img width="1366" height="768" alt="TC-01-Completed-Surveys-Displayed" src="https://github.com/user-attachments/assets/8bcd5a80-aedb-4a6f-9948-892416b46f6d" />


**Survey Response Details**

<img width="1366" height="768" alt="TC-02-Review-Survey-Details" src="https://github.com/user-attachments/assets/fcc2f45b-de78-46f6-a9da-ecf92e22d93f" />

---

## Scenario 2 — Verify Filter Functionality

1. Examined the Completed Surveys page.
2. Looked for filtering options.
3. Looked for search functionality.
4. Looked for dropdown selection menus.
5. Attempted to identify any mechanism for filtering survey history.

### Evidence

**No Filter Functionality Available**

<img width="1366" height="768" alt="TC-03-No-Filter-Available" src="https://github.com/user-attachments/assets/8ba65385-3c07-401f-9dbd-57f551b0a48a" />



---

# What I Observed

## Scenario 1 Result

The system successfully displayed previously completed surveys.

The completed survey **Wise Test 2** appeared in the student's survey history.

After selecting the survey, the system displayed the submitted responses, including:

* Text Array response
* Range response
* Radio Button response
* File Upload response
* Multiple Choice response
* Time response

The student was able to review all previously submitted answers successfully.

The functionality worked as expected.

---

## Scenario 2 Result

No filtering functionality was observed during testing.

The interface did not provide:

* Search bar
* Filter button
* Dropdown filter menu
* Sorting controls

Because no filtering mechanism was available, the alternative scenario involving filter results could not be tested.

---

# Expected Behavior

According to the Review Past Feedback use case:

* Students should be able to access previously completed surveys.
* Students should be able to review their own submitted responses.
* Survey details should be displayed correctly.
* Students should be able to apply filters to their survey history.
* The system should handle filter searches that return no results.

---

# Is This a Problem?

| # | Description                                                 | Type                             | Severity |
| - | ----------------------------------------------------------- | -------------------------------- | -------- |
| 1 | Completed surveys are displayed correctly                   | Expected Behavior                | N/A      |
| 2 | Previously submitted responses can be reviewed successfully | Expected Behavior                | N/A      |
| 3 | No filtering functionality was available during testing     | Missing Feature / Functional Gap | Medium   |

---

# Special Notes

The core functionality of reviewing past feedback operates correctly.

Positive observations:

* Completed surveys are visible.
* Students can open completed surveys.
* Previously submitted answers are displayed correctly.
* Students appear to have access only to their own responses.

However, the use case documentation references filtering capabilities that were not available in the tested interface.

Because no filtering controls were present, the related alternative scenarios could not be verified.

Additionally, the alternative scenario involving a student with no completed surveys could not be tested because the test account already contained a completed survey at the time of verification.

---

# Evidence Summary

* TC-01-Completed-Surveys-Displayed
* TC-02-Review-Survey-Details
* TC-03-No-Filter-Available

---

# My Thoughts / Questions

* Is filtering functionality planned for a future release?
* Has the filtering feature been removed from the current implementation?
* Should students receive additional information such as survey completion dates or submission summaries?
* Should the use case documentation be updated if filtering is no longer supported?

---

# Action Taken

☑ Completed manual testing

☑ Verified completed survey history

☑ Verified response review functionality

☑ Documented missing filtering functionality

☑ Continued testing activities

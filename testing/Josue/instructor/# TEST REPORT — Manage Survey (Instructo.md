# TEST REPORT — Manage Survey (Instructor Role)

**Tester:** Josue (@kamojosue09-blip)

**Date and :**Hour June 13, 2026

**Issue Reference:** #33

**Use Case:** Manage Survey (Instructor Role)

---

# What I Tested

This test verifies that an Instructor can:

* Access the survey management area
* Create surveys
* Manage question types
* Edit surveys and questions
* Delete surveys
* Follow the workflow described in the Manage Survey use cases

---

# What I Did

## Scenario 1 — Access Survey Management

* Logged in using Instructor credentials
* Accessed the Instructor dashboard
* Navigated to the Surveys management section

### Result

Successfully accessed the survey management area.

---

## Scenario 2 — Create Survey

* Clicked "Add New Survey"
* Entered:

  * Title: QA Test Survey Josue
  * Description: This survey was created for manual testing of the survey management feature.
  * Start Date: 13/06/2026
  * End Date: 20/06/2026
* Published the survey

### Result

Survey was successfully created and published.

---

## Scenario 3 — Create Survey With Missing Fields

* Created a survey without entering:

  * Title
  * Description
  * Start Date
  * End Date
* Published the survey

### Result

The survey was published successfully despite required information being missing.

---

## Scenario 4 — Manage Question Types

### Multiple Choice

Created a Multiple Choice question.

### True/False

Created a True/False question.

### Short Answer

Created a Text question and used it as a Short Answer question.

### Essay

Created a Text Array question and used it as an Essay-style question.

### Result

All question types were created successfully.

---

## Scenario 5 — Create Question With Missing Fields

* Created a question without:

  * Title
  * Associated Survey
* Published the question

### Result

The question was published successfully even though required fields were missing.

---

## Scenario 6 — Cancel Question Addition

Attempted to locate a cancel option while creating a question.

### Result

No Cancel, Discard, Close, or Back functionality was available.

Unable to fully test this use case.

---

## Scenario 7 — Edit Survey

* Opened an existing survey
* Modified:

  * Survey title
  * Survey dates
* Saved changes

### Result

Survey updated successfully.

---

## Scenario 8 — Edit Question

* Opened an existing question
* Modified question content
* Saved changes

### Result

Question updated successfully.

---

## Scenario 9 — Edit Closed Survey

Attempted to locate a survey status or close functionality.

### Result

No survey closing functionality was found.

Unable to test this scenario.

---

## Scenario 10 — Delete Survey

* Moved survey to Trash
* Verified survey appeared in Trash
* Permanently deleted survey

### Result

Survey was permanently removed from the system.

---

# What I Noticed

### Positive Findings

* Instructor dashboard is accessible
* Survey creation works
* Question creation works
* Survey editing works
* Question editing works
* Survey deletion works
* Multiple question types are available

### Observations

* No Cancel functionality exists for question creation
* No survey close functionality exists
* Essay question type is not explicitly available
* Short Answer question type is not explicitly available

The closest alternatives appear to be:

* Text = Short Answer
* Text Array = Essay

---

# What Should Have Happened

According to the use cases:

* Required fields should be validated before publishing
* Question creation should support cancellation
* Closed survey behavior should be testable if implemented

---

# Is This a Problem?

| # | Short Description                                                       | Type                                      | Severity |
| - | ----------------------------------------------------------------------- | ----------------------------------------- | -------- |
| 1 | Survey can be published without required fields                         | Validation Bug                            | High     |
| 2 | Question can be published without required fields                       | Validation Bug                            | High     |
| 3 | No cancel functionality available when creating questions               | Missing Functionality                     | Medium   |
| 4 | Closed survey workflow cannot be tested because no close feature exists | Missing Functionality / Use Case Mismatch | Medium   |

---

# Special Notes

* Instructor role has access to survey management features.
* Survey deletion process worked correctly.
* Permanent deletion removed the survey completely.
* Short Answer and Essay question types are not explicitly named in the interface.
* Validation logic for survey and question creation appears incomplete.

---

# Evidence

### TC-01-Instructor-Dashboard
![TC-01-Instructor-Dashboard](TC-01-Instructor-Dashboard.png)

Screenshot showing successful Instructor dashboard access.

### TC-02-Surveys-Management-Page
![TC-02-Surveys-Management-Page](TC-02-Surveys-Management-Page.png)

Screenshot showing survey management page.

### TC-03-Create-Survey-Form
![TC-03-Create-Survey-Form](TC-03-Create-Survey-Form.png)

Screenshot showing survey creation form.

### TC-04-Survey-Created-Successfully
![TC-04-Survey-Created-Successfully](TC-04-Survey-Created-Successfully.png)

Screenshot showing successful survey publication.

### TC-04-Question-Creation-Form
![TC-04-Question-Creation-Form](TC-04-Question-Creation-Form.png)

Screenshot showing question creation form and available question types.

### TC-05-Multiple-Choice-Question
![TC-05-Multiple-Choice-Question](TC-05-Multiple-Choice-Question.png)

Screenshot showing successful Multiple Choice question creation.

### TC-06-True-False-Question-Created
![TC-06-True-False-Question-Created](TC-06-True-False-Question-Created.png)

Screenshot showing successful True/False question creation.

### TC-07-Essay-Question-Created
![TC-07-Essay-Question-Created](TC-07-Essay-Question-Created.png)

Screenshot showing successful Essay-style question creation.

### TC-08-Survey-Edit-Successfully
![TC-08-Survey-Edited-Successfully.png](TC-08-Survey-Edited-Successfully.png)

Screenshot showing successful Short Answer question creation.

### TC-09-Survey-Found-In-Trach
![TC-09-Survey-Found-In-Trash.png](TC-09-Survey-Found-In-Trash.png)

Screenshot showing successful survey modification.

### TC-10-Survey-Permanently-Deleted-1
![TC-10-Survey-Permanently-Deleted.png](TC-10-Survey-Permanently-Deleted.png)

Screenshot showing survey located in Trash.


# My Thoughts / Questions

* Are survey title and dates intended to be mandatory?
* Are question title and associated survey intended to be mandatory?
* Should users be able to cancel question creation?
* Is survey closing functionality planned for future implementation?
* Should Short Answer and Essay appear explicitly as question types?

---

# Action Taken

☑ Continued testing

☑ Identified validation issues

☑ Documented missing functionality

☑ Prepared evidence for reporting

☑ Ready to create sub-issues for valid bugs

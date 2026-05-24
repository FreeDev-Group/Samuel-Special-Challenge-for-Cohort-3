# TEST REPORT — Provide Feedback

**Tester:** Jonathan Bitingingwa

**Date:**  20h May,2026

**Issue Reference:**  #15

**Use Case:**  Provide Feedback

---

## What I am testing
This test verifies that a student can access available surveys, answer survey questions, submit responses successfully, receive a confirmation message, 
and verify that the completed survey appears in the completed surveys section.  
Verifies whether the system correctly validates mandatory survey questions and prevents survey submission when required fields are not completed.  
Verifies whether the system automatically saves survey progress when a student exits before submission and whether the student can resume from the saved point after logging in again.

## What I did (steps)

### Scenario 1 —
-I opened the application: https://student.michaelkentburns.com/  
-I logged in as a Student using valid credentials  
-I navigated to the Student dashboard  
-I went to the top menu and clicked on “All Survey”  
-I saw a page listing available surveys  
-I selected “Read the home section at MKB Web site.”  
-I opened the survey and viewed the questions  
-I answered the survey questions  
-I clicked on “Submit”  
-I received the message: “Merci, vos réponses ont bien été enregistrées !”  
-I went to the “Completed Surveys” section from the top menu  
-I verified that the completed survey appeared in the completed surveys list  
-I opened the same survey again, The system displayed: “You have already responded to this survey. Thank you!”

### Scenario 2 —
-I opened the application: https://student.michaelkentburns.com/  
-I logged in as a Student using valid credentials  
-I navigated to the “All Survey” section  
-I selected “Read about section on the MKB Web site”  
-I opened the survey questions  
-I intentionally left one or more required questions unanswered  
-I clicked on “Submit”  

### Scenario 3 —  
-I opened the application: https://student.michaelkentburns.com/  
-I logged in as a Student using valid credentials  
-I navigated to the “All Survey” section  
-I selected “Backend questions 1” survey  
-I started answering several survey questions  
-I intentionally stopped halfway before completing the survey  
-I exited/refreshed/closed the survey page without submitting  
-I logged out or closed the browser session  
-I logged back into the application  
-I returned to the same survey

---

## What I noticed
**Scenario 1 Result:**  

-Positive observations:  
-Surveys were successfully displayed in the dashboard  
-Survey opened correctly  
-Questions were answerable without issues  
-Submission worked successfully  
-Confirmation message appeared after submission  
-Completed survey was reflected in the dashboard  
-System prevented duplicate survey submission by displaying a completion notice  
Observation:  
Confirmation message after submission is displayed in French: “Merci, vos réponses ont bien été enregistrées !” while the rest of the application interface is mainly in English.  

**Scenario 2 Result:**  

The system prevented the survey from being submitted On the unanswered required question, the system displayed the message: “Please fill out this field.”
Submission could not proceed until the missing required field was completed  
After answering the missing question and submitting again, I received the message: “Merci, vos réponses ont bien été enregistrées !”

**Scenario 3 Result:**  
The previously answered survey responses were not saved, when i reopened the survey, I had to start answering the questions again from the beginning
I did not receive any resume notification or indication that progress had been saved

---

## What should have happened
Based on the use case:    
-Student should view available surveys  
-Student should answer and submit survey questions  
-System should display confirmation message after submission  
-Dashboard should reflect survey completion status  
-System should prevent duplicate submissions
All these expected behaviors worked successfully.  

-The system should validate required fields before submission  
-Submission should be blocked when mandatory questions are unanswered  
-The system should prompt the student to complete missing fields before allowing submission  
The observed behavior matched the expected behavior.  

-The system should automatically save partial survey progres  
-The student should be able to resume the survey after returning  
-The system should ideally notify the student that saved progress was restored

---

## Is this a problem?

| # | Short Description | Type | Severity |
|---|-------------------|------|----------|
| 1 |Yes, The application interface is primarily in English, French confirmation message may confuse some users and creates inconsistency in user experience|UX / Localization consistency observation|Low|
| 2 |No, No issue identified, The validation worked correctly, Required fields were enforced, Submission was blocked until completion, Clear validation message appeared|N/A|N/A| 
| 3 |YES, Survey progress is not auto-saved after exiting before submission|Bug / Missing functionality implementation|Medium–High|

---

## Special Note
-Happy path functionality works correctly from survey access to submission  
-Completed survey tracking is functional  
-Duplicate submissions appear to be prevented  
-Auto-save functionality was not verified during this test  
-Required field validation behavior still needs dedicated testing  
-Required field validation is functioning correctly  
-System prevents incomplete survey submission  
-Validation feedback is immediate and understandable  
-Confirmation message still appears in French while most of the application is in English (previous UX observation)  
-The use case explicitly mentions auto-save functionality during interruption or exit  
-No resume notification or saved draft behavior was observed  
-Partial responses were completely lost after session interruption


---

## Evidence
<img width="1366" height="2879" alt="Image" src="https://github.com/user-attachments/assets/21abb4d3-9d9e-4f6d-bb77-d34f30c53b14" /> All Surveys page
<img width="1366" height="633" alt="Image" src="https://github.com/user-attachments/assets/71f66356-a7c1-4001-8511-f374520a25fc" /> Duplicate response prevention message
<img width="1366" height="633" alt="Image" src="https://github.com/user-attachments/assets/ad28233d-9d06-4d61-80da-8b3fa1a653eb" /> Completed Surveys section
<img width="1366" height="1665" alt="Image" src="https://github.com/user-attachments/assets/2cde22b3-a533-414f-9820-5ec93814f0e8" /> Unanswered required field
<img width="1366" height="670" alt="Image" src="https://github.com/user-attachments/assets/37d95e39-461a-4b62-b0c6-4fe9667d477c" />Validation message
<img width="1366" height="1740" alt="Image" src="https://github.com/user-attachments/assets/09a9582b-f5a8-4b6d-8889-a1fe06ef67b7" />Successful submission confirmation
<img width="1366" height="1613" alt="Image" src="https://github.com/user-attachments/assets/e5e7da67-2010-48ca-b04d-8f611bb40bcd" />Before exiting survey (completed responses)
<img width="1366" height="1613" alt="Image" src="https://github.com/user-attachments/assets/2e8b7715-0953-49a6-97d6-3a4f7bb77eef" /> Survey showing responses lost

---

## My thoughts / questions
-Confirmation message after submission appeared in French while the rest of the interface is mainly in English, creating minor language inconsistency.  
-Required field validation still needs verification.  
-Validation behavior appears consistent and user-friendly  
-It would be useful to verify whether all survey question types enforce validation equally  
-Is auto-save functionality not implemented yet?  
-Is progress intended to save only after specific intervals or actions?  
-Should drafts persist across sessions automatically?

---

## Action taken
- [x] Identified issue related to missing auto-save/resume functionality
- [x] Sub-issue should be created for survey progress loss after interruption
- [x] I added the `bug` label on the sub-issue
- [x] I continued testing

Sub-issue links:

https://github.com/FreeDev-Group/Samuel-Special-Challenge-for-Cohort-3/issues/20


---

## Files
`/testing/[jonathan]/[TR-UseCase-Provide_Feedback].md`

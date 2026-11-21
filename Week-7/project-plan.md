# Week 7 – Patient Appointment Prep

## Task 1: Fork the starter application

Created and verified a personal fork of the course SMART App starter repository.

- Owner: `tyquasiah`
- Repository: [Patient-Appointment-Prep](https://github.com/tyquasiah/Patient-Appointment-Prep)
- Original repository: [samoanGuy7/Smart-App](https://github.com/samoanGuy7/Smart-App)

The fork remains separate from this coursework repository. No starter-app code was changed as part of Week 7 Task 1, consistent with the task instructions.

## Task 2: Application purpose

**Patient Appointment Prep** helps patients prepare for upcoming healthcare appointments by bringing their recent test results and recorded health conditions together in one easy-to-review summary.

- Primary user: Patient
- Main problem: Patients may need to gather and review relevant health information before an appointment.
- Proposed solution: Present key patient details, recent test results, and recorded conditions in one view.

## Task 3: FHIR resource mapping

| Information needed | FHIR resource | Details to display |
|---|---|---|
| Patient Information | `Patient` | Patient name and date of birth |
| Recent Test Results | `Observation` | Test name, result, measurement unit, and test date when available |
| Recorded Health Conditions | `Condition` | Condition name and clinical status |

Fictional examples used in the planning sketch:
- Patient: NyAsia Ashante Hill
- Date of birth: November 5, 2002
- Test result: Hemoglobin A1c, 7.2%
- Example condition: Asthma, active

The asthma entry is an illustrative planning example only, not a real diagnosis. The Week 3 Observation did not include an effective date, so no test date is invented here.

## Task 4: First-screen sketch

The first-screen concept is named **Patient Appointment Prep**. It contains three main sections:

1. **Patient Information:** Displays the patient's name and date of birth.
2. **Recent Test Results:** Displays the test name, result, unit, and date when available.
3. **Recorded Health Conditions:** Displays condition names and their clinical status.

The sketch also includes a proposed “Review Appointment Information” button.

### Essential features for the first version

1. Patient Information
2. Recent Test Results
3. Recorded Health Conditions

### Later enhancements

- Share a health summary with a healthcare provider.
- Search and filter previous laboratory results.
- Appointment reminders and preparation notes.

The first-screen sketch was created using the visual mockup provided during the project work. Keep the actual sketch image with the student's course evidence; it is not embedded in this Markdown file.

## Week 7 completion note

The fork, app-purpose statement, FHIR resource mapping, and first-screen sketch have been completed as planning activities. The starter application has not yet been modified or launched. Week 8 covers opening the starter app and identifying one improvement for a future version.

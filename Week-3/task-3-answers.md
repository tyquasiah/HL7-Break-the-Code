# Week 3 – Task 3: Inspect, Explain, and Make a Change

## 1. Patient details
The patient's name is recorded in the `name` element, which contains the given and family names. The birth date is recorded in the `birthDate` element.

## 2. JSON structure
The `name` element is an array containing the patient's name entry. Inside that array is an object with `given` and `family` elements. The `given` element is also an array containing the patient's given name or names.

## 3. Data types and cardinality
In the FHIR Patient structure:
- `name` has data type `HumanName` and cardinality `0..*` (zero or more).
- `birthDate` has data type `date` and cardinality `0..1` (zero or one).

## 4. Measurement and result
The `code` element identifies what was measured: Hemoglobin A1c. The `valueQuantity` element records the result, including the numeric value (7.2) and unit (%).

## 5. Connecting resources
The Observation uses `subject.reference` to identify the Patient resource it belongs to. The reference is `Patient/patient-001`, which points to the Patient resource with ID `patient-001`.

## Updated Patient
The updated Patient resource adds `Ashante` after `NyAsia` in the existing `given` array. The resource ID remains `patient-001`, so the Observation's patient reference remains the same.

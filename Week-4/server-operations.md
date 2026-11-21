# Week 4 – HAPI FHIR R4 Server Operations

## Patient resource

The Week 4 exercise used a fictional Patient resource for NyAsia Ashante Hill. The resource was prepared for FHIR R4 and the US Core 6.1.0 Patient profile. The HAPI FHIR server assigned the resource ID; no ID was included in the submitted JSON.

The submitted Patient JSON is in [patient.json](patient.json).

## Recorded server results

The following results were reported by the student after performing the operations in the HAPI FHIR R4 Swagger interface:

| Operation | Purpose | Reported HTTP response | Result |
|---|---|---:|---|
| POST /Patient | Create the Patient resource | 201 | Created |
| GET /Patient/{id} | Retrieve the created Patient | 200 | Retrieved; patient name and birth date matched |
| DELETE /Patient/{id} | Delete the created Patient | 200 | Successful response |

## Assigned resource identifier

- Patient ID: `854764`
- Location header: `https://hapi.fhir.org/baseR4/Patient/854764/_history/1`
- Resource version in the location header: `1`

The Patient ID above was used for the GET and DELETE operations.

## Screenshot evidence

Screenshots of the POST, GET, and DELETE responses should be retained separately and submitted as directed by the instructor. They have not been added to this repository because image files were not provided for upload.

## Privacy note

All patient details used in this exercise are fictional. Do not add real patient information, passwords, access tokens, or other credentials to this public repository.

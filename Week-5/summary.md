# Week 5 – Exploring SMART on FHIR

## Task 1: Explore the SMART App Launch specification

Reviewed SMART App Launch version 2.2.0, which is based on FHIR R4.

The three connection approaches reviewed were:
- **Standalone Launch:** An application is launched independently of an existing EHR session and must obtain authorization to access protected information.
- **EHR Launch:** An application is launched from within an existing EHR session. Authorization is still required.
- **Backend Services Authorization:** An automated service authenticates using previously approved access and obtains an access token without a person signing in during each exchange.

## Task 2: Read a SMART discovery document

Reviewed the mock server's SMART discovery document at:

`https://api.mock.health/fhir/.well-known/smart-configuration`

The project instructions identify these endpoint values:
- Authorization endpoint: `https://api.mock.health/smart/authorize`
- Token endpoint: `https://api.mock.health/smart/token`

The discovery document also advertises:
- Capabilities: `launch-ehr` and `launch-standalone`
- PKCE code challenge method: `S256`
- Supported grant types: `authorization_code`, `refresh_token`, and `client_credentials`

Opening the discovery document returns configuration information. It does not, by itself, complete an authorization flow, provide an access token, or retrieve patient records.

## Task 3: Decode scopes and patient context

Reviewed the following scope concepts:
- `patient/Observation.rs`: Read and search Observation resources for the patient in context.
- `patient/Observation.cruds`: Includes create, read, update, delete, and search permissions.
- `patient/Patient.rs`: Read and search Patient resources for the patient in context.
- `launch/patient`: Patient context supplied during a launch.
- `openid` and `fhirUser`: Identity-related scopes.

The activity distinguished the signed-in user from the patient in context. It also distinguished scopes that are supported by a server, requested by an application, and actually granted by the authorization server.

For an application that only displays existing observations, read/search access (`.rs`) is more appropriate than create/update/delete access.

## Task 4: Explore the SMART App Gallery

Explored the three applications named in the project instructions:
- CommonHealth
- ASCVD Risk Calculator
- CDS Connect: Pain Management Summary

Also selected **Caren mHealth** as the additional application explored.

### Caren mHealth – exploration notes

The app was considered as an example of using health information from connected devices and patient measurements.

Potential users: patients and clinicians.

Potential problem addressed: collecting and reviewing health measurements from connected devices in a more organized way.

Potential FHIR resources, based on the app's described purpose:
- `Patient` – identifies the patient.
- `Observation` – can represent measurements such as heart rate or blood pressure.
- `Device` – can represent a connected medical or wearable device.

These resource choices are informed inferences for the exercise, not a verified list of the application's actual API requirements. Depending on the implementation, an app of this type may need both read and write access.

### Evidence note

The student confirmed Week 5 completion and reported recording information about Caren mHealth. Screenshots were not retained for the fourth activity (the additional-app exploration). Do not represent those screenshots as available. Any screenshots saved for Tasks 1–3 should remain in the student's separate Week 5 evidence folder for submission as instructed.

## Key takeaway

SMART on FHIR provides authorization and launch patterns that allow applications to request appropriate access to FHIR resources. The discovery document advertises connection information and capabilities, while scopes express requested permissions and patient context. An application's actual access depends on what the authorization server grants.

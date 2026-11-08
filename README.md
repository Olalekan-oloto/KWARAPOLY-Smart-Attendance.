# KWARAPOLY Smart Attendance — Starter v0.1

## What this package is
A responsive, clickable front-end prototype for the proposed Kwara State Polytechnic attendance system. It previews navigation, registration fields, role dashboards, course setup, attendance records and settings.

**It is not connected to Firebase yet.** Registration data is saved only in the browser's local storage. QR creation, QR scanning, camera capture, face verification, location verification, real authentication and secure attendance writes are placeholders and are not functional in this version.

Use fictional test data only. Do not enter real student or staff records.

## Run the prototype
1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. On a phone, open the extracted folder with a local web server or upload the files to a temporary static host. Camera access generally requires HTTPS or localhost.
4. Test Overview, Registration, Dashboard, Courses & classes, Attendance and Settings.

## Next implementation stage
Create a NEW Firebase project dedicated to KWARAPOLY. Do not reuse the MuizMarket Firebase project.
Enable:
- Email/password Authentication
- Cloud Firestore
- Firebase Storage
- Cloud Functions (for trusted QR/session validation and privileged actions)
- App Check

Then implement and test the database schema, role provisioning, admin approval, official academic catalogue, student/course enrolment, signed short-lived QR sessions, duplicate prevention, audit logs and privacy/retention controls.

## Production safeguards
- Do not allow users to self-assign Super Admin or Lecturer privileges.
- Admin accounts must be provisioned securely, not through public registration.
- Validate matric numbers against an approved school roster or registrar-provided data.
- Do not trust browser time, browser location, or client-written attendance status.
- QR tokens must be random, short-lived, session-bound and validated server-side.
- Face matching/liveness is not included. A selfie capture alone is not identity verification.
- Location should be optional and proportionate, with clear notice and an alternative process for students who cannot share location.
- Keep an audit trail for attendance edits and admin actions.
- Confirm the Polytechnic's official logo, institute/department list, course catalogue and data-protection requirements before launch.

## Included files
- `index.html` — responsive prototype
- `firestore.rules` — deny-by-default starter rules (intentionally not production-ready)
- `README.md` — setup and implementation notes

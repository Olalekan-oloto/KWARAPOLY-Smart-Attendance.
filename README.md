# KWARAPOLY Smart Attendance — Rebuild v1.0

This is a fresh mobile-responsive application foundation for the proposed KWARAPOLY Smart Attendance System.

## Open the prototype
1. Upload the contents of this folder to the root of a GitHub repository.
2. In GitHub, open Settings → Pages.
3. Under Build and deployment, select Deploy from a branch.
4. Select `main` and `/ (root)`, then Save.
5. Open the Pages URL GitHub provides.

## What works in this version
- Responsive dashboard and navigation.
- Preview role selector for Super Admin, Lecturer and Student.
- Fictional student record entry in the current browser session.
- Course catalogue entry in the current browser session.
- Preview attendance session creation.
- Preview announcements.
- Academic structure, report and security requirement screens.

## What is NOT live yet
This is a front-end development foundation, not an approved production attendance system. It does not yet provide real authentication, persistent database writes, server-validated QR attendance, live camera scanning, face matching/liveness, secure exports, or production role permissions. Preview records are held only in browser memory and disappear when the page is refreshed.

## Production build requirements
- Dedicated Firebase project (do not reuse another business app project).
- Firebase Authentication with verified accounts.
- Firestore schema and reviewed security rules.
- Cloud Functions for privileged actions, short-lived random QR tokens, attendance validation and audit logging.
- App Check and rate limiting.
- Approved school roster and course-registration imports.
- Consent, data minimization, retention/deletion policy and an accessible alternative to camera verification.
- Official KWARAPOLY approval, branding and academic directory validation before real deployment.

## Safety
Use fictional test data only. Do not upload real student records, photographs, biometric templates, passwords, or staff data to this prototype or a public GitHub repository. Do not deploy the deny-all Firestore rules as a substitute for a completed security design; they intentionally block all client access.

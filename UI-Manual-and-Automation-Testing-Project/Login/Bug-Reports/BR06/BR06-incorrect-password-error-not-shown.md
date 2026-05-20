# BR06 – Incorrect Password: Expected Error Message Not Displayed

## Summary
When logging in with a valid email and an incorrect password, Koel does not display the expected validation message. Instead, the login form shakes and shows a red outline, but no text feedback is provided.

## Environment
- QA – Koel
- https://qa.koel.app
- Version: v5.1.20

## Steps to Reproduce
1. Navigate to https://qa.koel.app/
2. Enter a valid email address (e.g., anita.surewicz@testpro.io)
3. Enter an incorrect password
4. Click “Log in”

## Expected Result
Koel displays the message: “Couldn't log you in.”

## Actual Result
- No “Couldn't log you in” message appears.
- Login form briefly shakes and shows a red outline.
- No text feedback is provided.
- User remains on the Login page.

## Impact
- Users receive no clear explanation for failed login attempts.
- UI validation is inconsistent across error scenarios.
- Automated tests cannot locate a CSS‑selectable error element.

## Evidence

- Screenshot: [TC06 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR06/TC06-incorrect-password-shows-error_IJ.png)
- Screenshot: [TC06 – IntelliJ Login Attempt (Valid Email + Invalid Password)](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR06/TC06-valid-email-invalid-password-shows-error_IJ.png)
- Screenshot: [TC06 – UI Error State](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR06/TC06-incorrect-password-shows-error_UI.png)

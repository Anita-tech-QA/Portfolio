# TC04 – Invalid Email (Missing Dot Symbol)

## Preconditions
- User is registered with a valid testpro.io email.
- User has a valid password for the registered account.
- User is on the Koel Login page: https://qa.koel.app/

## Test Steps
1. Enter an invalid email missing the dot symbol (e.g., anita.surewicz@testproio).
2. Enter a valid password.
3. Click the “Log in” button.

## Expected Result
- The UI displays the message: “Email format is incorrect.”
- User remains on the Login page.

## Actual Result 
- No “Email format is incorrect” message is displayed.
- The login form briefly shakes and shows a red outline.
- No text feedback is provided.
- User remains on the Login page.

## Status
❌ FAIL

## Traceability
- Automation Test: [TC04 Automation](/UI-Manual-and-Automation-Testing-Project/Login/Automation/AT04-invalid-email-no-dot-symbol-test.md)
- Bug Report: [BR04 – Missing Dot Symbol](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR04/BR04-missing-dot-symbol-expected-error-message-not-shown.md)

## Evidence

- Screenshot: [TC04 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR04/TC04-missing-dot-symbol_IJ.png)
- Screenshot: [TC04 – UI Red Outline / Shake](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR04/TC04-missing-dot-symbol_UI.png)

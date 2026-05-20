# TC03 – Invalid Email (Missing @ Symbol)

## Preconditions
- User is registered with a valid testpro.io email.
- User has a valid password for the registered account.
- User is on the Koel Login page: https://qa.koel.app/

## Test Steps
1. Enter an invalid email missing the @ symbol (e.g., anita.surewicztestpro.io).
2. Enter a valid password.
3. Click the “Log in” button.

## Expected Result
- The UI displays the message: “Email format is incorrect.”
- User remains on the Login page.

## Actual Result 
- No “Email format is incorrect” message is displayed.
- Browser shows native HTML5 tooltip:  
  “Please include an '@' in the email address…”

## Status
❌ FAIL

## Traceability
- Automation Test: [AT03 Automation](/UI-Manual-and-Automation-Testing-Project/Login/Automation/AT03-invalid-email-no-at-symbol-test.md)
- Bug Report: [BR03 – Missing @ Symbol](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR03/BR03-missing-at-symbol-expected-error-message-not-shown.md)

## Evidence

- Screenshot: [TC03 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR03/TC03-missing-at-symbol_IJ.png)
- Screenshot: [TC03 – Browser Tooltip Message](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR03/TC03-missing-at-symbol-tooltip_UI.png)

# TC02 – Invalid Email (Missing Domain)

## Preconditions
- User is registered with a valid testpro.io email.
- User has a valid password for the registered account.
- User is on the Koel Login page: https://qa.koel.app/

## Test Steps
1. Enter an invalid email missing the domain (e.g., anita.surewicz@).
2. Enter a valid password.
3. Click the “Log in” button.

## Expected Result
- The UI displays the message: “Email format is incorrect.”
- User remains on the Login page.

## Actual Result 
- No “Email format is incorrect” message is displayed.
- Browser shows native HTML5 tooltip:  
  “Please enter a part following '@'. 'anita.surewicz@' is incomplete.”

## Status
❌ FAIL

## Traceability
- Automation Test: [TC02 Automation](/UI-Manual-and-Automation-Testing-Project/Login/Automation/AT02-invalid-email-no-domain-test.md)
- Bug Report: [BR02 – Invalid Email Missing Domain](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR02/BR02-missing-domain-expected-error-message-not-shown.md)

## Evidence
- Screenshot: [TC02 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR02/TC02-missing-domain_IJ.png)
- Screenshot: [TC02 – Browser Tooltip Message](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR02/TC02-missing-domain-tooltip.png)

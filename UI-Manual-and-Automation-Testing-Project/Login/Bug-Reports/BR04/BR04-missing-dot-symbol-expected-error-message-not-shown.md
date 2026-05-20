# BR04 – Missing Dot Symbol: Expected Error Message Not Displayed

## Summary
When logging in with an email missing the dot symbol, Koel does not display the expected validation message.  
Instead, the login form shakes and shows a red outline, but no text feedback is provided.

## Environment
- QA – Koel
- https://qa.koel.app
- Version: v5.1.20

## Steps to Reproduce
1. Navigate to https://qa.koel.app/
2. Enter an invalid email missing the dot symbol (e.g., anita.surewicz@testproio)
3. Enter a valid password
4. Click “Log in”

## Expected Result
Koel displays the message: “Email format is incorrect.”

## Actual Result
- No “Email format is incorrect” message appears.
- Login form briefly shakes and shows a red outline.
- No text feedback is provided.
- User remains on the Login page.

## Impact
- UI validation is inconsistent across invalid email formats.
- Users receive visual feedback only (shake + red outline), not a clear error message.
- Automated tests cannot locate a CSS‑selectable error element.

## Evidence

- Screenshot: [TC04 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR04/TC04-missing-dot-symbol_IJ.png)
- Screenshot: [TC04 – UI Error State](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR04/TC04-missing-dot-symbol_UI.png)

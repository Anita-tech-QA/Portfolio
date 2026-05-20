# BR03 – Missing @ Symbol: Expected Error Message Not Displayed

## Summary
When logging in with an email missing the @ symbol, Koel does not display the expected validation message. Instead, the browser shows a native HTML5 tooltip.

## Environment
- QA – Koel  
- https://qa.koel.app  
- Version: v5.1.20

## Steps to Reproduce
1. Navigate to https://qa.koel.app/
2. Enter an invalid email missing the @ symbol (e.g., anita.surewicztestpro.io)
3. Enter a valid password
4. Click “Log in”

## Expected Result
- Koel displays the message: “Email format is incorrect.”

## Actual Result
- No “Email format is incorrect” message appears.
- Browser displays native tooltip:  
  “Please include an '@' in the email address…”

## Impact
- UI validation is inconsistent.
- Users receive browser-level feedback instead of application-level messaging.

## Evidence

- Screenshot: [TC03 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR03/TC03-missing-at-symbol_IJ.png)
- Screenshot: [TC03 – Browser Tooltip Message](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR03/TC03-missing-at-symbol-tooltip_UI.png)

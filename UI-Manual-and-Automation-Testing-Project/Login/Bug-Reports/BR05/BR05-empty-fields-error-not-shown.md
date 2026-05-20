# BR05 – Empty Fields: Expected Error Message Not Displayed

## Summary
When attempting to log in with both email and password fields left empty, Koel does not display the expected validation message.  
Instead, the browser shows a native HTML5 tooltip.

## Environment
- QA – Koel
- https://qa.koel.app
- Version: v5.1.20

## Steps to Reproduce
1. Navigate to https://qa.koel.app/
2. Leave the email field blank
3. Leave the password field blank
4. Click “Log in”

## Expected Result
Koel displays the message: “Email format is incorrect.”

## Actual Result
- No “Email format is incorrect” message appears.
- Browser displays native tooltip:  
  “Please fill out this field”
- User remains on the Login page.

## Impact
- UI validation is inconsistent across invalid input scenarios.
- Users receive browser‑level feedback instead of application‑level messaging.
- Automated tests cannot locate a CSS‑selectable error element.

## Evidence

- Screenshot: [TC05 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR05/TC05-empty-fields_IJ.png)
- Screenshot: [TC05 – Browser Tooltip Message](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR05/TC05-empty-fields-tooltip_UI.png)

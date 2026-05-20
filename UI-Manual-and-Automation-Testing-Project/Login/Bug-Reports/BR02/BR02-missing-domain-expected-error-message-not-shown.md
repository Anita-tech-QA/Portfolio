# BR02 – Missing Domain: Expected Error Message Not Displayed

## Summary
When logging in with an email missing the domain, Koel does not display the expected validation message.  
Instead, the browser shows a native HTML5 tooltip.

## Environment
- QA – Koel  
- https://qa.koel.app  
- Version: v5.1.20

## Steps to Reproduce
1. Navigate to https://qa.koel.app/
2. Enter an invalid email missing the domain (e.g., anita.surewicz@)
3. Enter a valid password
4. Click “Log in”

## Expected Result
Koel displays the message: “Email format is incorrect.”

## Actual Result
- No “Email format is incorrect” message appears.  
- Browser displays native tooltip:  
  “Please enter a part following '@'. 'anita.surewicz@' is incomplete”

## Impact
- UI validation is inconsistent.  
- Users receive browser‑level feedback instead of application‑level messaging.  
- Automated tests cannot locate a CSS‑selectable error element.

## Evidence

- Screenshot: [TC02 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR02/TC02-missing-domain_IJ.png)
- Screenshot: [TC02 – Browser Tooltip Message](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR02/TC02-missing-domain-tooltip_UI.png)

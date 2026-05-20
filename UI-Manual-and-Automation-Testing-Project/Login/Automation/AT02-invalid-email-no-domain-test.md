# TC02 – Invalid Email (Missing Domain) – Automation

## Traceability
- Manual Test: [TC02 – Invalid Email (Missing Domain)](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC02-invalid-email-no-domain.md)
- Bug Report: [BR02 – Missing Domain Error Message Not Shown](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR02/BR02-missing-domain-expected-error-message-not-shown.md)
  
## Scenario
Validate that Koel displays the correct error message when the user enters an email address missing the domain.

## Automation Logic
- Navigate to https://qa.koel.app/
- Enter invalid email: anita.surewicz@
- Enter valid password
- Click “Log In”
- Assert:
  - User remains on the Login page
  - (Attempted) Expected Koel validation message: "Email format is incorrect"

## Automation Result
- Confirmed: User remained on the Login page
- Not Confirmed: Expected Koel validation message

## Reason
Koel does not render a CSS‑selectable validation message for this error state.  
Only the browser’s native HTML5 tooltip appears, which cannot be located via Selenium.

# TC04 – Invalid Email (Missing Dot Symbol) – Automation

## Traceability
- Manual Test: [TC04 – Invalid Email (Missing Dot Symbol)](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC04-invalid-email-no-dot-symbol.md)
- Bug Report: [BR04 – Missing Dot Symbol Error Message Not Shown](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR04/BR04-missing-dot-symbol-expected-error-message-not-shown.md)
  
## Scenario
Validate that Koel displays the correct error message when the user enters an email address missing the dot symbol.

## Automation Logic
- Navigate to https://qa.koel.app/
- Enter invalid email: anita.surewicz@testproio
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
The login form shakes and shows a red outline, but no text message is displayed.  
Selenium cannot locate any error element.

# TC06 – Valid Email and Incorrect Password – Automation

## Traceability
- Manual Test: [TC06 – Valid Email and Incorrect Password](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC06-valid-email-and-incorrect-password.md)
- Bug Report: [BR06 – Incorrect Password Error Not Shown](/UI-Manual-and-Automation-Testing-Project/Login/Bug-Reports/BR06/BR06-incorrect-password-error-not-shown.md)

## Scenario
Validate that Koel displays the correct error message when the user enters a valid email but an incorrect password.

## Automation Logic
- Navigate to https://qa.koel.app/
- Enter valid email: anita.surewicz@testpro.io
- Enter incorrect password
- Click “Log In”
- Assert:
  - User remains on the Login page
  - (Attempted) Expected Koel validation message: "Couldn't log you in"

## Automation Result
- Confirmed: User remained on the Login page
- Not Confirmed: Expected Koel validation message

## Reason
Koel does not render a CSS‑selectable validation message for incorrect passwords.  
The login form shakes and shows a red outline, but no text message is displayed.  
Selenium cannot locate any error element.

# TC01 – Valid Email and Password – Automation

## Traceability
- Manual Test: [TC01 – Valid Email and Password](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC01/TC01-valid-email-and-password.md)

## Scenario
Validate that Koel successfully logs in a user with a valid email and correct password.

## Automation Logic
- Navigate to https://qa.koel.app/
- Enter valid registered email: anita.surewicz@testpro.io
- Enter correct password
- Click “Log In”
- Assert:
  - User is successfully logged in
  - User is redirected to the Homepage

## Automation Result
- Confirmed: User successfully logged in
- Confirmed: User was redirected to the Homepage

## Reason
This test validates the positive login flow and confirms that Koel correctly authenticates valid credentials.

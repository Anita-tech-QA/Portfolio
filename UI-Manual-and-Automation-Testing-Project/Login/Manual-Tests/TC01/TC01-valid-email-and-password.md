
# TC01 – Valid Email and Password

## Preconditions
- User is registered with a valid testpro.io email.
- User has a valid password for the registered account.
- User is on the Koel Login page: https://qa.koel.app/

## Test Steps
1. Enter a valid registered email (e.g., anita.surewicz@testpro.io).
2. Enter the correct password.
3. Click the “Log in” button.

## Expected Result
- User is successfully logged in.
- User is redirected to the Homepage.

## Actual Result (from execution)
- User successfully logged in.
- User was redirected to the Homepage.

## Status
🟢 PASS

## Traceability
- Automation Test:  
  [AT01 Automation](/UI-Manual-and-Automation-Testing-Project/Login/Automation/TC01/AT01-valid-login-test.md)

## Evidence
- [UI Before Login](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC01/TC01-valid-email-password-before-login_UI.png)
- [UI After Login](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC01/TC01-valid-email-password-after-login_UI.png)
- [IntelliJ – Passed](/UI-Manual-and-Automation-Testing-Project/Login/Automation/TC01/TC01-valid-login-test_IJ.png)

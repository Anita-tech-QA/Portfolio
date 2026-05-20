# TC07 – Login Redirects User to Previously Saved Page

## Preconditions
- User is registered with a valid testpro.io email.
- User is logged out.
- User attempts to access a protected page directly: https://qa.koel.app/#/albums

## Test Steps
1. Attempt to access the protected URL: https://qa.koel.app/#/albums.
2. Observe that the user is redirected to the Login page.
3. Enter a valid registered email.
4. Enter the correct password.
5. Click the “Log in” button.

## Expected Result
- User is successfully logged in.
- User is redirected to the previously saved URL (/albums).
- User is not taken to the default Homepage.

## Actual Result (from execution)
- User was successfully logged in.
- User was redirected to the saved URL (/albums).
- User was not taken to the Homepage.

## Status
🟢 PASS

## Traceability
- Automation Test:  
  [TC07 Automation](/UI-Manual-and-Automation-Testing-Project/Login/Automation/TC07/AT07-login-redirects-to-saved-page-test.md)

## Evidence
- [UI Before Redirect Login](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC07/TC07-before-redirect-login_UI.png)
- [UI After Redirect Login](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC07/TC07-after-redirect-login_UI.png)
- [IntelliJ – Passed](/UI-Manual-and-Automation-Testing-Project/Login/Automation/TC07/TC07-login-redirect-to-saved-page-test_IJ.png)

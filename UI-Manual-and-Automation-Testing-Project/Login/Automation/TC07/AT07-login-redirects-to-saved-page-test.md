# TC07 – Login Redirects User to Previously Saved Page – Automation

## Traceability
- Manual Test: [TC07 – Login Redirects to Previously Saved Page](/UI-Manual-and-Automation-Testing-Project/Login/Manual-Tests/TC07/TC07-login-redirects-to-previously-saved-page.md)

## Scenario
Validate that when a logged‑out user attempts to access a protected page, Koel redirects them to the Login page, and after successful login, returns them to the originally requested URL.

## Automation Logic
- Navigate directly to https://qa.koel.app/#/albums while logged out.
- Assert that the user is redirected to the Login page.
- Enter valid registered email: anita.surewicz@testpro.io
- Enter correct password
- Click “Log In”
- Assert:
  - User is successfully logged in
  - User is redirected to the saved URL (/albums)
  - User is not redirected to the Homepage

## Automation Result
- Confirmed: User was redirected to the Login page when accessing a protected URL.
- Confirmed: User successfully logged in.
- Confirmed: User was redirected to the previously saved page (/albums).
- Confirmed: User was not taken to the Homepage.

## Reason
This test validates Koel’s redirect logic for protected routes.  
The application correctly preserved the intended destination and returned the user to it after authentication.

# TC02 – User is redirected to Login page after logout – Automation

## Traceability
- Manual Test: [TC01 – User is Redirected to Login Page After Logout](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC02/TC02-user-is-redirected-to-loginpage-after-logout.md)

## Scenario
Validate that Koel correctly ends the user session and redirects the user to the **Login page** after clicking the **“Log student out”** button on the Home Page.

## Automation Logic
1. Navigate to https://qa.koel.app/
2. Enter valid registered email: anita.surewicz@testpro.io
3. Enter correct password
4. Click **“Log In”**
5. Confirm the user is on the Home Page
6. Click the **“Log student out”** button
7. Assert:
   - User is redirected to the Login page
   - User session is terminated (logout successful)

## Assertions
- Confirmed: User was redirected to the Login page  
- Confirmed: User was logged out of the application

## Automation Result
Confirmed: User was redirected to the Login page  
Confirmed: User session ended successfully

## Reason
This test validates the logout flow and ensures Koel properly terminates the user session and returns the user to the Login page. It confirms correct session handling and supports regression coverage for authentication and logout functionality.

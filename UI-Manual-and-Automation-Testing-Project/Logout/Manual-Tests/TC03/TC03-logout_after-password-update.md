# TC03 – User can log out after updating password

## Preconditions
- User is registered with a valid **testpro.io** email.
- User has a valid password for the registered account.
- User is logged in and on the Koel Home Page: https://qa.koel.app/#!/home
- User has navigated to the Profile page: https://qa.koel.app/#!/profile
- User has successfully updated their password.

## Test Steps
1. Confirm the user is on the Profile page after updating their password.
2. Click the **“Log student out”** button located in the top navigation bar.

## Expected Result
- User is logged out of the application.
- User session is terminated.

## Actual Result
- User was logged out successfully.
- Session ended and user was no longer authenticated.

## Status
🟢 **PASS**

## Traceability
- Jira Test: *Koel | Log out | User can log out after updating password*
- Related Story: Logout Functionality
- Regression Area: Authentication, Profile Management

## Evidence
- UI – Password update confirmation  
- UI – Logout action  
- Automation – IntelliJ execution result

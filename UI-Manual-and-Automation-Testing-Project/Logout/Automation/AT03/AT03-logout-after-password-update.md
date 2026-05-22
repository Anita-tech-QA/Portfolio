# TC03 – User can log out after updating password – Automation

## Traceability
Manual Test: **TC03 – User can log out after updating password**

## Scenario
Validate that after a user successfully updates their password on the Profile page, Koel still allows the user to log out properly using the **“Log student out”** button in the top navigation bar.

## Automation Logic
1. Log in to the Koel application using valid credentials.
2. Navigate to the Profile Page: https://qa.koel.app/#!/profile
3. Update the user’s password with a valid new password.
4. Save the updated password and confirm the **“Profile updated”** notification appears.
5. Locate the top navigation bar.
6. Click the **“Log student out”** button.
7. Assert that:
   - The user is logged out of the application.
   - The session is terminated.
   - The user is redirected to the Login page.

## Assertions
- Confirmed: Password was successfully updated.
- Confirmed: User was logged out of the application.
- Confirmed: User was redirected to the Login page.

## Automation Result
Confirmed: Password update was successful  
Confirmed: Logout action completed  
Confirmed: User was redirected to the Login page

## Reason
This automation test validates that Koel maintains correct session handling after a password update. It ensures that the logout functionality remains stable and accessible even after account changes, supporting regression coverage for authentication, profile management, and session termination.

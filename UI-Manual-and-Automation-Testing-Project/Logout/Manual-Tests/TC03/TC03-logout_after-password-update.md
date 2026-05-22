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
- Automation test: [AT02 Automation](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT03/AT03-logout-after-password-update.md)
  
## Evidence
- Screenshot: [TC03 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT03/TC03-logout-after-password-update_IJ.png)
- Screenshot: [TC03 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT03/TC03-logout-redirect-correct-url_IJ.png)
- Screenshot: [TC03 – Profile Page](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC03/TC03-profile-page_UI.png)
- Screenshot: [TC01 – After Logout](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC02/TC02-after-logout_UI.png)
- Screenshot: [TC01 – After Logout](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC02/TC02-after-logout_UI.png)

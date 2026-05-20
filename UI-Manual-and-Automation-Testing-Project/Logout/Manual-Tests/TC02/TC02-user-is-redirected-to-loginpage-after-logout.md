# TC02 – User is redirected to Login page after logout

## Preconditions
- User is registered with a valid **testpro.io** email.
- User has a valid password for the registered account.
- User is logged in and on the Koel Home Page: https://qa.koel.app/#!/home

## Test Steps
1. Ensure the user is on the Home Page after successful login.
2. Click the **“Log student out”** button located in the top navigation bar.

## Expected Result
- User is redirected to the **Login page**.
- User is fully **logged out** of the application (session ended).

## Actual Result
- User was redirected to the Login page.
- User session ended successfully.

## Status
🟢 **PASS**

## Traceability
- Automation test: [AT02 Automation](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT02/AT02-user-is-redirected-to-loginpage-after-logout.md)
  
## Evidence
- Screenshot: [TC02 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT02/TC02-logout-possible_IJ.png)
- Screenshot: [TC01 – Before Logout](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC02/TC02-before-logout_UI.png)
- Screenshot: [TC01 – After Logout](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC02/TC02-after-logout_UI.png)


# TC04 – **User cannot re‑enter the application using the browser Back button after logout**

## Preconditions
- User has a valid **testpro.io** account.
- User is logged in and on the Koel Home Page: https://qa.koel.app/#!/home
- Browser Back button is available.

## Test Steps
1. Click the **“Log student out”** button.
2. Verify the user is redirected to the **Login Page**.
3. Press the browser **Back** button.

## Expected Result
- User is fully logged out.
- Pressing the **Back** button does **not** return the user to the authenticated Home Page.
- Application remains on the **Login Page** and prevents re‑entry.

## Actual Result
- User was logged out successfully.
- Pressing the **Back** button did **not** restore access.
- Application stayed on the Login Page as expected.

## Status  
🟢 **PASS**

## Traceability
- Automation test: [AT04 Automation](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT04/AT04-user-cannot-reenter-app-after-logout.md)
  
## Evidence
- Screenshot: [TC03 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT03/TC03-logout-after-password-update_IJ.png)
- Screenshot: [TC04 – IntelliJ Execution Result](/UI-Manual-and-Automation-Testing-Project/Logout/Automation/AT04/TC04-user-cannot-reenter-app-after-logout_IJ.png)
- Screenshot: [TC04 – Profile Page](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC04/TC04-homepage-before-logout_UI.png)
- Screenshot: [TC04 – Profile Page](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC04/TC04-UI-after-logout-and-back-button_UI.png)

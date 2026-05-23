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
- Automation test: **[Logout re‑entry prevention](ca://s?q=Open_logout_reentry_prevention_test)**

## Evidence
- Screenshot: **[TC02 – IntelliJ Execution Result](ca://s?q=Open_TC02_IntelliJ_execution_result)**
- Screenshot: 

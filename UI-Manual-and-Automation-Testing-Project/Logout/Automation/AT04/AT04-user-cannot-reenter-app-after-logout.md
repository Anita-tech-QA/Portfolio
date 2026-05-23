# AT04 – **User cannot re‑enter the application after logout using the browser Back button – Automation**

## Traceability
- Manual Test: [TC04 – User Cannot Reenter App After Logout](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC04/TC04-user-cannot-reenter-app-after-logout.md)

## Scenario
Validate that after a user logs out of Koel, pressing the browser **Back** button does not allow the user to re‑enter the application.

## Automation Logic
1. Log in to the Koel application using valid credentials.
2. Click the **“Log student out”** button.
3. Verify the user is redirected to the **Login Page**.
4. Press the browser **Back** button.
7. Assert that:
   - The user is **not** returned to the Home Page.
   - The session remains terminated.

## Assertions
- ✔️ Confirmed: User was logged out of the application.  
- ✔️ Confirmed: Pressing the Back button did **not** restore access.  

## Automation Result
- **Confirmed:** Logout action completed  
- **Confirmed:** Back‑button navigation was blocked  

## Reason
This automation test verifies that Koel correctly prevents re‑entry into authenticated pages after logout.  
It ensures proper session invalidation and supports regression coverage for **authentication** and **session termination**.

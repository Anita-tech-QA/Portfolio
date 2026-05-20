# AT01 – “Log student out” button appears near “Profile” button on Home Page – Automation

## Traceability
- Manual Test: [TC01 – Logout Button Appears Next to Profile Button](/UI-Manual-and-Automation-Testing-Project/Logout/Manual-Tests/TC01/TC01-logout-button-visible-near-profile-button.md)
  
## Scenario
Validate that Koel displays the **“Log student out”** button in the top navigation bar immediately next to the **“Profile”** button after a successful login.

## Automation Logic
1. Log in to the Koel application using valid credentials.
2. Navigate to the Home Page: https://qa.koel.app/#!/home
3. Locate the top navigation bar.
4. Identify the **Profile** button.
5. Assert that the **“Log student out”** button:
   - is visible  
   - appears directly next to the **Profile** button

## Assertions
- Confirmed: “Log student out” button is displayed.
- Confirmed: Button appears next to the “Profile” button in the navigation bar.

## Automation Result
Confirmed: “Log student out” button was displayed  
Confirmed: Button appeared next to the “Profile” button

## Reason
This automation test validates the presence and correct placement of the logout button, ensuring that users can clearly and consistently access the logout functionality from the Home Page. It confirms UI stability and supports regression coverage for navigation elements.

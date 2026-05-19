# TC04 - Koel | Artists | UI Artist List Matches Database Records

## Preconditions
- User is registered and logged into Koel: https://qa.koel.app/#!/home  
- User navigates to the Artists page: https://qa.koel.app/#!/artists  
- Access to the database is available  
- Artists exist in the database with valid metadata  

## Test Data
- SQL Query: SELECT * FROM artists ORDER BY name ASC;  
- Expected DB artist list: Enter Value...  
- Expected UI artist list: Enter Value...

## Steps
1. Log into DBeaver  
2. Execute the SQL query: SELECT * FROM artists ORDER BY name ASC;  
3. Review the list of artists returned by the database  
4. Navigate to https://qa.koel.app/#!/artists  
5. Compare the UI artist list with the DB artist list  
6. Check for missing artists or extra artists in the UI  

## Expected Result
- The UI displays all artists returned by the database.  
- No additional artists appear in the UI.  
- No artists are missing from the UI.

## Actual Result
- UI does not reflect the artists in the database.  
- "Various Artists" appears in the DB but does not appear on the Artists page.

## Status
❌ **Failed**

## Evidence
- Screenshot: [TC04-1](/Manual-Testing-Project/Evidence/TC04-1.png)
- Screenshot: [TC04-2](/Manual-Testing-Project/Evidence/TC04-2.png)
- Screenshot: [TC04-3](/Manual-Testing-Project/Evidence/TC04-3.png)
- Screenshot: [TC04-4](/Manual-Testing-Project/Evidence/TC04-4.png)   
- Related Bug Report: [BR04-ARTISTS-UI-Does-Not-Reflect-DB-Artists.md](../Bug-Reports/BR04-ARTISTS-UI-Does-Not-Reflect-DB-Artists.md)

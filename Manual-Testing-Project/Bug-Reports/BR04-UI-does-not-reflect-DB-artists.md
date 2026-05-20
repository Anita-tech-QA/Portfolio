# Bug Report: Koel | Artists | UI does not reflect the artists in the DB

## Summary
The Artists page does not display all artists that exist in the database.  
The UI is missing artists that appear in the DB records, resulting in inconsistent and incomplete artist listings.

## Environment
Application: Koel  
Environment: QA  
URL: https://qa.koel.app/#!/artists  
Module: Artists

## Preconditions
- Valid Koel user account  
- User is logged into the application  
- Access to the database is available  
- Artists exist in the database with valid metadata  

## Steps to Reproduce
1. Log into DBeaver  
2. Run the SQL query: SELECT * FROM artists ORDER BY name ASC;  
3. Review the list of artists returned by the database  
4. Navigate to https://qa.koel.app/#!/artists  
5. Compare the UI artist list with the DB artist list  

## Expected Result
- UI reflects the artists in the database.  
- All artists returned by the DB appear in the UI, and no artists are missing.

## Actual Result
- UI does not reflect the artists in the database.  
- "Various Artists" appears in the DB but does not appear on the Artists page.

## Evidence
- Screenshot: [TC04-1](/Manual-Testing-Project/Evidence/TC04-1.png)
- Screenshot: [TC04-2](/Manual-Testing-Project/Evidence/TC04-2.png)
- Screenshot: [TC04-3](/Manual-Testing-Project/Evidence/TC04-3.png)
- Screenshot: [TC04-4](/Manual-Testing-Project/Evidence/TC04-4.png)   

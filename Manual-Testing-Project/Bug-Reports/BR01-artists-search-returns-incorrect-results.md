# Bug Report: Koel | Artists | User is not able to find the correct artist in the search function

## Summary
The Artists search functionality does not correctly filter results when entering a full or partial valid artist name.  
Non‑matching artists appear for a full search, and no results appear for a partial search, even when matching artists exist.

## Environment
- Application: Koel  
- Environment: QA  
- URL: https://qa.koel.app/#!/home  
- Module: Artists Search  

## Preconditions
- Valid Koel user account  
- User is logged into the application  
- Artists exist in the database (e.g., Lobo Loco, Robert)

## Steps to Reproduce
1. Log into Koel: https://qa.koel.app/#!/home  
2. Type a valid artist name **“Lobo Loco”** into the search field  
3. Delete the artist name  
4. Enter a partial valid artist name **“Robert”** into the search field  

## Expected Result
- When entering **“Lobo Loco”**, only the matching artist is displayed and non‑matching artists are not displayed.  
- When entering **“Robert”**, relevant matching artists are displayed and non‑matching artists are not displayed.

## Actual Result
- Full artist search **“Lobo Loco”** displays additional non‑matching artists (The Blank Tapes, Defunct by Metre).  
- Partial artist search **“Robert”** returns **no results**, even though matching artists exist.

## Evidence
- Screenshot: [TC01-1](/Manual-Testing-Project/Evidence/TC01-1.png) 
- Screenshot: [TC01-2](/Manual-Testing-Project/Evidence/TC01-2.png)  
- Screenshot: [TC01-3](/Manual-Testing-Project/Evidence/TC01-3.png)  
- Screenshot: [TC01-4](/Manual-Testing-Project/Evidence/TC01-4.png)

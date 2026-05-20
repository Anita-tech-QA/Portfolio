# Test Case: Artists Search – User is able to find the correct artist using the search field

## Objective
Verify that the Artists search functionality correctly displays matching artists when the user enters a full or partial valid artist name.


## Preconditions
- Valid Koel user account  
- User is logged into Koel: https://qa.koel.app/#!/home  
- Artists exist in the database (e.g., Lobo Loco, Robert)


## Test Data
- Full artist name: **Lobo Loco**  
- Partial artist name: **Robert**


## Steps
1. Log into Koel  
2. Click on the search field  
3. Enter the full valid artist name: **"Lobo Loco"**  
4. Observe the displayed results  
5. Delete the artist name from the search field  
6. Enter a partial valid artist name: **"Robert"**  
7. Observe the displayed results


## Expected Result
- When entering **"Lobo Loco"**, only the matching artist is displayed.  
- Non‑matching artists are not displayed.  
- When entering **"Robert"**, relevant matching artists are displayed.  
- Non‑matching artists are not displayed.


## Actual Result
- Full artist search **"Lobo Loco"** incorrectly displays additional artists (The Blank Tapes, Defunct by Metre).  
- Partial artist search **"Robert"** returns **no results**, even though matching artists exist.


## Status
❌ **Failed**


## Evidence
- Screenshot: [TC01-1](/Manual-Testing-Project/Evidence/TC01-1.png)
- Screenshot: [TC01-2](/Manual-Testing-Project/Evidence/TC01-2.png)
- Screenshot: [TC01-3](/Manual-Testing-Project/Evidence/TC01-3.png)
- Screenshot: [TC01-4](/Manual-Testing-Project/Evidence/TC01-4.png)
- Related Bug Report: [BR01-ARTISTS-Artists-Search-Returns-Incorrect-Results.md](../Bug-Reports/BR01-ARTISTS-Artists-Search-Returns-Incorrect-Results.md)

# TC05: Koel | Artists | Search returns no results for invalid artist

## Objective
Verify that the Artists search functionality correctly displays **no results** when the user enters an invalid or non‑existent artist name, and confirm through the database that the invalid artist does not exist.

## Preconditions
- Valid Koel user account  
- User is logged into Koel: https://qa.koel.app/#!/home  
- Artists exist in the Koel database (validated via DBeaver using `SELECT * FROM artists ORDER BY name ASC;`)  
- The invalid artist name **"Bongo bongo"** does **not** exist in the database (confirmed via database query)  
- User is on the Artists page or Home page with the search bar visible  

## Test Data
- Invalid artist name: **"Bongo bongo"**

## Steps
1. Log into Koel  
2. Click on the search field  
3. Enter an invalid artist name: **"Bongo bongo"**  
4. Observe the displayed results under:
   - Songs  
   - Artists  
   - Albums  

## Expected Result
- No matching artists should be displayed.  
- No matching songs should be displayed.  
- No matching albums should be displayed.  
- A clear **“None found”** or equivalent empty‑state message should appear in each section.  
- Database confirms that **"Bongo bongo"** does not exist in the `artists` table.  

## Actual Result
- **Songs:** Displays *“None found”* correctly.  
- **Artists:** Incorrectly displays an unrelated artist (**Metre**).  
- **Albums:** Incorrectly displays an unrelated album (**Chevalerie EP by AKMV‑18**).  
- Search results do **not** reflect the invalid query.  
- Database confirms **"Bongo bongo"** does not exist, so UI behavior is incorrect.  

## Status
❌ **Failed**

## Evidence
- Screenshot: [TC05-1](/Manual-Testing-Project/Evidence/TC05-1.png)
- Screenshot: [TC05-2](/Manual-Testing-Project/Evidence/TC05-2.png)
- Related Bug Report: [BR05 - Invaid Artist Search Returns Incorrect Results](../Bug-Reports/BR05-invalid-artist-search-returns-incorrect-results.md)

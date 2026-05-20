# Bug Report: Koel | Artists | Invalid search returns unrelated results

## Summary
When the user enters an invalid artist name in the search field, the UI incorrectly displays unrelated artists and albums instead of showing an empty result set.  
The UI behavior does not match the database records, which confirm that the invalid artist does not exist.

## Environment
- Application: Koel  
- Environment: QA  
- URL: https://qa.koel.app/#!/artists  
- Module: Artists / Search  

## Preconditions
- Valid Koel user account  
- User is logged into the application  
- Access to the Koel database is available  
- Artists exist in the database (validated via `SELECT * FROM artists ORDER BY name ASC;`)  
- The invalid artist name **"Bongo bongo"** does **not** exist in the database  

## Steps to Reproduce
1. Log into DBeaver  
2. Run the SQL query: SELECT * FROM artists ORDER BY name ASC;  
3. Confirm that **"Bongo bongo"** does not exist in the database  
4. Log into Koel  
5. Navigate to https://qa.koel.app/#!/artists  
6. Enter **"Bongo bongo"** into the search field  
7. Observe the results under:
   - Songs  
   - Artists  
   - Albums  

## Expected Result
- No artists, songs, or albums should be displayed.  
- UI should show **“None found”** or an equivalent empty‑state message.  
- UI results should match the database (invalid artist should not return any results).

## Actual Result
- **Songs:** Correctly displays *“None found”*.  
- **Artists:** Incorrectly displays unrelated artist (**Metre**).  
- **Albums:** Incorrectly displays unrelated album (**Chevalerie EP by AKMV‑18**).  
- UI returns **false positives** despite the invalid artist not existing in the database.  

## Evidence
- Screenshot: [TC05-1](/Manual-Testing-Project/Evidence/TC05-1.png)
- Screenshot: [TC05-2](/Manual-Testing-Project/Evidence/TC05-2.png)

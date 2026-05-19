# TC06: Koel | Artists | Search is case insensitive

## Purpose
Verify that the Artists search functionality returns the same results regardless of letter casing, ensuring a user‑friendly and consistent search experience.

## Preconditions
- Valid Koel user account  
- User is logged into the application  
- User is on the Artists page or Home page with the search bar visible  
- At least one known artist exists in the system (e.g., “Chad Crouch”)

## Test Data
- "chad"  
- "CHAD"  
- "Chad"

## Steps
1. Enter **"chad"** into the search field  
2. Observe the artist results  
3. Clear the search field  
4. Enter **"CHAD"**  
5. Observe the artist results  
6. Clear the search field  
7. Enter **"Chad"**  
8. Observe the artist results  
9. Compare all three result sets

## Expected Result
- The same artist appears for all three search variations.  
- Search results do not change based on letter casing.  
- No additional or missing artists appear between searches.

## Actual Result
- Search results are identical across all three inputs.  
- Case‑insensitive search confirmed.

## Status
✅ **Passed**  

## Evidence
- Screenshot: [TC06-1](/Manual-Testing-Project/Evidence/TC06-1.png)
- Screenshot: [TC06-2](/Manual-Testing-Project/Evidence/TC06-2.png)
- Screenshot: [TC06-3](/Manual-Testing-Project/Evidence/TC06-3.png)

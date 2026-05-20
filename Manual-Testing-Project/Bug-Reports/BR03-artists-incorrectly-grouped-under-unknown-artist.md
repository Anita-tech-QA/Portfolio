# Bug Report: Koel | Artists | Artists are incorrectly grouped under “Unknown Artist”

## Summary
Artists are incorrectly displayed as “Unknown Artist” on the Artists page.  
Valid artist metadata exists in the track data, but the UI does not render the correct artist name.

## Environment
Application: Koel  
Environment: QA  
URL: https://qa.koel.app/#!/artists  
Module: Artists

## Preconditions
- Valid Koel user account  
- User is logged into the application  
- Artists exist in the database with valid metadata  

## Steps to Reproduce
1. Navigate to https://qa.koel.app/#!/artists  
2. Observe the displayed artist list  
3. Click on an artist entry  
4. Review the artist details and track metadata  

## Expected Result
Artist name, number of albums, number of songs, and number of plays is visible.  
No missing text or incorrect fallback labels are displayed.

## Actual Result
"Unknown Artist" is displayed despite artist names being present in track data: https://qa.koel.app/#!/artist/1

## Evidence
- Screenshot: [TC03](/Manual-Testing-Project/Evidence/TC03.png)  

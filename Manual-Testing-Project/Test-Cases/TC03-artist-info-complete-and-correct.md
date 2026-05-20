# TC03 - Koel | Artists | Artists are displayed with complete and correct information

## Preconditions
- User is registered and logged into Koel: https://qa.koel.app/#!/home  
- User is on the Artists page of the Koel app: https://qa.koel.app/#!/artists  
- Artists exist in the database

## Test Data
- Artist: Enter Value...  
- Expected metadata values: Enter Value...

## Steps
1. Navigate to https://qa.koel.app/#!/artists  
2. Observe the list of displayed artists  
3. Review the artist name, number of albums, number of songs, and number of plays  
4. Check for missing text or broken images  

## Expected Result
- Artist name, number of albums, number of songs, and number of plays are visible.  
- No missing text or broken images are present.

## Actual Result
- "Unknown Artist" is displayed despite artist names being present in track data: https://qa.koel.app/#!/artist/1.  

## Status
❌ **Failed**

## Evidence
- Screenshot: [TC03](/Manual-Testing-Project/Evidence/TC03.png)
- Related Bug Report: [BR03-ARTISTS-Artists-Incorrectly-Grouped-Under-Unknown-Artist.md](../Bug-Reports/BR03-ARTISTS-Artists-Incorrectly-Grouped-Under-Unknown-Artist.md)

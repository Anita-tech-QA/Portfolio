# Test Case: GET /api/song/{song_id}/info without Bearer token returns 401 Unauthorized

## Objective
Verifies that the API should return **401 Unauthorized** when the user attempts to retrieve song information using a valid song ID but without providing a Bearer token.

## Preconditions
- Valid user account  
- Valid song ID exists in the system  
- Postman environment configured  
- Endpoint `GET /api/song/{song_id}/info` is available  

## Test Data
- song_id: *(valid)*  
- token: *(missing)*  

## Steps
1. Send a GET request to `/api/song/{song_id}/info` using a valid song ID  
2. Do **not** include a Bearer token in the authorization header  
3. Submit the request  
4. Observe the response  

## Expected Result
- Response status: **401 Unauthorized**.  
- Response body indicates that authentication is required.  
- No song information is displayed.  

## Actual Result
The request returned **200 OK** instead of the expected 401 Unauthorized.  
This behavior is incorrect and has been logged as a defect.

## Status
❌ **Failed**

## Evidence
- Screenshot: [TC04](/API-Testing-Project/Evidence/Screenshots/TC04.png) 
- Related Bug Report: [BR04 – GET song info without token returns 200](../Bug-Reports/BR04-Get-Song-Info-No-Token-Returns-200.md)

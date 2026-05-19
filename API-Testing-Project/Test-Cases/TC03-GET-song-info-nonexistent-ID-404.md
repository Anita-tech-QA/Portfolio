# Test Case: GET /api/song/{song_id}/info with non‑existent song ID returns 404 Not Found

## Objective
Verifies that the API returns **404 Not Found** when the user attempts to retrieve song information using a song ID that does not exist in the system.

## Preconditions
- Valid user account  
- Valid Bearer token  
- Postman environment configured  
- Endpoint `GET /api/song/{song_id}/info` is available  

## Test Data
- song_id: *(missing)*  
- token: *(valid)*  

## Steps
1. Send a GET request to `/api/song/{invalid_song_id}/info` using a song ID that does not exist  
2. Include a valid Bearer token in the authorization header  
3. Submit the request  
4. Observe the response  

## Expected Result
- Response status: **404 Not Found**.  
- Response body indicates that the song could not be found.  
- No song information is displayed.  

## Actual Result
- The request returned **404 Not Found**.  
- The response body indicated that the song resource does not exist.  
- No song information was displayed.

## Status
✅ **Passed**

## Evidence
- Screenshot: [TC03](/API-Testing-Project/Evidence/Screenshots/TC03.png)  

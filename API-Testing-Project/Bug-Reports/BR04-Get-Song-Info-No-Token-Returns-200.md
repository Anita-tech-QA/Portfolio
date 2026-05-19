# Bug Report: GET /api/song/{song_id}/info without Bearer token returns 200 OK (Should be 401 Unauthorized)

## Summary
The API incorrectly returns **200 OK** when requesting song information without providing a Bearer token.  
A 401 Unauthorized response is expected for unauthenticated requests.

## Environment
- QA Environment: Koel  
- Endpoint: `GET /api/song/{song_id}/info`  
- Authentication: Bearer token *(missing)*  

## Preconditions
- Valid user account exists  
- Valid song ID exists in the system  
- Postman environment configured  
- Endpoint is available  

## Steps to Reproduce
1. Send a GET request to `/api/song/{song_id}/info` using a valid song ID  
2. Do **not** include a Bearer token in the authorization header  
3. Submit the request  
4. Observe the response  

## Expected Result
- Response status: **401 Unauthorized**.  
- Response body indicates that authentication is required.  
- No song information is displayed.  

## Actual Result
- Response status: **200 OK**.  
- The API returned a successful response even though no Bearer token was provided.  
- This behavior violates expected authentication requirements.  

## Evidence
- Screenshot: [TC04](/API-Testing-Project/Evidence/Screenshots/TC04.png)  

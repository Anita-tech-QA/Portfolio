# Test Case: GET /api/{song}/play/{transcode?}/{bitrate?}?jwt-token={{token}} returns 200 OK

## Objective
Verifies that a valid user with a valid Bearer token can successfully play a song using the Koel API and receive a **200 OK** response with a returned audio stream or response body.

## Preconditions
- Endpoint **GET /api/{song}/play/{transcode?}/{bitrate?}** is available  
- A valid song ID exists in the system  
- Valid Bearer token for a registered user is available  
- Postman environment is configured  

## Test Data
- song_id:   
- token: 

## Steps
1. Send a **GET** request to `/api/{song}/play/{transcode?}/{bitrate?}?jwt-token={{token}}`  
2. Use a **valid song ID**  
3. Include a **valid Bearer token** in the query parameter
4. Submit the request  
5. Observe the response  

## Expected Result
- Response status: **200 OK**.  
- Response body is returned (audio stream).  

## Actual Result
- Response status: **200 OK**.  
- The API successfully returned the response body.  
- The request behaved as expected for a valid song ID and valid token.

## Status
✅ **Passed**

## Evidence
Screenshot: [TC06](/API-Testing-Project/Evidence/Screenshots/TC06.png)

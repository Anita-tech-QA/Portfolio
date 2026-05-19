# Test Case: GET /api/song/{song_id}/info returns 401 Unauthorized for invalid or overly long tokens

## Objective
Verifies that the API correctly rejects all unauthorized requests by returning **401 Unauthorized** when the Bearer token is expired, invalid, or too long.

---

## Preconditions
- Valid user account exists  
- Postman environment configured  
- Existing song ID available  
- Authentication is required for this endpoint  

---

## Test Data
- **song_id:** (valid existing ID)  
- **Unauthorized token variations:**  
  - Expired token  
  - Invalid token (random string)  
  - Excessively long token  

---

## Steps
1. Send the same request using an **expired** Bearer token.  
2. Send the request using an **invalid** token (e.g., `"abc123"`).  
3. Send the request using an **excessively long** token.  
4. Observe the response status code and response body for each request.

---

## Expected Result
For **all** unauthorized token variations:

- **Response status:** `401 Unauthorized`  
- **Response body:** Contains an authentication error message  
- **No song information is returned**

---

## Actual Result
All unauthorized token variations failed:

- **Expired token:** API returned **200 OK** instead of 401  
- **Invalid token:** API returned **200 OK** instead of 401  
- **Overly long token:** API returned **404 Not Found** instead of 401  

The API did not enforce consistent authentication behavior for unauthorized requests.

---

## Status
❌ Failed

---

## Evidence
Screenshots:  
- Screenshot: [TC06 - expired token](/API-Testing-Project/Evidence/Screenshots/TC06.png)
- Screenshot: [TC07- long token](/API-Testing-Project/Evidence/Screenshots/TC07.png)
- Screenshot: [TC08 - invalid token](/API-Testing-Project/Evidence/Screenshots/TC08.png)
- Related Bug Report: [BR10 – Incorrect Status Codes for Unauthorized Tokens](../Bug-Reports/BR10-Get-Song-Info-No-Token-Returns-200.md)

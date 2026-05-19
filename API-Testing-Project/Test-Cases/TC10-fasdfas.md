# Test Case: GET /api/song/{song_id}/info returns 401 Unauthorized for invalid or missing tokens

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
- TC05-1 (Expired token)  
- TC05-2 (Invalid token)  
- TC05-3 (Overly long token)

# Bug Report: GET /api/song/{song_id}/info returns incorrect status codes for unauthorized tokens

## Summary
The `/api/song/{song_id}/info` endpoint returns incorrect and inconsistent status codes when unauthorized Bearer tokens are used.  

Instead of returning **401 Unauthorized** for all invalid authentication attempts, the API responds with **200 OK** or **404 Not Found**, depending on the token variation.

This behavior violates expected authentication rules and may expose unintended information about the system.

---

## Environment
- QA Environment: Koel  
- Endpoint: `GET /api/song/{song_id}/info`  
- Authentication: Bearer token required  

---

## Preconditions
- Valid user account exists  
- Valid song ID exists in the system  
- Postman environment configured  
- Endpoint is available  
- Unauthorized token variations prepared (expired, invalid, overly long)  

---

## Steps to Reproduce
1. Send a GET request to `/api/song/{song_id}/info` using a valid song ID.  
2. Repeat the request using each unauthorized token variation:
   - Expired token  
   - Invalid token 
   - Overly long token  
3. Observe the response status and body for each request.

---

## Expected Result
For **all** unauthorized token variations:

- **Response status:** `401 Unauthorized`  
- **Response body:** Indicates authentication is required  
- **No song information is returned**

---

## Actual Result
- **Expired token:** Returned **200 OK**  
- **Invalid token:** Returned **200 OK**  
- **Overly long token:** Returned **404 Not Found**  

The API does not enforce consistent or correct authentication behavior.

---

## Evidence
- Screenshot: [TC05.1 - expired token](/API-Testing-Project/Evidence/Screenshots/TC05.1.png)
- Screenshot: [TC05.2 - long token](/API-Testing-Project/Evidence/Screenshots/TC05.2.png)
- Screenshot: [TC05.3 - invalid token](/API-Testing-Project/Evidence/Screenshots/TC05.3.png)

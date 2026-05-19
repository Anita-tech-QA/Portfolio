# Koel API Testing — Get Song Information

This project validates the Koel music streaming application's `GET /api/song/{song_id}/info` endpoint, focusing on authentication, input validation, and correct response handling. All testing was performed against the Koel QA environment and managed in Jira (Zephyr). API calls were executed and validated using Postman.

The goal was to ensure that registered users can retrieve song information successfully and that the API correctly enforces authentication rules.

## What this project demonstrates
- API testing using Postman  
- Authentication and security validation (Bearer tokens)  
- Negative testing and error‑handling validation  
- Evidence‑based bug reporting  
- Working within a Jira‑managed QA workflow  
- Organised documentation suitable for a QA portfolio  

## Coverage includes
- Valid request → 200 OK  
- Missing or invalid token → 401 Unauthorized  
- Missing or incorrect song ID → 404 Not Found  
- Incorrect HTTP method handling  
- Token edge cases (expired, overly long, malformed)  

## Repository structure
- **Test-Cases** — structured API test cases with evidence  
- **Bug-Reports** — defects with clear reproduction steps and screenshots  
- **Evidence/Screenshots** — supporting screenshots for tests and bugs  

## Documented defects include
- Missing/invalid tokens returning 200 OK instead of 401  
- Overly long tokens returning 404 Not Found  
- Authentication not enforced correctly 

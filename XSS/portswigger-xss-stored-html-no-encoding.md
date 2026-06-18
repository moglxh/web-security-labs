# PortSwigger Lab - Stored XSS (HTML Context, No Encoding)

## Vulnerability
Stored Cross-Site Scripting (XSS)

## Description
User input was stored by the application and later rendered in the HTML response without encoding. This allowed persistent execution of arbitrary JavaScript whenever the affected page was viewed.

## What I did
- Identified a stored input point (e.g., comment field)
- Injected a script payload
- Observed that the payload was saved by the application
- Confirmed that the script executed whenever the page was loaded

## Key Learning
- Stored XSS is more dangerous than reflected XSS
- Malicious scripts persist and affect multiple users
- Lack of output encoding leads to persistent vulnerabilities

## Impact
An attacker can execute JavaScript in every user's browser who views the affected page, potentially leading to session hijacking, data theft, or phishing.

## Fix
- Encode user input before rendering
- Sanitize stored data
- Use frameworks with automatic output escaping
- Implement Content Security Policy (CSP)

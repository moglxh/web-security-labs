# PortSwigger Lab - Reflected XSS (HTML Context, No Encoding)

## Vulnerability
Reflected Cross-Site Scripting (XSS)

## Description
The application reflected user input directly into the HTML response without any encoding or sanitization, allowing execution of arbitrary JavaScript in the browser.

## What I did
- Identified a reflected input point in the application
- Injected a basic script payload
- Observed that the payload was executed in the browser
- Confirmed full control over the HTML context

## Key Learning
- Lack of input encoding leads to direct XSS vulnerabilities
- Reflected XSS executes immediately when a victim interacts with a crafted request
- Understanding context is critical for crafting payloads

## Impact
An attacker can execute arbitrary JavaScript in a victim’s browser, potentially leading to session hijacking, credential theft, or phishing attacks.

## Fix
- Encode user input before rendering in HTML
- Use secure frameworks that auto-sanitize output
- Implement Content Security Policy (CSP)

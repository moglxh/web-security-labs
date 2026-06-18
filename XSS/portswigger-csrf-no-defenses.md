# PortSwigger Lab - CSRF (No Defenses)

## Vulnerability
Cross-Site Request Forgery (CSRF)

## Description
The application did not implement any CSRF protections. This allowed an attacker to trick an authenticated user into performing unintended actions.

## What I did
- Identified a sensitive action (e.g., email/password change)
- Observed that no CSRF token or protection was in place
- Crafted a malicious request that performs the action
- Delivered the request via a crafted page
- Verified that the action executed when the victim accessed the page

## Key Learning
- CSRF exploits trust between browser and server
- No user interaction is required beyond visiting a malicious page
- Lack of CSRF tokens leads to critical vulnerabilities

## Impact
An attacker can perform unauthorized actions on behalf of authenticated users, leading to account compromise or data manipulation.

## Fix
- Implement CSRF tokens
- Use SameSite cookies
- Validate request origin (Referer/Origin headers)

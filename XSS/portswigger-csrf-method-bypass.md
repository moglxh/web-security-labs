# PortSwigger Lab - CSRF (Token Validation Depends on Request Method)

## Vulnerability
CSRF with flawed token validation

## Description
The application implemented CSRF protection, but only enforced token validation for specific request methods (e.g., POST). By switching the request method, the protection could be bypassed.

## What I did
- Identified a state-changing request
- Observed that CSRF token validation only applied to POST requests
- Modified the request to use a different method (e.g., GET)
- Replayed the request without a valid CSRF token
- Successfully performed the action without protection

## Key Learning
- Security mechanisms must be applied consistently across all request methods
- Partial protection can be bypassed by altering request behavior
- Attackers look for logic flaws, not just missing protections

## Impact
An attacker can bypass CSRF protections and perform unauthorized actions on behalf of users.

## Fix
- Enforce CSRF validation on all state-changing requests
- Do not rely on HTTP method restrictions alone
- Implement robust, consistent validation logic

# PortSwigger Lab - CSRF (Token Validation Depends on Token Presence)

## Vulnerability
CSRF with flawed token validation logic

## Description
The application checked the CSRF token only when it was present in the request. If the token was omitted entirely, the request was processed without validation.

## What I did
- Identified a state-changing request protected by a CSRF token
- Tested behavior by removing the token from the request
- Observed that the server did not enforce validation without the token
- Crafted a request without the token
- Successfully performed the action as the victim

## Key Learning
- Security checks must enforce validation, not depend on optional presence
- Conditional validation logic leads to bypass opportunities
- Attackers can manipulate request structure to evade protections

## Impact
An attacker can bypass CSRF protection entirely by omitting the token, allowing unauthorized actions on behalf of authenticated users.

## Fix
- Require CSRF tokens for all state-changing requests
- Reject requests missing required tokens
- Implement strict validation logic

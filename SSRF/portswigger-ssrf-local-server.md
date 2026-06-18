# PortSwigger Lab - Basic SSRF Against Local Server

## Vulnerability
Server-Side Request Forgery (SSRF)

## Description
The application fetched external resources based on user-controlled input without proper validation. This allowed requests to be made from the server to internal resources.

## What I did
- Identified functionality that performed server-side requests
- Modified the request target using controlled input
- Redirected the server request to localhost/internal services
- Accessed internal functionality not intended for external users
- Successfully exploited SSRF to interact with the local server

## Key Learning
- SSRF allows attackers to make requests from the server itself
- Internal services may trust localhost traffic
- Improper URL validation can expose internal infrastructure

## Impact
An attacker can access internal services, sensitive endpoints, or cloud metadata services through the vulnerable server.

## Fix
- Restrict outbound server requests
- Validate and whitelist allowed destinations
- Block access to internal IP ranges and localhost

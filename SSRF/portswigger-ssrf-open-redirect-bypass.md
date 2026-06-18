# PortSwigger Lab - SSRF via Open Redirection Bypass

## Vulnerability
Server-Side Request Forgery (SSRF) with filter bypass using open redirection

## Description
The application attempted to restrict SSRF by validating request destinations. However, an open redirection vulnerability was used to bypass these restrictions and redirect server-side requests to internal resources.

## What I did
- Identified server-side request functionality
- Discovered an open redirect endpoint within the application
- Crafted a request pointing to the trusted redirect endpoint
- Used the redirect to force the server into requesting internal resources
- Successfully bypassed SSRF protections

## Key Learning
- Vulnerabilities can often be chained together
- Open redirects can be leveraged to bypass SSRF filtering
- Trusting internal endpoints without strict validation is dangerous

## Impact
An attacker can bypass SSRF protections and gain access to restricted internal systems through trusted redirection mechanisms.

## Fix
- Validate final redirect destinations
- Restrict server-side requests to strict allowlists
- Prevent open redirect vulnerabilities

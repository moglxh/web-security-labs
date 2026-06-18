# PortSwigger Lab - SSRF with Blacklist-Based Input Filter

## Vulnerability
Server-Side Request Forgery (SSRF) with weak blacklist filtering

## Description
The application attempted to prevent SSRF by blocking specific input patterns and destinations using a blacklist approach. However, the filtering was insufficient and could be bypassed.

## What I did
- Identified server-side request functionality
- Analyzed the blacklist filtering behavior
- Crafted payloads to bypass blocked keywords/IP restrictions
- Reached restricted internal resources despite filtering
- Successfully exploited SSRF against protected targets

## Key Learning
- Blacklist filtering is unreliable for SSRF prevention
- Attackers can use alternative representations and bypass techniques
- Input validation must be strict and whitelist-based

## Impact
An attacker can bypass weak filtering and access internal services or sensitive resources through the vulnerable server.

## Fix
- Use strict allowlists instead of blacklists
- Restrict outbound requests to approved destinations only
- Block private/internal IP ranges and localhost access

# PortSwigger Lab - Basic SSRF Against Another Back-End System

## Vulnerability
Server-Side Request Forgery (SSRF)

## Description
The application made server-side requests based on user-controlled input without proper validation. This allowed access to internal back-end systems that were not externally accessible.

## What I did
- Identified a feature performing server-side requests
- Manipulated the target URL/IP address
- Probed internal network resources through the vulnerable server
- Discovered and accessed an internal back-end system
- Successfully interacted with restricted internal functionality

## Key Learning
- SSRF can be used to pivot into internal networks
- Back-end systems often trust internal traffic
- Improper request validation exposes internal infrastructure

## Impact
An attacker can access internal services, administrative interfaces, or sensitive systems hidden behind the firewall.

## Fix
- Restrict outbound requests from the server
- Validate and whitelist allowed destinations
- Block access to private/internal IP ranges

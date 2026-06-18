# PortSwigger Lab - SSRF with Whitelist-Based Input Filter

## Vulnerability
Server-Side Request Forgery (SSRF) with whitelist filter bypass

## Description
The application attempted to restrict SSRF by allowing requests only to whitelisted domains. However, improper URL validation allowed the whitelist protection to be bypassed.

## What I did
- Identified server-side request functionality
- Analyzed how the whitelist validation was implemented
- Crafted a payload that abused URL parsing behavior
- Bypassed the whitelist restriction
- Successfully accessed restricted internal resources

## Key Learning
- URL parsing inconsistencies can lead to SSRF bypasses
- Whitelist protections must validate destinations securely
- Attackers exploit trust assumptions in validation logic

## Impact
An attacker can bypass SSRF protections and interact with internal systems despite allowlist restrictions.

## Fix
- Perform strict canonicalization and validation of URLs
- Resolve and verify final destinations server-side
- Restrict outbound requests to approved resources only

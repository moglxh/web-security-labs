# PortSwigger Lab - Reflected XSS (Filter Bypass)

## Vulnerability
Reflected Cross-Site Scripting (XSS) with input filtering

## Description
The application attempted to block XSS by restricting most HTML tags and attributes. However, the filtering was insufficient, allowing crafted payloads to bypass restrictions and execute JavaScript.

## What I did
- Identified a reflected input point
- Tested which tags and attributes were allowed
- Crafted a payload using permitted elements
- Bypassed input filtering
- Successfully executed JavaScript in the browser

## Key Learning
- Blacklist-based filtering is ineffective for preventing XSS
- Attackers can adapt payloads to bypass restrictions
- Understanding allowed input is key to crafting exploits

## Impact
An attacker can bypass weak filtering mechanisms and execute malicious scripts, leading to client-side attacks such as session hijacking or phishing.

## Fix
- Use proper output encoding based on context
- Avoid relying on blacklist filtering
- Implement Content Security Policy (CSP)

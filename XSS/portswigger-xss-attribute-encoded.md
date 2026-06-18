# PortSwigger Lab - Reflected XSS (Attribute Context with Encoding)

## Vulnerability
Reflected Cross-Site Scripting (XSS) in attribute context

## Description
User input was reflected inside an HTML attribute, and angle brackets were encoded. However, the application did not properly handle attribute context, allowing injection by breaking out of the attribute.

## What I did
- Identified input reflected within an HTML attribute
- Observed that angle brackets were encoded
- Crafted a payload to break out of the attribute using quotes
- Injected an event handler to execute JavaScript
- Successfully triggered script execution

## Key Learning
- Output encoding must match the context (HTML vs attribute)
- Encoding `< >` alone is not enough
- Attribute injection can be exploited using quotes and event handlers

## Impact
An attacker can execute arbitrary JavaScript by injecting payloads into improperly handled HTML attributes.

## Fix
- Properly encode output based on context
- Escape quotes inside attributes
- Use secure templating frameworks
- Implement Content Security Policy (CSP)

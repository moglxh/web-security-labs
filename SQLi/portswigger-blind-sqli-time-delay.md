# PortSwigger Lab - Blind SQL Injection (Time-Based)

## Vulnerability
Blind SQL Injection using time delays

## Description
The application did not return visible data or errors. Instead, time delays were used as a side-channel to infer whether a condition was true or false.

## What I did
- Identified an injection point
- Crafted payloads that introduce delays when conditions are TRUE
- Measured response time differences
- Used timing behavior to infer database information
- Extracted data step-by-step using delays

## Key Learning
- Time-based SQLi works even when no output or errors are visible
- Response timing can act as a covert communication channel
- Patience and precision are critical in blind SQLi

## Impact
An attacker can extract sensitive database information even in highly restricted environments with no direct feedback.

## Fix
- Use parameterized queries (prepared statements)
- Implement strict input validation
- Avoid executing user-controlled queries

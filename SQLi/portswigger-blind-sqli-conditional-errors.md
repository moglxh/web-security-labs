# PortSwigger Lab - Blind SQL Injection (Conditional Errors)

## Vulnerability
Blind SQL Injection using conditional error-based responses

## Description
The application did not return query results directly but produced errors when specific conditions were met. These errors were used as indicators to infer database information.

## What I did
- Identified an injection point
- Crafted conditional payloads that trigger errors when TRUE
- Observed error vs normal responses
- Used this behavior to extract data step-by-step
- Inferred sensitive information from the database

## Key Learning
- Errors can act as side-channel indicators in blind SQL injection
- Applications leaking error behavior are vulnerable even without data output
- Logical testing is key to extracting hidden data

## Impact
An attacker can extract sensitive data by triggering and observing database errors, leading to potential data breaches.

## Fix
- Use parameterized queries (prepared statements)
- Handle errors securely (avoid exposing database behavior)
- Validate and sanitize all user input

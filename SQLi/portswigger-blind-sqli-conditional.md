# PortSwigger Lab - Blind SQL Injection (Conditional Responses)

## Vulnerability
Blind SQL Injection using conditional responses

## Description
The application was vulnerable to SQL injection but did not return query results directly. Instead, it responded differently based on whether a condition was true or false, allowing inference of data.

## What I did
- Identified an injection point in a request
- Sent conditional payloads (TRUE/FALSE)
- Observed differences in application responses
- Used this behavior to infer database information step-by-step
- Extracted sensitive data indirectly

## Key Learning
- Not all SQL injection vulnerabilities expose data directly
- Conditional logic can be used to infer hidden information
- Careful observation is critical in blind SQLi

## Impact
An attacker can extract sensitive data from the database even when no direct output is shown.

## Fix
- Use parameterized queries (prepared statements)
- Implement proper input validation
- Avoid exposing behavioral differences in responses

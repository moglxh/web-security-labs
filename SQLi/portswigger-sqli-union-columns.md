# PortSwigger Lab - SQL Injection (UNION Attack - Column Enumeration)

## Vulnerability
SQL Injection using UNION-based attack

## Description
The application was vulnerable to SQL injection, allowing the use of UNION queries to combine results and extract additional data. The first step was determining the number of columns returned by the original query.

## What I did
- Identified an injection point in the application
- Used ORDER BY / UNION SELECT techniques to determine the number of columns
- Confirmed the correct number of columns for successful UNION injection
- Prepared the query for further data extraction

## Key Learning
- UNION attacks require matching the number of columns in the original query
- Column enumeration is a critical step in SQL injection
- Structured testing helps build successful payloads

## Impact
An attacker can prepare and execute UNION-based queries to extract sensitive data from the database.

## Fix
- Use parameterized queries (prepared statements)
- Implement strict input validation
- Avoid exposing database errors

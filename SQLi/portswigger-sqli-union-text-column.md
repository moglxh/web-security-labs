# PortSwigger Lab - SQL Injection (UNION Attack - Finding Text Column)

## Vulnerability
SQL Injection using UNION-based attack

## Description
The application was vulnerable to SQL injection, allowing UNION queries to be used. After determining the number of columns, the next step was identifying which column could display text data.

## What I did
- Used UNION SELECT with different data types
- Tested each column position with text values
- Identified which column accepted and displayed text data
- Confirmed a valid column for further data extraction

## Key Learning
- Not all columns accept the same data types
- Identifying a text-compatible column is essential for extracting readable data
- SQL injection requires structured and step-by-step testing

## Impact
An attacker can use the identified column to extract and display sensitive data from the database.

## Fix
- Use parameterized queries (prepared statements)
- Validate and sanitize user input
- Prevent detailed database error exposure

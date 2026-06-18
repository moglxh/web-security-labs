# PortSwigger Lab - SQL Injection (UNION Attack - Data Extraction)

## Vulnerability
SQL Injection using UNION-based attack

## Description
The application was vulnerable to SQL injection, allowing UNION queries to retrieve data from other database tables once the query structure and column types were understood.

## What I did
- Identified an SQL injection point
- Determined the number of columns in the query
- Found a column that supports text data
- Used UNION SELECT to query other tables
- Retrieved sensitive data (e.g., usernames and passwords)

## Key Learning
- SQL injection can expose entire database contents
- Structured approach (columns → types → extraction) is essential
- Sensitive data in databases must be properly protected

## Impact
An attacker can extract sensitive information such as user credentials, leading to account compromise and data breaches.

## Fix
- Use parameterized queries (prepared statements)
- Apply strict input validation
- Implement least privilege for database access

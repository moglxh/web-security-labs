# PortSwigger Lab - SQL Injection (WHERE Clause - Hidden Data Retrieval)

## Vulnerability
SQL Injection in WHERE clause

## Description
The application was vulnerable to SQL injection, allowing manipulation of the database query to retrieve hidden data that should not be accessible.

## What I did
- Identified input that was directly used in a SQL query
- Injected SQL payload to modify the WHERE clause logic
- Bypassed filtering conditions to retrieve additional data
- Successfully accessed hidden information from the database

## Key Learning
- Improper input validation can lead to SQL injection
- SQL logic can be manipulated to bypass application restrictions
- Even simple injection points can expose sensitive data

## Impact
An attacker can retrieve unauthorized data from the database, potentially exposing sensitive information.

## Fix
- Use parameterized queries (prepared statements)
- Implement proper input validation and sanitization
- Avoid directly embedding user input in SQL queries

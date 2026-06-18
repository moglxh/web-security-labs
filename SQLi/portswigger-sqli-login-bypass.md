# PortSwigger Lab - SQL Injection (Login Bypass)

## Vulnerability
SQL Injection in authentication (login bypass)

## Description
The login functionality was vulnerable to SQL injection, allowing manipulation of the authentication query to bypass login without valid credentials.

## What I did
- Identified that user input was directly used in a SQL query
- Injected a payload to modify the query logic
- Bypassed authentication checks without knowing the password
- Gained access to the application

## Key Learning
- Authentication systems are a critical target for SQL injection
- Improper input handling can completely break login mechanisms
- SQL logic can be manipulated to bypass security controls

## Impact
An attacker can bypass authentication and gain unauthorized access to user accounts or administrative functionality.

## Fix
- Use parameterized queries (prepared statements)
- Avoid direct insertion of user input into SQL queries
- Implement proper input validation and sanitization

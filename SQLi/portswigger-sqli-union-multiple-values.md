# PortSwigger Lab - SQL Injection (UNION Attack - Multiple Values in Single Column)

## Vulnerability
SQL Injection using UNION-based attack

## Description
The application was vulnerable to SQL injection, but only one column could display data. This required combining multiple values into a single column to extract useful information.

## What I did
- Identified the SQL injection point
- Determined the number of columns
- Found the column that supports text output
- Used SQL concatenation to combine multiple values into one column
- Retrieved multiple pieces of data (e.g., username and password) in a single output

## Key Learning
- Output limitations can be bypassed using SQL concatenation
- Understanding database functions is important for effective exploitation
- Creative query manipulation is key in real-world scenarios

## Impact
An attacker can extract multiple sensitive data fields even when the application limits output to a single column.

## Fix
- Use parameterized queries (prepared statements)
- Restrict database query behavior
- Validate and sanitize all user inputs

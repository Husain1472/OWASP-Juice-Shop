# OWASP-Juice-Shop
OWASP Juice Shop Penetration Testing Project

## Overview
A security assessment of OWASP Juice Shop, demonstrating vulnerabilities like SQLi, XSS, and IDOR. Conducted as part of my internship to showcase ethical hacking skills.

## Key Findings
- **SQL Injection**: Bypassed login via `' OR 1=1 --`.
- **XSS**: Executed arbitrary JavaScript in the search bar.
- **IDOR**: Accessed unauthorized user data via `/rest/user/{id}`.

## Tools Used
- Burp Suite
- SQLMap
- Docker (Juice Shop)

## How to Reproduce
1. Run Juice Shop:
   ```bash
   docker run -d -p 3000:3000 bkimminich/juice-shop

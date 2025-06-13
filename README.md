# OWASP Juice Shop Penetration Testing Report

![OWASP Juice Shop Logo](https://raw.githubusercontent.com/juice-shop/juice-shop/master/frontend/src/assets/public/images/JuiceShop_Logo.png)

## 📜 Overview
A comprehensive security assessment of **OWASP Juice Shop**, a deliberately vulnerable web application. This project demonstrates real-world penetration testing techniques while adhering to ethical hacking principles.

## 🎯 Project Objectives
- Identify and exploit common web vulnerabilities
- Document findings for technical and non-technical stakeholders
- Develop remediation strategies for discovered vulnerabilities

## 🔍 Key Findings
| Vulnerability               | Risk Level | Impact                          | Proof |
|-----------------------------|------------|---------------------------------|-------|
| SQL Injection (Login Bypass)| Critical   | Full admin access               | [Screenshot](report/screenshots/sqli_login.png) |
| Persistent XSS (Search Bar) | High       | Stored malicious script execution | [Video](report/proofs/xss_demo.mp4) |
| IDOR (User API)             | Medium     | Unauthorized data access        | [JSON Response](report/data/user_2.json) |

## 🛠️ Tools Used
- **Burp Suite Community** (Proxy/Repeater/Intruder)
- **SQLMap** (Automated SQLi exploitation)
- **Docker** (Juice Shop deployment)

## 🚀 Getting Started
### Prerequisites
- Docker ([Install Guide](https://docs.docker.com/get-docker/))
- Kali Linux/Ubuntu
- Burp Suite ([Download](https://portswigger.net/burp/communitydownload))

### Installation
1. Deploy Juice Shop:
   ```bash
   docker run -d -p 3000:3000 bkimminich/juice-shop

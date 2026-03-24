# Web Application Security Assessment Lab

## 📌 Project Overview
This repository contains a collection of vulnerability reports and proof-of-concept (PoC) exploits conducted within a custom-built, isolated local laboratory environment. The purpose of this project is to demonstrate practical hands-on experience with modern web application vulnerabilities, penetration testing methodologies, and professional security documentation.

## 🏗️ Lab Architecture
To safely execute these assessments, I designed and configured an isolated, dual-adapter virtualized network:
* **Hypervisor:** VMware
* **Attacker Machine:** Kali Linux (Configured with NAT for tool retrieval and Host-Only for target isolation)
* **Target Infrastructure:** Docker Engine running intentionally vulnerable modern web applications.

## 🛠️ Tools & Technologies Used
* **Containerization:** Docker & Docker Compose
* **Exploitation Targets:** OWASP Juice Shop (Node.js/Angular)
* **Techniques:** Manual payload injection, input validation bypass, browser-side exploitation.
* **Version Control:** Git & GitHub

## 📂 Vulnerabilities Researched & Exploited
This repository documents the successful exploitation and remediation strategies for the following vulnerabilities:

1. **[Authentication Bypass via SQL Injection (SQLi)](./OWASP-Juice-Shop/SQL-Injection-Login-Bypass/vulnerability-report.md)**
   * **Description:** Exploited unsanitized input in the login mechanism to bypass password authentication and gain administrative access.
   * **Impact:** Full account takeover and unauthorized access to backend records.

2. **[DOM-Based Cross-Site Scripting (XSS)](./OWASP-Juice-Shop/DOM-Cross-Site-Scripting/vulnerability-report.md)**
   * **Description:** Leveraged unescaped user input in the application's search functionality to execute arbitrary JavaScript within the client's browser.
   * **Impact:** Potential for session hijacking, phishing, and malicious redirection.

## ⚠️ Disclaimer
All security assessments and exploits documented in this repository were conducted strictly within a legally owned, locally hosted, and completely isolated virtual environment. This project is strictly for educational purposes and to demonstrate professional cybersecurity competencies.

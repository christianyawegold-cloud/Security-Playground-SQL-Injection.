# Security-Playground-SQL-Injection.
Demonstrating a SQL injection login bypass vulnerability in a custom Python web server.
# Security Playground: SQL Injection (Login Bypass)

## 🎯 Project Overview
This project is a custom-built lab environment demonstrating a SQL Injection (SQLi) vulnerability. The objective was to build a vulnerable Python-based web server and successfully bypass the authentication mechanism using malicious SQL payloads.

## 🏗️ Lab Architecture
* **Target Machine:** Ubuntu Server running a custom Python web application and SQLite database.
* **Attacker Machine:** Kali Linux.
* **Vulnerability:** Unsanitized user input in the SQL query handling the login authentication.

## ⚔️ The Attack Vector
By injecting a specific SQL payload (`' OR '1'='1`) into the username/password fields via a `curl` request, the backend database logic is manipulated into evaluating the statement as `TRUE`. This allows an attacker to bypass the password check and gain unauthorized access to the application.

## 📸 Proof of Concept (PoC)
1. **The Vulnerable Code:** *<img width="572" height="17" alt="Screenshot 2026-10-04 185554" src="https://github.com/user-attachments/assets/06665e43-1e6c-4294-93f3-c4cf8d4332bc" />

2. **The Attack Execution:** <img width="700" height="18" alt="image" src="https://github.com/user-attachments/assets/5fca9977-f166-4d8a-b41e-e99351f7d7fc" />


3. **Successful Bypass:** *<img width="765" height="66" alt="image" src="https://github.com/user-attachments/assets/4fddc3b3-368c-49d7-8b9e-81e6c3497e7f" />

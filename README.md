**Name:** HARNIL MODI

**Company:** CODTECH IT SOLUTIONS

**ID:** CT08DAN

**Domain:** Cyber Security & Ethical Hacking

**Duration:** December to January 2025

**Mentor:** Neela Santhosh Kumar



## **Overview of the Project :-** 

### Project :- WEB APPLICATION PENETRATION TESTING

In this task, I was required to perform penetration testing on a web application to identify and exploit vulnerabilities such as SQL injection, cross-site scripting (XSS), and insecure authentication mechanisms. Since no specific test environment was provided, I utilized the publicly available and intentionally vulnerable website http://testphp.vulnweb.com/ for this purpose.

### Document Findings

**1. SQL Injection (SQLi)**

Vulnerability:

During testing, I used SQLmap to identify and exploit SQL injection vulnerabilities in the web application. The tool was used to extract database information, including tables and columns, and I successfully dumped the data available in the columns.

**Steps Taken:**

-I identified injectable parameters in the application.

-Used SQLmap to automate the exploitation of the vulnerability, allowing access to the database structure (tables and columns).

-Dumped the available data from the database, which could include sensitive information like usernames, passwords, etc.

**Impact:**

SQL injection allows attackers to manipulate the database and gain access to sensitive information, which could be used for further attacks, including privilege escalation, data theft, and system compromise.

**Remediation:**

To fix this issue, the application should implement parameterized queries or prepared statements to prevent SQL injection. Additionally, input validation and output encoding should be implemented to ensure that user inputs are properly sanitized.
![image alt](https://github.com/user-attachments/assets/377a243d-7f65-48ed-9553-67e50a2339da)

## 2. Cross-Site Scripting (XSS)

**Vulnerability:**

I identified a Cross-Site Scripting (XSS) vulnerability in the web application by injecting a basic alert script into the search bar.

**Steps Taken:**

-I entered a simple XSS payload (<script>alert(9)</script>) in the search bar.

-The payload was executed within the client browser, demonstrating the vulnerability.

**Impact:**

XSS vulnerabilities allow attackers to inject malicious scripts that run in the context of a user’s browser, potentially leading to session hijacking, defacement, and data theft. This type of vulnerability can impact both users and administrators of the application.

**Remediation:**

To mitigate XSS vulnerabilities, the application should sanitize all user inputs by escaping special characters such as <, >, and &. Implementing a Content Security Policy (CSP) and using HTTP-only cookies will further reduce the risk.
![image alt](https://github.com/user-attachments/assets/ee79742f-7f11-429b-ad72-0287d78ed539)

## 3. Brute Force Vulnerability in Authentication Mechanism

**Vulnerability:**

I identified a brute force vulnerability in the authentication mechanism. The login form did not implement protections such as two-factor authentication (2FA) or password complexity requirements, making it susceptible to brute-force attacks.

**Steps Taken:**

I tested the login functionality using a Cluster Bomb attack technique, combined with a basic username/password list sourced from PortSwigger.

During testing, I observed that the application lacked protections such as account lockout or CAPTCHA after multiple failed login attempts, making it easy for an attacker to repeatedly guess password combinations.

Based on this, I determined that weak password policies and the absence of 2FA made the system highly vulnerable to brute force attacks, allowing the attacker to eventually gain unauthorized access.

**Impact:**

Brute force attacks can lead to unauthorized access to user accounts, potentially allowing attackers to steal sensitive data, escalate privileges, or take control of user sessions. This could result in data breaches, account takeover, or other forms of unauthorized actions.

**Remediation:**

To mitigate this vulnerability, the application should implement:

-Two-factor authentication (2FA) to provide an additional layer of security beyond just passwords.

-Password complexity requirements to enforce the use of strong and unpredictable passwords.

-Account lockout mechanisms or CAPTCHA after multiple failed login attempts to prevent automated brute-force attacks.

-This update reflects the specific tools and methods you used for brute force testing. Let me know if you'd like further adjustments!
![image alt](https://github.com/user-attachments/assets/ea699671-9247-403f-ac43-0cfdb6401697)


### Technologies and Tools Used:

1. SQLmap:

-A tool used to automate the detection and exploitation of SQL injection vulnerabilities. It helped in extracting database information such as tables, columns, and data from vulnerable endpoints.

2. Cross-Site Scripting (XSS):

-A vulnerability that allows an attacker to inject malicious scripts into web pages. A basic JavaScript alert script was used to test for XSS in the search bar of the web application.

3. Cluster Bomb (Brute Force Attack):

-A brute-force attack technique that tests combinations of usernames and passwords. Used with a PortSwigger password list to attempt login with common credentials and identify brute-force vulnerabilities.

4. PortSwigger:

-Provided a basic username and password list used in conjunction with Cluster Bomb for brute-force testing on the login page.

5. Test Environment (http://testphp.vulnweb.com/):

-An intentionally vulnerable web application used for testing security vulnerabilities in a controlled environment.
![image alt](https://github.com/user-attachments/assets/dc8907df-928b-4c7f-841a-00a2312bdf07)


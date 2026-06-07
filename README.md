# 🛡️ Vulnerability Assessment Report — Future Interns Cyber Security Task 1 (2026)

![Risk Badge](https://img.shields.io/badge/Critical-1-red) ![Risk Badge](https://img.shields.io/badge/High-5-orange) ![Risk Badge](https://img.shields.io/badge/Medium-2-yellow) ![License](https://img.shields.io/badge/Scope-Passive%20%2F%20Read--Only-blue)

---

## 📋 Overview

This repository contains the deliverables for **Cyber Security Internship Task 1 (2026)** from [Future Interns](https://futureinterns.com).

The task required performing a **passive vulnerability assessment** on a public website, documenting security weaknesses, classifying them by risk level, and presenting findings in a professional audit report.

---

## 🌐 Website Tested

| Field | Details |
|-------|---------|
| **Target** | http://testphp.vulnweb.com |
| **Owner** | Acunetix (intentionally vulnerable for training) |
| **Purpose** | Legal practice environment for security assessment |
| **Technology** | PHP, MySQL, Apache |

> ⚠️ **testphp.vulnweb.com** is a deliberately vulnerable web application created and maintained by Acunetix specifically for ethical security training. It is 100% legal and encouraged to scan.

---

## 🔍 Scope

| Item | Details |
|------|---------|
| **Assessment Type** | Passive / Read-Only Vulnerability Assessment |
| **Allowed** | Public-facing pages, header analysis, passive scanning, manual review |
| **Not Performed** | Exploitation, brute force, login bypass, DoS attacks |
| **Compliance** | OWASP Testing Guidelines (Passive), ethical hacking standards |

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **OWASP ZAP** (Passive Mode) | Automated passive vulnerability scanning |
| **Browser DevTools** (F12) | HTTP header inspection, cookie analysis |
| **Nmap** | Port enumeration and service detection |
| **securityheaders.com** | Rapid HTTP security header validation |
| **Manual Review** | URL parameter analysis, information disclosure checks |

---

## 📊 Findings Summary

| ID | Vulnerability | Risk | CVSS |
|----|--------------|------|------|
| VUL-001 | Missing HTTP Security Headers | 🟠 HIGH | 7.5 |
| VUL-002 | SQL Injection (SQLi) | 🔴 CRITICAL | 9.8 |
| VUL-003 | Reflected Cross-Site Scripting (XSS) | 🟠 HIGH | 7.4 |
| VUL-004 | Stored Cross-Site Scripting (XSS) | 🟠 HIGH | 8.2 |
| VUL-005 | Unencrypted HTTP Transmission | 🟠 HIGH | 7.5 |
| VUL-006 | Directory Listing Enabled | 🟡 MEDIUM | 5.3 |
| VUL-007 | Insecure Session Management | 🟠 HIGH | 7.3 |
| VUL-008 | Sensitive Information Disclosure | 🟡 MEDIUM | 5.3 |

**Total: 1 Critical · 5 High · 2 Medium**

---

## 📁 Repository Contents

```
📂 vulnerability-assessment-task1/
├── 📄 README.md                                        ← This file
├── 📋 Vulnerability_Assessment_Report_FutureInterns.pdf ← Full report
└── 📂 evidence/
    ├── missing_security_headers.png
    ├── sql_injection_error.png
    ├── xss_reflected.png
    ├── directory_listing.png
    └── insecure_cookies.png
```

---

## ✅ Top Remediation Priorities

1. **[CRITICAL]** Fix SQL Injection — use prepared statements for all DB queries
2. **[HIGH]** Enable HTTPS/TLS — install certificate, redirect HTTP → HTTPS, enable HSTS
3. **[HIGH]** Add Security Headers — CSP, X-Frame-Options, X-Content-Type-Options
4. **[HIGH]** Fix XSS — sanitise input server-side, encode all output
5. **[HIGH]** Secure Session Cookies — set Secure + HttpOnly flags, invalidate on logout
6. **[MEDIUM]** Disable Directory Listing — `Options -Indexes` in Apache config
7. **[MEDIUM]** Suppress Error Details — custom error pages, `expose_php=Off`

---

## 📚 References

- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [OWASP Top 10 (2021)](https://owasp.org/www-project-top-ten/)
- [CVSS v3.1 Scoring System](https://www.first.org/cvss/)
- [Mozilla Security Headers Guide](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

---

## 👤 Author

**Security Intern** — Future Interns Cyber Security Program  
📅 Assessment Date: June 07, 2026  
🏢 Organization: [Future Interns](https://futureinterns.com)  
🔗 LinkedIn: [Future Interns](https://www.linkedin.com/company/future-interns)

---

> *This assessment was conducted ethically using passive techniques only. No systems were harmed or exploited. All findings are documented for educational purposes as part of the Future Interns internship program.*

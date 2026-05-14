# 🔐 API Security Risk Analysis

![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)
![Internship](https://img.shields.io/badge/Internship-Future%20Interns-blue?style=flat)
![Task](https://img.shields.io/badge/Task-03-orange?style=flat)
![Tools](https://img.shields.io/badge/Tools-Postman%20%7C%20DevTools-purple?style=flat)
![Methodology](https://img.shields.io/badge/Methodology-OWASP-red?style=flat)

> **Cybersecurity Internship — Task 03 | Future Interns | April 2026**  
> A comprehensive security assessment of a public REST API, covering authentication flaws, data exposure, and transport security weaknesses.

---

## 📌 Executive Summary

This project presents a full security assessment of a public REST API (**JSONPlaceholder**), conducted as part of the Future Interns cybersecurity program. The goal was to identify systemic vulnerabilities, evaluate business risks, and deliver actionable remediation strategies — following industry-standard methodologies.

---

## 🎯 Project Objectives

- **Vulnerability Assessment** — Identify flaws in authentication mechanisms and access control
- **Data Privacy Audit** — Detect unauthorized exposure of Personally Identifiable Information (PII)
- **Risk Communication** — Translate technical findings into business-centric risk impact statements
- **Strategic Remediation** — Develop clear, prioritized steps for vulnerability mitigation

---

## 🛠️ Methodology & Tooling

The assessment followed a **non-intrusive, read-only approach**.

| Tool | Usage |
|---|---|
| **Postman** | Automated request crafting and response payload analysis |
| **Browser DevTools** | Deep-packet inspection of HTTP headers and network latency |

### Audit Workflow

```
1. Reconnaissance    →  API documentation analysis + endpoint mapping
2. Traffic Analysis  →  Manual HTTP header and status code inspection
3. Security Profiling → Risk classification (Low → Critical)
4. Reporting         →  Documented findings with evidence and remediation
```

---

## 🚨 Vulnerability Assessment Matrix

| ID | Vulnerability | Severity | OWASP Category | Status |
|---|---|---|---|---|
| 01 | Missing Authentication | 🔴 HIGH | API2:2023 Broken Auth | Documented |
| 02 | Excessive Data Exposure (PII Leakage) | 🔴 CRITICAL | API3:2023 Broken Object Property Level Auth | Documented |
| 03 | Missing Security Headers | 🟡 MEDIUM | API7:2023 Server Side Request Forgery | Documented |

### Key Findings

**01 — Broken Access Control**
> The `/users` endpoint returns sensitive data including GPS coordinates and private contact details with a `200 OK` status — without requiring any API key or JWT token.

**02 — Information Leakage (PII)**
> The `/comments` and `/posts` endpoints expose internal metadata and user email addresses to unauthenticated requests, creating a direct GDPR compliance risk.

**03 — Weak Transport Security**
> Missing modern security headers (`X-Content-Type-Options`, `Strict-Transport-Security`, `Content-Security-Policy`) increase the attack surface for Man-in-the-Middle (MitM) and injection attacks.

---

## 📸 Evidence & Screenshots

### Authentication Test — Unauthenticated `/users` endpoint
![Screenshot 1](screenshot%201.png)

### PII Leakage — Exposed email addresses in `/comments`
![Screenshot 2](screenshot%202.png)

### Missing Security Headers — DevTools inspection
![Screenshot 3](screenshot%203.png)

### Endpoint Mapping — Postman Collection
![Screenshot 4](screenshot%204.png)

### Risk Summary — Full findings overview
![Screenshot 5](screenshot%205.png)

---

## 📄 Full Report

📥 [Download the full technical report (PDF)](Task3_API_Security_Report_v2.pdf)

The report includes:
- Detailed risk impact analysis per vulnerability
- Business consequences for each finding
- Step-by-step remediation recommendations
- OWASP API Security Top 10 mapping

---

## 🧠 Key Takeaways

Through this project, I developed hands-on experience in:

- **API security testing** using Postman — from endpoint mapping to response analysis
- **OWASP API Top 10** methodology applied to a real-world REST API
- **Risk classification** — translating raw findings into business-level impact
- **Professional report writing** — clear, structured, and actionable security documentation
- Understanding the difference between **functional testing** and **security testing**

---

## ⚖️ Ethical Compliance

This assessment was performed **exclusively on a public sandbox API** (JSONPlaceholder) intended for testing purposes. All activities strictly adhered to the **read-only rule** — no exploitation, brute-forcing, or Denial of Service (DoS) tests were conducted.

---

## 📁 Repository Structure

```
FUTURE_CS_03/
├── README.md                        # Project overview (this file)
├── Task3_API_Security_Report_v2.pdf # Full technical security report
├── screenshot 1.png                 # Unauthenticated endpoint test
├── screenshot 2.png                 # PII leakage evidence
├── screenshot 3.png                 # Missing security headers
├── screenshot 4.png                 # Postman endpoint collection
└── screenshot 5.png                 # Risk summary overview
```

---

## 👤 Author

**Richmond Konan** — Cybersecurity Analyst Junior | SOC | Network Security  
📍 Côte d'Ivoire  
🔗 [LinkedIn](https://linkedin.com/in/richmonddelmas) • [GitHub](https://github.com/ixsecure) • [Portfolio](https://beacons.ai/richmonddelmas)  
📩 delmasrichmond@gmail.com

---

## 🏷️ Topics

`api-security` `owasp` `postman` `cybersecurity` `penetration-testing` `rest-api` `vulnerability-assessment` `internship` `security-audit` `pii`

# API Security Risk Analysis Report
**Cybersecurity Internship | Task 03**

## Executive Summary
This repository features a comprehensive security assessment of a public REST API. The project focuses on identifying systemic vulnerabilities, evaluating business risks, and providing actionable remediation strategies. The assessment was conducted following industry-standard methodologies to ensure a thorough audit of authentication, data exposure, and transport security.

## Project Objectives
* **Vulnerability Assessment:** Identify flaws in authentication mechanisms and access control.
* **Data Privacy Audit:** Detect unauthorized Exposure of Personally Identifiable Information (PII).
* **Risk Communication:** Translate technical findings into business-centric risk impact statements.
* **Strategic Remediation:** Develop clear, prioritized steps for vulnerability mitigation.

## Methodology & Tooling
The assessment followed a non-intrusive, read-only approach focused on the **JSONPlaceholder** ecosystem.

### Technical Stack
| Outil | Usage |
| :--- | :--- |
| **Postman** | Used for automated request crafting and response payload analysis. |
| **Browser DevTools** | Utilized for deep-packet inspection of HTTP headers and network latency. |

### Audit Workflow
1. **Reconnaissance:** Detailed analysis of API documentation and endpoint mapping.
2. **Traffic Analysis:** Manual inspection of HTTP response headers and status codes.
3. **Security Profiling:** Classification of risks based on severity (Low to Critical).
4. **Reporting:** Documentation of findings with supporting evidence and patches.

## Vulnerability Assessment Matrix

| ID | Vulnerability | Severity | Status |
| :--- | :--- | :--- | :--- |
| **01** | Missing Authentication | **HIGH** | Documented |
| **02** | Excessive Data Exposure (PII Leakage) | **CRITICAL** | Documented |
| **03** | Missing Security Headers | **MEDIUM** | Documented |

### Key Findings
* **Broken Access Control:** The `/users` endpoint returns sensitive data including GPS coordinates and private contact details with a `200 OK` status without requiring an API key or JWT.
* **Information Leakage:** The `/comments` and `/posts` endpoints expose internal metadata and user email addresses to unauthenticated requests.
* **Weak Transport Security:** Lack of modern security headers increases the surface area for Man-in-the-Middle (MitM) and Injection attacks.

## Repository Structure
* `Task3_API_Security_Report.pdf`: The full technical dossier including risk impact and remediation.
* `screenshots/`: Evidence of API responses and header configurations.
* `README.md`: Project overview and summary.

## Ethical Compliance
This assessment was performed exclusively on a public sandbox API intended for testing. All activities adhered to the "Read-Only" rule; no exploitation, brute-forcing, or Denial of Service (DoS) tests were conducted.


API Security Risk Analysis Report
Future Interns — Cybersecurity Internship | Task 3 | April 2026
 Overview
This repository contains the API Security Risk Analysis Report completed as part of the Future Interns Cybersecurity Internship (Task 3).
The assessment was performed on a public demo API to identify common security vulnerabilities, classify risks, and suggest remediation steps — following ethical and legal guidelines.
 Objective
Analyze a public/demo API for security risks
Identify authentication and access control issues
Detect data exposure vulnerabilities
Explain risks in simple, business-friendly language
Suggest clear remediation steps
🛠️ Tools Used
Tool
Purpose
Postman
Send API requests and inspect responses
Browser DevTools (Chrome)
Inspect HTTP headers and network traffic
JSONPlaceholder API
Public demo API used as test target
 Target API
Name: JSONPlaceholder
URL: https://jsonplaceholder.typicode.com
Type: Public demonstration API (safe and legal to test)
🔍 Scope & Methodology
✅ Allowed
Testing public/demo APIs only
Read-only GET requests
Inspecting headers and API responses
Documentation analysis
❌ Forbidden
Any exploitation or bypass attempts
Flood tests / DoS attacks
Attacking private or production APIs
Methodology Steps
Selected a public demo API (JSONPlaceholder)
Reviewed API documentation
Tested endpoints using Postman (GET requests only)
Inspected authentication requirements
Analyzed HTTP response headers
Identified security risks
Classified risk severity (Low / Medium / High / Critical)
Proposed remediation steps
Documented all findings in a professional report
🚨 Vulnerabilities Found
#
Vulnerability
Risk Level
Status
1
Missing Authentication
HIGH
Documented
2
Excessive Data Exposure
CRITICAL
Documented
3
Missing Security Headers
MEDIUM
Documented
📁 Repository Contents
FUTURE_CS_03/
│
├── README.md                          ← This file
├── Task3_API_Security_Report.pdf      ← Full security report
└── screenshots/
    ├── postman_users_response.jpg     ← GET /users result
    ├── postman_users_headers.jpg      ← Response headers
    ├── postman_posts_response.jpg     ← GET /posts result
    └── postman_comments_response.jpg  ← GET /comments result
📊 Key Findings Summary
GET /users → Exposes names, emails, addresses, GPS coordinates, phone numbers without any authentication (200 OK)
GET /posts → Exposes 7.98 KB of internal publications without authentication (200 OK)
GET /comments → Exposes 40.77 KB of emails and comments without authentication (200 OK)
Response Headers → Missing X-Frame-Options, Content-Security-Policy, Strict-Transport-Security, X-Content-Type-Options
✅ Ethical Statement
This assessment was conducted ethically using read-only methods only.
No exploitation, bypass attempts, or unauthorized access was performed.
All testing followed the Future Interns ethical guidelines.
👤 Author
Richmond Delmas
Future Interns — Cybersecurity Intern
April 2026

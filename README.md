# Cybersecurity Portfolio

**Maximilian Rivera** | Security Operations & Incident Response | GRC & Compliance | HIPAA | Prior U.S. Government Clearance

---

## About Me

U.S. Air Force veteran with a prior U.S. government security clearance and a background in compliance operations, audit documentation, and regulatory adherence in high-stakes environments. Google Cybersecurity Certificate, June 2026. Served as compliance lead for QA product hold events in a HIPAA-regulated medical supply chain — collecting evidence, applying quarantine controls, maintaining audit trails, and safeguarding PHI in coordination with regional management. Built GRC documentation across HIPAA Security Rule, NIST CSF, ISO 27001, PCI DSS, and SOC 2. Lean Six Sigma Yellow Belt. Targeting healthcare compliance, GRC analyst, and HIPAA-focused roles where operational compliance experience and hands-on GRC documentation translate directly to day-one value.

---

## Independent Projects

### 1. Internal Security Audit — Meridian Health Group
**Type:** Controls & Compliance Assessment
**Frameworks:** NIST CSF | PCI DSS | GDPR | SOC Type 1 & 2
**Risk Score:** 8/10 (High)

Conducted a simulated internal IT security audit for a mid-sized healthcare organization. Evaluated 14 security controls across three regulatory frameworks. Identified critical gaps in encryption, access control, and disaster recovery. Produced a formal checklist with prioritized remediation recommendations.

**Key Findings:**
- 9 of 14 controls not in place including encryption, IDS, and least privilege
- Full PCI DSS non-compliance — no encryption or password management
- Partial GDPR compliance — breach notification exists but data classification does not
- Recommendations focused on encryption, IDS deployment, DR planning, and separation of duties

[View Checklist](audits/MHG_Checklist.pdf)

---

### 2. Incident Report — DoS Attack via ICMP Flood
**Type:** Incident Response & Analysis
**Framework:** NIST Cybersecurity Framework (CSF)

Analyzed a denial-of-service attack in which a threat actor flooded an internal network with ICMP packets through an unconfigured firewall, causing a two-hour outage. Applied all five NIST CSF functions to document the incident and build a remediation plan.

**Key Actions:**
- Identified misconfigured firewall as the root vulnerability
- Implemented ICMP rate limiting and source IP verification
- Deployed IDS/IPS and network monitoring for ongoing detection
- Staged service restoration prioritizing critical systems first

[View Report](incident-reports/NIST_CSF_Portfolio_Report.pdf)

---

### 3. Incident Report — Brute Force & Network Traffic Analysis
**Type:** Security Incident Response
**Tools:** Wireshark | tcpdump | Network Protocol Analysis

Investigated a brute force attack and concurrent abnormal network traffic event. Captured and analyzed packet data to identify attack vectors, document findings, and recommend hardening measures.

**Key Actions:**
- Identified failed authentication patterns consistent with credential stuffing
- Analyzed PCAP data to trace attack origin and lateral movement indicators
- Documented timeline, affected systems, and evidence chain
- Recommended account lockout policies, MFA enforcement, and network segmentation

[View Report](incident-reports/Brute_Force_Security_Incident_Report.docx)

---

### 4. Incident Report — SYN Flood Attack Response
**Type:** Network Security Incident
**Framework:** NIST SP 800-61 | TCP/IP Protocol Analysis

Analyzed a SYN flood attack targeting a web-facing server. Identified the attack pattern using packet analysis, documented the incident lifecycle, and produced hardening recommendations to prevent recurrence.

**Key Actions:**
- Identified half-open connection accumulation consistent with SYN flood
- Traced attack traffic and documented source patterns
- Recommended SYN cookies, rate limiting, and firewall ACL updates
- Produced formal incident report with timeline and remediation plan

[View Report](incident-reports/SYN_Flood_Incident_Report_Completed.docx)

---

### 5. File Permissions in Linux
**Type:** Linux Authorization & Access Control
**Concepts:** Principle of Least Privilege | chmod | File Permission Strings

Audited and corrected file system permissions for a research team in a Linux environment. Used `ls -la` to identify permission mismatches against policy, then applied `chmod` to remove unauthorized access and restrict sensitive files.

**Key Actions:**
- Removed write access for others on project_k.txt (`chmod o-w`)
- Secured hidden file .project_x.txt to read-only (`chmod u-w,g-w,g+r`)
- Restricted drafts directory to owner only (`chmod g-x`)
- Interpreted and documented 10-character Linux permission strings

[View Report](incident-reports/File_Permissions_in_Linux.pdf)

---

### 6. SQL Filters for Security Investigation
**Type:** Database Investigation & Security Analysis
**Tools:** SQL (MariaDB) | AND, OR, NOT, LIKE operators

Investigated two potential security incidents using SQL filters against login and employee machine databases. Wrote targeted queries to isolate after-hours failed logins, suspicious date-range activity, and logins from unexpected geographies.

**Key Actions:**
- Filtered failed login attempts after 18:00 using AND with time comparison
- Retrieved login activity across a two-day window using OR on date values
- Excluded logins from specific country using NOT LIKE with wildcard
- Isolated employees by department and office location for security update deployment

[View Report](incident-reports/Apply_Filters_to_SQL_Queries.pdf)

---

### 7. Algorithm for File Updates in Python
**Type:** Security Automation & Python Scripting
**Tools:** Python | File I/O | String Manipulation

Built a Python algorithm to automate allow-list management for an IP-based access control system. The script reads an existing allow list, removes IPs that appear on a remove list, and writes the updated list back — eliminating manual error in a routine security maintenance task.

**Key Actions:**
- Read allow list file contents into a working string using `.read()`
- Converted string to list with `.split()` for iteration
- Iterated through remove list and deleted matching IPs using `.remove()`
- Rejoined and wrote updated allow list back to file with `.join()` and `.write()`

[View Report](incident-reports/Algorithm_for_File_Updates_in_Python.pdf)

---

### 8. Vulnerability Assessment Report
**Type:** Risk & Vulnerability Assessment
**Framework:** NIST SP 800-30 | Threat Modeling

Conducted a vulnerability assessment for a simulated organization. Identified attack surfaces, evaluated likelihood and impact of key threats, and produced a formal risk assessment with prioritized remediation recommendations.

**Key Actions:**
- Identified and categorized vulnerabilities across network, application, and physical layers
- Applied NIST SP 800-30 threat likelihood and impact scoring
- Prioritized findings by risk rating and business impact
- Produced formal report with remediation roadmap

[View Report](incident-reports/Vulnerability_Assessment_Report.pdf)

---

### 9. Policy Development & GRC Lab — VoltEdge Systems
**Type:** GRC | Security Policy Writing | Risk Management
**Frameworks:** NIST CSF | NIST SP 800-30 | ISO 27001 | HIPAA-aligned

Drafted two production-ready security policies and a full GRC risk and compliance package for VoltEdge Systems, a simulated mid-size technology firm. Policies cover acceptable use and formal incident response. GRC package includes risk register, BIA, and RACI matrix.

**Key Actions:**
- Authored Acceptable Use Policy (AUP) covering device use, data handling, and violation consequences
- Authored Incident Response Policy aligned with NIST SP 800-61 phases
- Built risk register, Business Impact Analysis, and RACI matrix to NIST SP 800-30
- Defined roles, responsibilities, escalation paths, and 72-hour breach notification triggers

[View AUP](policies/VoltEdge_Acceptable_Use_Policy.pdf) | [View IR Policy](policies/VoltEdge_Incident_Response_Policy.pdf) | [View GRC Workbook](policies/VoltEdge_GRC_Risk_Compliance_Package.xlsx)

---

### 10. Healthcare Vendor Risk Assessment — ClearPath Health
**Type:** Third-Party Risk Management | HIPAA Compliance
**Frameworks:** HIPAA Security Rule (45 CFR Part 164) | ISO 27001:2022 Annex A | SOC 2 Type II

Conducted a full third-party vendor risk assessment for ClearPath Health, Inc., a telehealth SaaS platform seeking onboarding as a Business Associate for Lakewood Regional Medical Center. Evaluated security posture using a 40-question questionnaire and documentation review including SOC 2 report, security policies, and penetration test summary.

**Key Findings:**
- 12 total findings: 3 Critical, 4 High, 3 Medium, 2 Low
- Critical: No MFA on admin accounts, no executed BAAs with subprocessors, no HIPAA incident response plan
- 71% overall questionnaire compliance across 6 security domains
- Issued conditional approval with 90-day remediation plan and 15/30-day hard deadlines

[View Assessment](vendor-risk-assessment/Vendor_Risk_Assessment_ClearPath_Health.pdf)

---

### 11. Healthcare Compliance Mapping Matrix
**Type:** GRC | Multi-Framework Compliance Mapping
**Frameworks:** HIPAA Security Rule | NIST CSF | ISO 27001:2022 Annex A | SOC 2 Type II

Built a comprehensive compliance mapping matrix for Lakewood Regional Medical Center, mapping 33 HIPAA Security Rule controls across NIST CSF, ISO 27001:2022 Annex A, and SOC 2 Type II. Includes control-by-control status assessment, risk ratings, evidence requirements, owners, and remediation target dates.

**Key Outputs:**
- 33 controls mapped across 4 frameworks with COMPLIANT / PARTIAL / NON-COMPLIANT status
- 20 compliant (61%), 7 partial (21%), 6 non-compliant (18%)
- Summary dashboard with compliance rates by HIPAA safeguard type and NIST CSF function
- Document control and high-priority gap tracking for executive reporting

[View Matrix](compliance-matrix/Healthcare_Compliance_Mapping_Matrix.xlsx)

---

### 12. Zero Trust Identity & Access Management Lab — Meridian Health Group
**Type:** Identity & Access Management | Microsoft Entra ID | Zero Trust Architecture
**Frameworks:** NIST SP 800-207 Zero Trust Architecture | HIPAA Security Rule | NIST CSF 2.0 | CIS Controls v8

Built a full identity and access management (IAM) lab for a simulated healthcare organization using Microsoft Entra ID. The goal was simple: make sure the right people have access to the right things — and nobody has more access than they need for their job.

Set up 10 user accounts across 6 departments, organized them into 10 security groups, and assigned roles based on least privilege. Enabled multi-factor authentication for all users. Documented 7 conditional access policies that control who can log in, from where, and on what device. Built an access review process and a full Joiners-Movers-Leavers workflow so the organization always knows who has access and why.

**Key Actions:**
- Created 10 user accounts (employees, service accounts, external vendor) with role-based access control and least privilege applied to every role
- Configured 10 security groups used to target authentication policies and Microsoft 365 permissions
- Documented 7 Conditional Access policies — MFA for all users, blocking outdated login methods, geo-restricting access to the US, requiring compliant devices for admin accounts, and restricting vendor access
- Built a Joiners-Movers-Leavers (JML) workflow with defined timelines: accounts enabled within 24 hours of hire, disabled within 4 hours of termination
- Completed two quarterly access review cycles — reviewed every role assignment, documented decisions, and removed access that was no longer needed
- Identified 6 security findings with risk ratings and a prioritized fix plan aligned to HIPAA and NIST

[View IAM Lab Report](zero-trust-iam-lab/MHG_ZeroTrust_IAM_Lab_Report.docx) | [View RBAC Matrix](zero-trust-iam-lab/MHG_RBAC_Matrix_ZeroTrust_IAM.xlsx)

---

## Skills & Tools

- **Security Tools:** Splunk (SPL) • Chronicle (YARA-L) • Wazuh • Suricata • Wireshark • tcpdump • Linux CLI • SQL (MariaDB) • Python • Microsoft Entra ID
- **Security Operations:** Incident Response (NIST SP 800-61) • IDS Rule Tuning • Threat Detection • Vulnerability Assessment • Threat Modeling • CIA Triad • Access Control • Identity & Access Management (IAM) • Zero Trust Architecture • RBAC
- **GRC & Compliance:** HIPAA Security Rule • NIST CSF • NIST RMF • NIST SP 800-30/800-53/800-207 • ISO 27001:2022 • PCI DSS • SOC 2 Type II • Vendor Risk Assessment • Compliance Mapping • Risk Register • Policy Writing
- **Enterprise Systems:** SAP • AIMS • SmartSolve • Microsoft Office (Advanced Excel) • RF Warehouse Systems

---

## Certifications

- Google Cybersecurity Certificate — Coursera, June 2026
- SC-900: Microsoft Security, Compliance & Identity Fundamentals — June 2026
- Lean Six Sigma Yellow Belt — Cardinal Health, 2023
- Prior U.S. Government Security Clearance — U.S. Air Force, 2007–2011

---

## Contact

- **LinkedIn:** [linkedin.com/in/riveramaximilian](https://www.linkedin.com/in/maximilianrivera)
- **Email:** riveramaximilian@gmail.com

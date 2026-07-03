# GRC & Compliance Portfolio

**Maximilian Rivera** | GRC & Compliance | HIPAA · SOC 2 · ISO 27001 · PCI DSS | Security Operations & Incident Response | Prior U.S. Government Clearance

---

## About Me

I'm a U.S. Air Force veteran with a prior government security clearance and five years running compliance operations in a HIPAA-regulated pharmaceutical supply chain. I've served as compliance owner for QA product hold events: collecting audit evidence, applying quarantine controls, and safeguarding PHI in coordination with regional management.

Outside that day job, I built the GRC portfolio below, covering HIPAA, NIST CSF, ISO 27001, PCI DSS, and SOC 2. It includes a completed third-party vendor risk assessment, a 33-control compliance mapping matrix, and a full HIPAA security risk analysis for an 85,000-patient network.

Google Cybersecurity Certificate, June 2026. Lean Six Sigma Yellow Belt. I'm looking for compliance analyst, GRC analyst, and HIPAA-focused roles where this operational and applied GRC background delivers value from day one.

---

## GRC & Compliance Projects

### 1. Third-Party Vendor Risk Assessment (ClearPath Health)

**Type:** Third-Party Risk Management | HIPAA Compliance
**Frameworks:** HIPAA Security Rule (45 CFR Part 164) | ISO 27001:2022 Annex A | SOC 2 Type II

Ran a full vendor risk assessment for a telehealth SaaS platform seeking onboarding as a Business Associate for a regional medical center. Evaluated security posture using a 40-question questionnaire and a documentation review covering the vendor's SOC 2 report, security policies, and penetration test summary.

**Key Findings:**
- 12 total findings: 3 Critical, 4 High, 3 Medium, 2 Low
- Critical: no MFA on admin accounts, no executed BAAs with subprocessors, no HIPAA incident response plan
- 71% overall questionnaire compliance across 6 security domains
- Issued conditional approval with a 90-day remediation plan and 15/30-day hard deadlines

[View Assessment](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/vendor-risk-assessment/Vendor_Risk_Assessment_ClearPath_Health.pdf)

---

### 2. Healthcare Compliance Mapping Matrix

**Type:** GRC | Multi-Framework Compliance Mapping
**Frameworks:** HIPAA Security Rule | NIST CSF | ISO 27001:2022 Annex A | SOC 2 Type II

Built a compliance mapping matrix for a regional medical center, mapping 33 HIPAA Security Rule controls across NIST CSF, ISO 27001:2022 Annex A, and SOC 2 Type II. Includes a control-by-control status assessment, risk ratings, evidence requirements, owners, and remediation target dates.

**Key Outputs:**
- 33 controls mapped across 4 frameworks with compliant / partial / non-compliant status
- 20 compliant (61%), 7 partial (21%), 6 non-compliant (18%)
- Summary dashboard with compliance rates by HIPAA safeguard type and NIST CSF function
- Document control and high-priority gap tracking for executive reporting

[View Matrix](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/compliance-matrix/Healthcare_Compliance_Mapping_Matrix.xlsx)

---

### 3. Internal Security Audit (Meridian Health Group)

**Type:** Controls & Compliance Assessment
**Frameworks:** NIST CSF | PCI DSS | GDPR | SOC Type 1 & 2
**Risk Score:** 8/10 (High)

Ran an internal IT security audit for a mid-sized healthcare organization. Evaluated 14 security controls across three regulatory frameworks, found critical gaps in encryption, access control, and disaster recovery, and produced a formal checklist with prioritized remediation.

**Key Findings:**
- 9 of 14 controls not in place, including encryption, IDS, and least privilege
- Full PCI DSS non-compliance: no encryption, no password management
- Partial GDPR compliance: breach notification exists, data classification does not
- Recommendations covered encryption, IDS deployment, DR planning, and separation of duties

[View Checklist](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/audits/MHG_Checklist.pdf)

---

### 4. HIPAA Security Risk Analysis (SunRidge Health Partners)

**Type:** GRC | Security Risk Analysis
**Frameworks:** HIPAA Security Rule (45 CFR Part 164) | NIST SP 800-30 Rev. 1 | NIST CSF 2.0
**Risk Register:** 10 risks scored | 3 Critical findings

Ran a full HIPAA Security Risk Analysis for an 85,000-patient health network. Inventoried 7 ePHI systems, scored 10 risk scenarios using NIST SP 800-30 Likelihood x Impact methodology, and assessed 30 HIPAA Security Rule controls across Administrative, Physical, and Technical Safeguards.

**Key Findings:**
- Critical: ransomware threat vector, no DMARC, no phishing simulations, annual-only training
- Critical: third-party clearinghouse handling 100% of revenue cycle operations, BAA unreviewed since 2021, no BCP
- Critical: active web tracking pixel PHI disclosure via analytics tags, in violation of HHS OCR guidance
- 47% of assessed controls returned as a complete gap, no adequate control in place

**Deliverables:**
- Risk register with 10 scored risk scenarios
- 30-control HIPAA gap analysis
- 4-phase remediation roadmap, 365 days, roughly $303,500
- Executive summary mapped against the HHS HIPAA Security Rule NPRM

[View SRA Workbook](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/hipaa-security-risk-analysis/SunRidge_HIPAA_SRA_2025.xlsx) | [View Executive Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/hipaa-security-risk-analysis/SunRidge_HIPAA_SRA_Executive_Report_2025.docx)

---

### 5. Policy Development & GRC Lab (VoltEdge Systems)

**Type:** GRC | Security Policy Writing | Risk Management
**Frameworks:** NIST CSF | NIST SP 800-30 | ISO 27001 | HIPAA-aligned

Drafted two production-ready security policies and a full GRC risk and compliance package for a mid-size technology firm. Policies cover acceptable use and formal incident response. The GRC package includes a risk register, BIA, and RACI matrix.

**Key Actions:**
- Wrote an Acceptable Use Policy covering device use, data handling, and violation consequences
- Wrote an Incident Response Policy aligned to NIST SP 800-61 phases
- Built a risk register, Business Impact Analysis, and RACI matrix to NIST SP 800-30
- Defined roles, responsibilities, escalation paths, and 72-hour breach notification triggers

[View AUP](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/policies/VoltEdge_Acceptable_Use_Policy.pdf) | [View IR Policy](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/policies/VoltEdge_Incident_Response_Policy.pdf) | [View GRC Workbook](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/policies/VoltEdge_GRC_Risk_Compliance_Package.xlsx)

---

### 6. Zero Trust Identity & Access Management Lab (Meridian Health Group)

**Type:** Identity & Access Management | Microsoft Entra ID | Zero Trust Architecture
**Frameworks:** NIST SP 800-207 Zero Trust Architecture | HIPAA Security Rule | NIST CSF 2.0 | CIS Controls v8

Built a full IAM lab for a healthcare organization using Microsoft Entra ID, with the goal of making sure the right people have access to the right things and nobody has more than they need.

Set up 10 user accounts across 6 departments, organized into 10 security groups, with roles assigned on least privilege. Enabled MFA for all users, documented 7 conditional access policies, and built a full Joiners-Movers-Leavers workflow so the organization always knows who has access and why.

**Key Actions:**
- Created 10 user accounts (employees, service accounts, external vendor) with RBAC and least privilege on every role
- Configured 10 security groups used to target authentication policies and Microsoft 365 permissions
- Documented 7 Conditional Access policies: MFA for all users, blocking outdated login methods, geo-restricting access, requiring compliant devices for admin accounts, and restricting vendor access
- Built a JML workflow: accounts enabled within 24 hours of hire, disabled within 4 hours of termination
- Ran two quarterly access review cycles, reviewed every role assignment, documented decisions, and removed unneeded access
- Flagged 6 security findings with risk ratings and a prioritized fix plan aligned to HIPAA and NIST

[View IAM Lab Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/zero-trust-iam-lab/MHG_ZeroTrust_IAM_Lab_Report.docx) | [View RBAC Matrix](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/zero-trust-iam-lab/MHG_RBAC_Matrix_ZeroTrust_IAM.xlsx)

---

### 7. SOC 2 Readiness Assessment (Crestline Technology Partners)

**Type:** GRC | Audit Readiness
**Frameworks:** SOC 2 Type II | Trust Services Criteria (CC6, CC7, CC9)

Ran a SOC 2 readiness assessment ahead of a Type II audit for a mid-size technology firm. Evaluated 22 controls across logical access (CC6), system operations (CC7), and risk mitigation (CC9).

**Key Findings:**
- Identified 14 control gaps across the three trust services categories evaluated
- Issued a formal management letter documenting each gap and its associated risk
- Built a 12-month phased remediation roadmap to close gaps ahead of the audit window

[View Report](#) *(link pending)*

---

## Google Cybersecurity Certificate — Applied Labs

Completed as part of the Google Cybersecurity Certificate program. These labs cover incident response, network analysis, and security fundamentals, and back up the technical literacy behind the GRC work above.

### 8. Vulnerability Assessment Report

**Type:** Risk & Vulnerability Assessment | **Framework:** NIST SP 800-30 | Threat Modeling

Ran a vulnerability assessment for a mid-size organization. Identified attack surfaces, scored likelihood and impact of key threats, and produced a formal risk assessment with prioritized remediation.

**Key Actions:**
- Categorized vulnerabilities across network, application, and physical layers
- Applied NIST SP 800-30 threat likelihood and impact scoring
- Prioritized findings by risk rating and business impact
- Produced a formal report with a remediation roadmap

[View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/Vulnerability_Assessment_Report.pdf)

---

### 9. Incident Report (DoS Attack via ICMP Flood)

**Type:** Incident Response & Analysis | **Framework:** NIST Cybersecurity Framework (CSF)

Analyzed a denial-of-service attack where a threat actor flooded an internal network with ICMP packets through an unconfigured firewall, causing a two-hour outage. Applied all five NIST CSF functions to document the incident and build a remediation plan.

**Key Actions:**
- Identified the misconfigured firewall as the root vulnerability
- Implemented ICMP rate limiting and source IP verification
- Deployed IDS/IPS and network monitoring for ongoing detection
- Staged service restoration, prioritizing critical systems first

[View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/NIST_CSF_Portfolio_Report.pdf)

---

### 10. Incident Report (Brute Force & Network Traffic Analysis)

**Type:** Security Incident Response | **Tools:** Wireshark | tcpdump | Network Protocol Analysis

Investigated a brute force attack alongside an abnormal network traffic event. Captured and analyzed packet data to identify attack vectors, document findings, and recommend hardening measures.

**Key Actions:**
- Identified failed authentication patterns consistent with credential stuffing
- Analyzed PCAP data to trace attack origin and lateral movement indicators
- Documented the timeline, affected systems, and evidence chain
- Recommended account lockout policies, MFA enforcement, and network segmentation

[View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/Brute_Force_Security_Incident_Report.docx)

---

### 11. Incident Report (SYN Flood Attack Response)

**Type:** Network Security Incident | **Framework:** NIST SP 800-61 | TCP/IP Protocol Analysis

Analyzed a SYN flood attack targeting a web-facing server. Identified the attack pattern through packet analysis, documented the incident lifecycle, and produced hardening recommendations to prevent recurrence.

**Key Actions:**
- Identified half-open connection accumulation consistent with a SYN flood
- Traced attack traffic and documented source patterns
- Recommended SYN cookies, rate limiting, and firewall ACL updates
- Produced a formal incident report with timeline and remediation plan

[View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/SYN_Flood_Incident_Report_Completed.docx)

---

### 12. Security Fundamentals Practice

**Type:** Coursework Labs | **Tools:** SQL (MariaDB) · Linux CLI · Python

Three short labs from the certificate coursework, each demonstrating a different fundamental: querying, access control, and automation.

- **SQL Filters for Security Investigation:** wrote targeted SQL queries (AND, OR, NOT LIKE) against login and employee databases to isolate after-hours failed logins, suspicious date ranges, and logins from unexpected geographies. [View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/Apply_Filters_to_SQL_Queries.pdf)
- **File Permissions in Linux:** audited and corrected file system permissions for a research team, using `ls -la` and `chmod` to remove unauthorized access and enforce least privilege. [View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/File_Permissions_in_Linux.pdf)
- **Algorithm for File Updates in Python:** built a script to automate allow-list management for an IP-based access control system, reading, filtering, and rewriting the list programmatically. [View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/incident-reports/Algorithm_for_File_Updates_in_Python.pdf)

---

## Skills & Tools

- **GRC & Compliance:** HIPAA Security Rule · NIST CSF · NIST RMF · NIST SP 800-30/800-53/800-207 · ISO 27001:2022 · PCI DSS · SOC 2 Type II · Vendor Risk Assessment · Compliance Mapping · Risk Register · Policy Writing
- **Security Operations:** Incident Response (NIST SP 800-61) · IDS Rule Tuning · Threat Detection · Vulnerability Assessment · Threat Modeling · Access Control · Identity & Access Management (IAM) · Zero Trust Architecture · RBAC
- **Security Tools:** Splunk (SPL) · Chronicle (YARA-L) · Wazuh · Suricata · Wireshark · tcpdump · Linux CLI · SQL (MariaDB) · Python · Microsoft Entra ID
- **Enterprise Systems:** SAP · AIMS · SmartSolve · Microsoft Office (Advanced Excel) · RF Warehouse Systems

---

## Certifications

- Google Cybersecurity Certificate, Coursera, June 2026
- SC-900: Microsoft Security, Compliance & Identity Fundamentals, June 2026
- Lean Six Sigma Yellow Belt, Cardinal Health, 2023
- Prior U.S. Government Security Clearance, U.S. Air Force, 2007 to 2011

---

## Contact

- **LinkedIn:** [linkedin.com/in/maximilianrivera](https://www.linkedin.com/in/maximilianrivera)
- **Email:** riveramaximilian@gmail.com

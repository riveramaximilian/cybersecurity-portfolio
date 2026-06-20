# Cybersecurity Portfolio

**Maximilian Rivera** | Security Operations & Incident Response | GRC & Compliance

---

## About Me

Air Force veteran with a prior government clearance and 15 years building reliable systems in environments where errors have consequences. Google Cybersecurity Certificate completed June 2026. I have designed processes from scratch, cut error rates by 30 percent in a regulated healthcare environment, and built GRC documentation across NIST, HIPAA, PCI DSS, and SOC 2.

I detect anomalies, investigate alerts, and document findings end to end. Trained in NIST SP 800-61 incident response, IDS rule tuning, and threat detection across Splunk, Chronicle, Wazuh, and Suricata. Lean Six Sigma Yellow Belt.

---

## Independent Projects

### 1. Internal Security Audit - Meridian Health Group
**Type:** Controls & Compliance Assessment
**Frameworks:** NIST CSF | PCI DSS | GDPR | SOC Type 1 & 2
**Risk Score:** 8/10 (High)

Conducted a simulated internal IT security audit for a mid-sized healthcare organization. Evaluated 14 security controls and assessed compliance across three regulatory frameworks. Identified critical gaps in encryption, access control, and disaster recovery, and produced a formal checklist with prioritized remediation recommendations.

**Key Findings:**
- 9 of 14 controls not in place, including encryption, IDS, and least privilege
- Full PCI DSS non-compliance - no encryption or password management system
- Partial GDPR compliance - breach notification plan exists but data classification does not
- Recommendations focused on encryption, IDS deployment, DR planning, and separation of duties

[View Checklist](audits/MHG_Checklist.pdf)

---

### 2. Incident Report Analysis - DoS Attack via ICMP Flood
**Type:** Incident Response & Analysis
**Framework:** NIST Cybersecurity Framework (CSF)

Analyzed a denial of service attack in which a malicious actor flooded an organization's internal network with ICMP packets through an unconfigured firewall, causing a two-hour outage. Applied all five NIST CSF functions to document the incident and establish a remediation plan.

**Key Actions:**
- Identified misconfigured firewall as the root vulnerability
- Implemented ICMP rate limiting and source IP verification at the firewall
- Deployed IDS/IPS and network monitoring software for ongoing detection
- Staged service restoration prioritizing critical systems first

[View Report](incident-reports/NIST_CSF_Portfolio_Report.pdf)

---

### 3. File Permissions in Linux
**Type:** Linux Authorization & Access Control
**Concepts:** Principle of Least Privilege | chmod | File Permission Strings

Audited and corrected file system permissions for a research team on a Linux environment. Used ls -la to identify permission mismatches against organizational policy, then applied chmod to remove unauthorized write access, secure a hidden archived file, and restrict a directory to its owner only.

**Key Actions:**
- Removed write access for others on project_k.txt (chmod o-w)
- Secured hidden file .project_x.txt to read-only for user and group (chmod u-w,g-w,g+r)
- Restricted drafts directory to owner only (chmod g-x)
- Interpreted and documented 10-character Linux permission strings

[View Report](incident-reports/File_Permissions_in_Linux.pdf)

### 4. Apply Filters to SQL Queries
**Type:** Database Investigation & Security Analysis
**Tools:** SQL (MariaDB) | AND, OR, NOT, LIKE operators

Investigated two potential security incidents using SQL filters against an organization's login attempt and employee machine database. Wrote targeted queries to isolate after-hours failed logins, suspicious date-range activity, and logins originating outside of Mexico.

**Key Actions:**
- Filtered failed login attempts after 18:00 using AND with a time comparison
- Retrieved login activity across a two-day window using OR on date values
- Excluded Mexican login attempts using NOT with LIKE and the % wildcard
- Isolated Marketing employees in East building offices using AND with pattern matching
- Identified all non-IT employees using NOT for department-wide exclusion

[View Report](incident-reports/Apply_Filters_to_SQL_Queries.pdf)

---

### 5. Vulnerability Assessment Report
**Type:** Risk Assessment & Remediation Planning
**Framework:** NIST SP 800-30 | CVE | CVSS

Performed a vulnerability assessment on an organization's publicly accessible MySQL database server running on Linux. Evaluated three threat scenarios using NIST SP 800-30 likelihood and severity ratings and produced a prioritized remediation plan.

**Key Findings:**
- Unauthorized data exfiltration rated Critical (likelihood 3 x severity 3 = 9)
- Competitor denial of service rated High (2 x 3 = 6) due to single point of failure
- Insider data alteration rated Moderate (2 x 2 = 4) due to lack of role-based access controls
- Remediation focused on MFA, IP allowlisting, TLS encryption, and least privilege access

[View Report](incident-reports/Vulnerability_Assessment_Report.pdf)

### 6. Incident Handler's Journal
**Type:** Incident Documentation & Tool Exploration
**Framework:** NIST Incident Response Lifecycle

Maintained a four-entry security journal documenting incident investigations and tool exploration. Entries cover a ransomware attack on a healthcare clinic, a spear phishing campaign, and hands-on use of Suricata IDS and Wazuh SIEM.

**Key Entries:**
- Ransomware at a healthcare clinic: analyzed attack vector, impact, and recovery gaps
- Spear phishing at Imaginary Bank: dissected a targeted email to confirm malicious intent
- Suricata: reviewed rule syntax, EVE JSON output, and flow-based filtering
- Wazuh: queried indexed SSH login failures to identify a brute force pattern against root

[View Journal](incident-reports/Incident_Handlers_Journal.pdf)

### 7. Algorithm for File Updates in Python
**Type:** Python Automation & File Management
**Concepts:** File I/O | String Parsing | Access Control Automation

Developed a Python algorithm to automate updates to an IP allow list used for access control. The script reads the current allow list, removes flagged IPs, and writes the updated list back to file.

**Key Actions:**
- Read and parsed file contents using with open() and .split()
- Iterated through remove list and conditionally removed matching entries
- Applied principle of least privilege by ensuring only authorized IPs retain access

[View Report](incident-reports/Algorithm_for_File_Updates_in_Python.pdf)

### 8. VoltEdge Systems GRC Lab
**Type:** GRC Documentation | Risk Management
**Concepts:** NIST SP 800-30 | SOC 2 | CCPA | Risk Register | BIA | RACI

Built a complete GRC documentation package for a fictional EV fleet management company from scratch. Risk register (15 risks), business impact analysis (10 functions, RTO/RPO/financial impact), and RACI matrix (15 controls x 10 roles) - all structured for an actual audit.

### 9. VoltEdge Systems Policy Writing
**Type:** Security Policy | GRC Documentation
**Concepts:** NIST SP 800-61 | SOC 2 | CCPA | Acceptable Use | Incident Response

Wrote two enterprise security policies aligned to NIST SP 800-61 and SOC 2 - an Acceptable Use Policy and a four-tier Incident Response Policy covering the full IR lifecycle, evidence handling, and CCPA notification timelines.

[View Acceptable Use Policy](Policies/VoltEdge_Acceptable_Use_Policy.pdf) | [View Incident Response Policy](Policies/VoltEdge_Incident_Response_Policy.pdf)

---

## Skills & Tools

- **Security Tools:** Splunk (SPL) - Chronicle (YARA-L) - Wazuh - Suricata - Wireshark - tcpdump - Linux CLI - SQL (MariaDB) - Python - Microsoft Entra ID
- **Security Operations:** Incident Response (NIST SP 800-61) - IDS Rule Tuning - Threat Detection - Vulnerability Assessment - Threat Modeling - CIA Triad - Access Control
- **GRC & Compliance:** NIST CSF - NIST RMF - NIST SP 800-30/800-53 - PCI DSS - GDPR - SOC 2 - HIPAA - Risk Register - Business Impact Analysis - RACI Matrix - Policy Writing
- **Enterprise Systems:** SAP - AIMS - SmartSolve - Microsoft Office (Advanced Excel) - RF Warehouse Systems

---

## Certifications

- Google Cybersecurity Certificate - Coursera, June 2026
- SC-900: Microsoft Security, Compliance & Identity Fundamentals - June 2026
- Lean Six Sigma Yellow Belt - Cardinal Health, 2023
- Prior U.S. Government Security Clearance - U.S. Air Force, 2007-2011

---

## Contact

- **LinkedIn:** [linkedin.com/in/riveramaximilian](https://www.linkedin.com/in/riveramaximilian)
- **Email:** riveramaximilian@gmail.com

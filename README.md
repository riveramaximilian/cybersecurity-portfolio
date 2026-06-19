# Cybersecurity Portfolio

**Maximilian Rivera** | Supply Chain Risk & Compliance | Transitioning to Cybersecurity

---

## About Me

Air Force veteran with 15+ years in supply chain risk management, compliance, and data integrity. Currently completing the **Google Cybersecurity Certificate** (Coursera) to formalize my transition into GRC, risk analysis, and security operations. I bring a compliance-first mindset built in regulated environments - Cardinal Health, federal supply chains, and DoD-adjacent logistics - where data accuracy and access control aren't optional.

Prior U.S. government security clearance. FEMA IS-700 and IS-800 certified. Lean Six Sigma Yellow Belt. Now building hands-on security skills to match the operational background.

---

## Portfolio Projects

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

Analyzed a denial of service attack in which a malicious actor flooded an organization's internal network with ICMP packets through an unconfigured firewall, causing a two-hour outage. Applied all five NIST CSF functions — Identify, Protect, Detect, Respond, and Recover — to document the incident and establish a remediation plan.

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

Audited and corrected file system permissions for a research team on a Linux environment. Used `ls -la` to identify permission mismatches against organizational policy, then applied `chmod` to remove unauthorized write access, secure a hidden archived file, and restrict a directory to its owner only.

**Key Actions:**
- Removed write access for others on project_k.txt (`chmod o-w`)
- Secured hidden file .project_x.txt to read-only for user and group (`chmod u-w,g-w,g+r`)
- Restricted drafts directory to owner only (`chmod g-x`)
- Interpreted and documented 10-character Linux permission strings

[View Report](incident-reports/File_Permissions_in_Linux.pdf)

---

### 4. Apply Filters to SQL Queries
**Type:** Database Investigation & Security Analysis
**Tools:** SQL (MariaDB) | AND, OR, NOT, LIKE operators

Investigated two potential security incidents using SQL filters against an organization's login attempt and employee machine database. Wrote targeted queries to isolate after-hours failed logins, suspicious date-range activity, and logins originating outside of Mexico. Also queried employee tables to identify machines in specific departments and office locations for security update deployment.

**Key Actions:**
- Filtered failed login attempts after 18:00 using AND with a time comparison
- Retrieved login activity across a two-day window using OR on date values
- Excluded Mexican login attempts using NOT with LIKE and the % wildcard
- Isolated Marketing employees in East building offices using AND with pattern matching
- Retrieved Finance and Sales employees using OR across department values
- Identified all non-IT employees using NOT for department-wide exclusion

[View Report](incident-reports/Apply_Filters_to_SQL_Queries.pdf)

---

## Skills & Tools

- **Frameworks:** NIST CSF, NIST RMF, PCI DSS, GDPR, SOC 1/2, HIPAA
- **Concepts:** CIA Triad, Risk Assessment, Access Control, Threat Modeling, Security Auditing, Linux File Permissions
- **Tools (in progress):** Wireshark, Linux CLI, SQL, SIEM basics
- **Background Tools:** SAP, AIMS, SmartSolve, SQL, Excel (Advanced)

---

## Certifications

- Google Cybersecurity Certificate *(in progress - Coursera, 2026)*
- FEMA IS-700: National Incident Management System (June 2026)
- FEMA IS-800: National Response Framework (June 2026)
- Lean Six Sigma Yellow Belt

---

## Contact

- **LinkedIn:** [linkedin.com/in/riveramaximilian](https://www.linkedin.com/in/riveramaximilian)
- **Email:** riveramaximilian@gmail.com

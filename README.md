# GRC & Compliance Portfolio

**Maximilian Rivera** | GRC & Compliance | HIPAA · SOC 2 · ISO 27001 · PCI DSS | Prior U.S. Government Clearance

---

## About Me

I'm a U.S. Air Force veteran with a prior government security clearance and five years running compliance operations in a HIPAA-regulated pharmaceutical supply chain. I've served as compliance owner for QA product hold events: collecting audit evidence, applying quarantine controls, and safeguarding PHI in coordination with regional management.

Outside that day job, I built the GRC portfolio below, covering HIPAA, NIST CSF, ISO 27001, PCI DSS, and SOC 2. It includes a completed third-party vendor risk assessment, a 33-control compliance mapping matrix, and a full HIPAA security risk analysis for an 85,000-patient network.

Google Cybersecurity Certificate, June 2026. Lean Six Sigma Yellow Belt. I'm looking for compliance analyst, GRC analyst, and HIPAA-focused roles where this operational and applied GRC background delivers value from day one.

---

## GRC & Compliance Projects

*Note: these are self-directed projects built on fictional organizations, produced to professional deliverable standards.*

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

### 3. Zero Trust Identity & Access Management Design (Meridian Health Group)

**Type:** Identity & Access Management | Microsoft Entra ID | Zero Trust Architecture
**Frameworks:** NIST SP 800-207 Zero Trust Architecture | HIPAA Security Rule | NIST CSF 2.0 | CIS Controls v8

Designed a full identity and access management architecture for a healthcare organization on Microsoft Entra ID, applying least privilege and Zero Trust so the right people have access to the right things and nobody has more than they need.

Specified 10 user accounts across 6 departments, organized into 10 security groups with roles assigned on least privilege. Defined MFA for all users, 7 conditional access policies, and a full Joiners-Movers-Leavers workflow so the organization always knows who has access and why.

**Key Actions:**
- Designed 10 user accounts (employees, service accounts, external vendor) with RBAC and least privilege on every role
- Defined 10 security groups to target authentication policies and Microsoft 365 permissions
- Specified 7 Conditional Access policies: MFA for all users, blocking outdated login methods, geo-restricting access, requiring compliant devices for admin accounts, and restricting vendor access
- Modeled a Joiners-Movers-Leavers workflow: accounts enabled within 24 hours of hire, disabled within 4 hours of termination
- Defined two quarterly access review cycles covering every role assignment, with documented decisions and removal of unneeded access
- Documented 6 security findings with risk ratings and a prioritized fix plan aligned to HIPAA and NIST

[View IAM Design Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/zero-trust-iam-lab/MHG_ZeroTrust_IAM_Lab_Report.pdf) | [View RBAC Matrix](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/zero-trust-iam-lab/MHG_RBAC_Matrix_ZeroTrust_IAM.xlsx)

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
- 4-phase remediation roadmap over 365 days, itemized by line item to roughly $303,500 (detailed in the workbook)
- Executive summary mapped against the HHS HIPAA Security Rule NPRM

[View SRA Workbook](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/hipaa-security-risk-analysis/SunRidge_HIPAA_SRA_2025.xlsx) | [View Executive Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/hipaa-security-risk-analysis/SunRidge_HIPAA_SRA_Executive_Report_2025.pdf)

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

### 6. SOC 2 Readiness Assessment (Crestline Technology Partners)

**Type:** GRC | Audit Readiness
**Frameworks:** SOC 2 Type II | Trust Services Criteria (CC6, CC7, CC9)

Ran a SOC 2 readiness assessment ahead of a Type II audit for a mid-size technology firm. Evaluated 22 controls across logical access (CC6), system operations (CC7), and risk mitigation (CC9).

**Key Findings:**
- Identified 14 control gaps across the three trust services categories evaluated
- Issued a formal management letter documenting each gap and its associated risk
- Built a 12-month phased remediation roadmap to close gaps ahead of the audit window

[View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/soc2-readiness-assessment/SOC2-Readiness-Assessment-Crestline-Technology-Partners.pdf)

---

## Certificate Coursework (Google Cybersecurity Certificate)

Foundational labs from the Google Cybersecurity Certificate, included as supporting technical background rather than GRC projects.

- **Vulnerability Assessment (NIST SP 800-30):** attack-surface identification, likelihood and impact scoring, and prioritized remediation. [View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/google-cert-labs/Vulnerability_Assessment_Report.pdf)
- **Incident Report, DoS via ICMP Flood (NIST CSF):** applied all five CSF functions to document and remediate a denial-of-service outage. [View Report](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/google-cert-labs/NIST_CSF_Portfolio_Report.pdf)
- **Security fundamentals (SQL, Linux, Python):** SQL investigation queries, Linux file-permission hardening, and a Python allow-list automation script. [SQL](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/google-cert-labs/Apply_Filters_to_SQL_Queries.pdf) · [Linux](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/google-cert-labs/File_Permissions_in_Linux.pdf) · [Python](https://github.com/riveramaximilian/cybersecurity-portfolio/blob/main/google-cert-labs/Algorithm_for_File_Updates_in_Python.pdf)

---

## Skills & Tools

- **GRC & Compliance:** HIPAA Security Rule · NIST CSF · NIST RMF · NIST SP 800-30/800-53/800-207 · ISO 27001:2022 · PCI DSS · SOC 2 Type II · Vendor Risk Assessment · Compliance Mapping · Risk Register · Policy Writing · Audit Readiness
- **Security & Access Governance:** Identity & Access Management (IAM) · Zero Trust Architecture · RBAC · Access Reviews · Microsoft Entra ID · Vulnerability Assessment · Threat Modeling
- **Additional Technical:** Incident Response (NIST SP 800-61) · SQL (MariaDB) · Python · Linux CLI
- **Enterprise Systems:** SAP · AIMS · SmartSolve · Microsoft Office (Advanced Excel)

---

## Certifications

- Google Cybersecurity Certificate, Coursera, June 2026
- SC-900: Microsoft Security, Compliance & Identity Fundamentals, June 2026
- Lean Six Sigma Yellow Belt, Cardinal Health, 2023
- Prior U.S. Government Security Clearance, U.S. Air Force, 2007 to 2011

---

## Contact

- **Location:** Wildwood, Florida. Open to remote work.
- **LinkedIn:** [linkedin.com/in/maximilianrivera](https://www.linkedin.com/in/maximilianrivera)
- **Email:** riveramaximilian@gmail.com

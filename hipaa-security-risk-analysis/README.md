# HIPAA Security Risk Analysis — SunRidge Health Partners

**GRC Portfolio Project | Maximilian Rivera**  
[![HIPAA](https://img.shields.io/badge/HIPAA-45%20CFR%20164-blue)](https://www.hhs.gov/hipaa)
[![NIST SP 800-30](https://img.shields.io/badge/NIST-SP%20800--30%20Rev.1-navy)](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final)
[![NIST CSF 2.0](https://img.shields.io/badge/NIST%20CSF-2.0-green)](https://www.nist.gov/cyberframework)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()

---

## Overview

A comprehensive, enterprise-grade HIPAA Security Risk Analysis (SRA) conducted for **SunRidge Health Partners** — a fictional integrated health network serving ~85,000 patients across Central Florida's retirement corridor (Ocala, Marion County).

This project demonstrates end-to-end GRC analyst competency: identifying ePHI systems, characterizing threats, assessing likelihood and impact, scoring risks, mapping HIPAA controls, and producing a prioritized remediation roadmap — grounded in real-world healthcare cybersecurity events from 2024–2025.

**Deliverables:**
- `SunRidge_HIPAA_SRA_2025.xlsx` — 7-tab Excel workbook (risk register, ePHI inventory, control gap assessment, remediation roadmap)
- `SunRidge_HIPAA_SRA_Executive_Report_2025.docx` — Professional executive report for leadership and board presentation

---

## About the Fictional Organization

| Field | Detail |
|-------|--------|
| **Organization** | SunRidge Health Partners, Inc. |
| **Type** | Covered Entity — Integrated Health Network |
| **Location** | Ocala, Florida (Marion, Sumter, Lake, Citrus Counties) |
| **Patients** | ~85,000 active — 68% Medicare / Medicare Advantage |
| **Workforce** | ~1,400 employees and contractors |
| **Facilities** | Ocala Regional Medical Center (287-bed acute care) + 3 outpatient/behavioral health facilities |
| **Primary EHR** | Epic Systems (cloud-hosted) |
| **Supporting Systems** | LabCore HL7 v2 (legacy, EOL) · MedBridge Clearinghouse · MyChart Portal · Teladoc Telehealth |
| **Business Associates** | 14 active BAs |

---

## Regulatory Framework

| Standard | Scope |
|----------|-------|
| **45 CFR Part 164** | HIPAA Security Rule — primary compliance mandate |
| **NIST SP 800-30 Rev. 1** | Risk assessment methodology (Likelihood x Impact) |
| **NIST CSF 2.0** | Cybersecurity framework alignment |
| **NIST SP 800-53** | Security control reference |
| **HHS SRA Tool Guidance (2014)** | Implementation guidance for 164.308(a)(1) |
| **HHS HIPAA Security Rule NPRM (Dec 2024)** | Proposed rule changes — first update since 2013 |

---

## SRA Findings Summary

| Risk Level | Count | Score Range |
|-----------|-------|-------------|
| CRITICAL | 3 | 20-25 |
| HIGH | 4 | 15-19 |
| MEDIUM | 3 | 8-14 |
| LOW | 0 | 1-7 |
| **Total** | **10** | |

### Top 3 Critical Risks

**R-01 — Ransomware via Spear-Phishing (Score: 25)**  
Healthcare is the #1 ransomware target globally (17% of all attacks, 458 events in 2024). SunRidge's posture — no DMARC/DKIM, annual-only training, no phishing simulation — mirrors conditions enabling the Ascension Health attack (May 2024, 5.6M patients, 140 hospitals on paper protocols).

**R-02 — Third-Party Clearinghouse BA Compromise (Score: 20)**  
Single-vendor billing dependency, BAA not reviewed since 2021, no BCP for disruption. Modeled after Change Healthcare ransomware (Feb 2024) — 192.7M records, largest healthcare breach in US history.

**R-09 — Web Tracking Pixel PHI Disclosure (Score: 15 — Active Violation)**  
Google Analytics and Meta Pixel active on patient scheduling pages — ongoing HIPAA Privacy Rule violation per HHS OCR Dec 2022 bulletin. Modeled after Kaiser Permanente's 2024 disclosure (13.4M patients, advertising platforms received PHI).

---

## Real-World Context

| Event | Date | Impact | Relevance |
|-------|------|--------|-----------|
| Change Healthcare Ransomware | Feb 2024 | 192.7M records — largest healthcare breach in US history | R-02: Clearinghouse BA risk |
| Ascension Health Ransomware | May 2024 | 5.6M patients, 140 hospitals disrupted via phishing | R-01: Ransomware threat vector |
| Florida Dept. of Health (RansomHub) | Jun 2024 | 729,699 FL residents, 100GB data leaked | Regional threat awareness |
| Kaiser Permanente Tracking Pixels | 2024 | 13.4M patients — PHI sent to ad platforms | R-09: Active violation discovered |
| Retina Group of Florida | Nov 2024 | 153,000 patients — unauthorized endpoint access | R-03: Unencrypted device risk |
| HHS HIPAA Security Rule NPRM | Dec 27, 2024 | First Security Rule update since 2013 | All risks — NPRM gap analysis |

---

## Workbook Structure (7 Tabs)

| Tab | Contents |
|-----|----------|
| **Dashboard** | 5x5 risk heat map, KPI summary (CRITICAL/HIGH/MEDIUM counts), top findings, regulatory context |
| **Organization Profile** | Entity info, facility details, SRA scope and methodology statement |
| **ePHI Inventory** | 7 systems: medium, data flow, ePHI elements, vendor, BA status, risk rating |
| **Threat Library** | 12 threat scenarios: NIST categories, threat sources, descriptions, likelihood base |
| **Risk Register** | 10 risks: full narrative, L x I scoring, HIPAA CFR citations, NPRM gap, recommended controls, cost, owner |
| **Control Gap Assessment** | 30 HIPAA Security Rule controls rated: COMPLIANT / PARTIAL / GAP / IN PROGRESS |
| **Remediation Roadmap** | 20 action items across 4 phases, 365-day timeline, ~$303,500 total investment estimate |

---

## HIPAA Control Gap Summary

30 controls assessed across Administrative, Physical, and Technical Safeguard categories:

- **COMPLIANT: 1** (3%) — Workstation Use Policy (164.310(b))
- **PARTIAL: 14** (47%) — Controls exist with identified enforcement or scope gaps
- **GAP: 14** (47%) — No adequate control in place
- **IN PROGRESS: 1** (3%) — Risk Analysis (this SRA, 164.308(a)(1))

Critical gaps: Encryption at rest/in transit · MFA / Person Authentication · Disaster Recovery Plan · Automated account de-provisioning · Audit log review · TPRM program

---

## Remediation Roadmap

| Phase | Timeline | Investment | Focus Areas |
|-------|----------|-----------|-------------|
| Phase 1: Immediate | 0-30 Days | ~$36,000 | Remove tracking pixels, isolate EOL lab server, enable MFA, emergency BA review |
| Phase 2: Short-Term | 31-90 Days | ~$84,000 | Email security (DMARC/DKIM), telehealth audit, auto-deprovision, update all BAAs |
| Phase 3: Mid-Term | 91-180 Days | ~$86,000 | MDM deployment, formal TPRM program, portal MFA, BCP/DRP with tabletop |
| Phase 4: Strategic | 181-365 Days | ~$95,000 | External pen test, network segmentation, SIEM, NPRM final rule readiness |
| **Total** | **365 Days** | **~$303,500** | |

OCR civil monetary penalties: up to $1.9M per violation category per year if unaddressed.

---

## Skills Demonstrated

- HIPAA Security Rule (45 CFR Part 164) — Administrative, Physical, and Technical Safeguards
- NIST SP 800-30 Rev. 1 — Threat identification, likelihood/impact determination, risk scoring
- NIST CSF 2.0 and NIST SP 800-53 — Framework alignment and control mapping
- PHI / ePHI system inventory and characterization
- Business Associate risk management and TPRM
- Control gap analysis (30 HIPAA Security Rule controls)
- Risk register development with full threat narratives
- Remediation roadmap: phased prioritization, cost estimation, ownership assignment
- Real-world threat landscape research and OCR enforcement context
- HHS HIPAA Security Rule NPRM (December 2024) — compliance gap analysis and future-state readiness

---

## Repository Structure

```
hipaa-security-risk-analysis/
├── README.md
├── SunRidge_HIPAA_SRA_2025.xlsx                    <- Main SRA workbook (7 tabs)
└── SunRidge_HIPAA_SRA_Executive_Report_2025.pdf   <- Executive report
```

---

## About

**Maximilian Rivera** — GRC & Compliance Analyst  
Google Cybersecurity Certificate · SC-900: Microsoft Security, Compliance & Identity Fundamentals · FEMA IS-700/800 · Lean Six Sigma Yellow Belt · Prior U.S. Government Security Clearance (U.S. Air Force)

[LinkedIn](https://linkedin.com/in/maximilianrivera) · [GitHub Portfolio](https://github.com/riveramaximilian/cybersecurity-portfolio)

---

*This is a fictional scenario created for portfolio purposes. SunRidge Health Partners does not exist. All patient data, facility details, and incident information are fabricated for demonstration.*

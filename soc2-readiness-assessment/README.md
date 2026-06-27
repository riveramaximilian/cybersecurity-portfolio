# SOC 2 Type II Readiness Assessment — Crestline Technology Partners

This SOC 2 Type II readiness assessment was completed as an independent portfolio project to demonstrate applied GRC skills outside of a professional engagement. The assessment evaluates 22 controls across CC6, CC7, and CC9 of the AICPA Trust Services Criteria for a simulated B2B SaaS company preparing for its first audit. Built using AICPA TSC 2017 with 2022 points of focus, NIST CSF 2.0 alignment, and formatted to mirror real client-facing GRC deliverables.

## What’s Inside

**`SOC2-Readiness-Assessment-Crestline-Technology-Partners.pdf`** — Full assessment document including:

- **Executive Summary** — Written for a non-technical CEO/CFO audience: what SOC 2 is, what was found, and what the stakes are
- **Control Assessment Table** — 22 controls across CC6 (Logical Access), CC7 (System Operations), and CC9 (Risk Mitigation), each with current state, gap rating, risk rating, and specific remediation guidance with named owners
- **Findings Summary** — Consolidated gap list sorted by severity with narrative deep-dives on Critical findings
- **Management Letter** — Formal readiness opinion addressed to company leadership: scope, methodology, finding counts by severity, and a conditional path to audit readiness
- **12-Month Remediation Roadmap** — Three-phase plan: critical gap closure (Days 1-90), program infrastructure build (Days 91-180), and evidence generation for the Type II observation period (Days 181-365)

## Scenario

**Crestline Technology Partners** — Simulated mid-size B2B SaaS platform (~120 employees) managing HR workflows and payroll data for small business clients. Four years operating, fast growth, first enterprise client requiring SOC 2 Type II, no formal security program, part-time IT manager. A realistic and common profile for companies at this compliance inflection point.

## Key Findings

| Severity | Finding |
|----------|---------|
| Critical | Orphaned accounts — 7 former employee accounts still active, including one with DB admin access 18 months post-departure |
| Critical | No MFA on privileged accounts — production database accessed with username/password only |
| Critical | No formal access termination process — no offboarding checklist, no deprovisioning workflow |
| High | No incident response plan — no escalation path, defined roles, or breach notification procedure |
| High | Informal change management — direct-to-production deployments, no change tickets or rollback docs |
| High | Vendor contracts missing security terms — 6 vendors touching client payroll data, none with DPAs |
| Medium | No BCP/DRP — no recovery procedures, no tested RTO/RPO targets |

**Overall readiness opinion: NOT READY for SOC 2 Type II audit engagement.**

## Framework References

- AICPA Trust Services Criteria 2017 (CC6, CC7, CC9) with 2022 Points of Focus
- NIST Cybersecurity Framework 2.0 (alignment context)
- Formatted to mirror real client-facing GRC deliverables

## Portfolio Series

1. **HIPAA Security Risk Analysis** — SunRidge Health Partners
2. **Healthcare Vendor Risk Assessment** — ClearPath Health
3. **SOC 2 Type II Readiness Assessment** — Crestline Technology Partners ← this project

# 06 — Gap Assessment

Each finding, the evidence, the specific rule it implicates, and severity. I map to the HIPAA rule and the OCR guidance rather than hand-waving at "HIPAA" in general, because that specificity is what makes a finding defensible and actionable.

---

### F-01 — Meta Pixel discloses behavioral-health booking + email to Meta — **Critical**

- **Evidence:** Pixel fires on `/booking/*/confirm`; outbound request to `facebook.com/tr` includes hashed email and event context identifying the service line.
- **Rule:** HIPAA Privacy Rule, 45 CFR 164.502 — impermissible disclosure of PHI without authorization or a permitted basis. Meta offers no BAA (164.502(e)).
- **Also:** OCR Dec 2022 Bulletin explicitly names this scenario. FTC Act unfairness (cf. BetterHelp).
- **Status:** Open. Requires same-day containment.

### F-02 — GA4 ingests PHI (service-line URL + IP + client ID) with no BAA — **Critical**

- **Evidence:** All-page GA4 tag; `g/collect` payload carries full URL path containing condition/service, client ID, and IP.
- **Rule:** 45 CFR 164.502; 164.514 (IP + health context is not de-identified). No BAA with Google for this data.
- **Status:** Open.

### F-03 — TikTok Pixel on prescription-refill confirmation — **Critical**

- **Evidence:** TikTok pixel present on `/refills/confirm`; sends page-load event with IP/device signals in a PHI context.
- **Rule:** 45 CFR 164.502; no BAA available from TikTok.
- **Status:** Open.

### F-04 — Session replay captures intake questionnaire keystrokes — **High**

- **Evidence:** Hotjar recording active on intake form; input masking disabled; captures symptom/screener entries pre-submit.
- **Rule:** 45 CFR 164.502 (disclosure to Hotjar, no BAA); 164.312 (Security Rule, unauthorized data capture).
- **Status:** Open.

### F-05 — No consent gate before non-essential tags fire — **Medium**

- **Evidence:** All tags load on page load with no opt-in; no consent-management platform.
- **Rule:** Supports F-01–F-04; also FTC expectations and state privacy laws (e.g., broad consumer-health-data rules). Best-practice control gap.
- **Status:** Open.

### F-06 — Subprocessors receive data without confirmed BAAs — **Medium**

- **Evidence:** HubSpot and Intercom receive identifiers/content; BAA status unconfirmed in vendor records.
- **Rule:** 45 CFR 164.502(e), 164.308(b) — business associate contracts required.
- **Status:** Open. Confirm or execute; terminate flow if not obtainable.

### F-07 — No maintained data map / RoPA and no defined retention — **Medium**

- **Evidence:** No processing register existed before this assessment; PA-08 and PA-10 retention undefined.
- **Rule:** 45 CFR 164.316 (documentation), 164.530(j); Security Rule risk-analysis expectation (164.308(a)(1)).
- **Status:** Open. This is the root-cause finding.

---

## Summary

| Severity | Count | Findings |
|---|---|---|
| Critical | 3 | F-01, F-02, F-03 |
| High | 1 | F-04 |
| Medium | 3 | F-05, F-06, F-07 |

The three Criticals share one fix pattern (stop sending PHI to vendors with no BAA), and the Mediums are the governance that keeps them fixed. That shapes the roadmap.

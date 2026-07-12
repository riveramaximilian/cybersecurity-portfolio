# PHI Data-Flow & Third-Party Tracking Privacy Assessment

**A hands-on privacy assessment of a (fictional) direct-to-consumer telehealth provider, focused on where protected health information (PHI) leaks to third-party tracking technologies, and how to stop it.**

> This is a self-directed portfolio project. "NorthBay TeleHealth" is a fictional company I built to model a real and well-documented problem: telehealth and hospital websites disclosing PHI to advertising and analytics vendors through tracking pixels. No real patient data was used. The scenario, findings, and remediation plan are my own work.

---

## Why I built this

In December 2022, HHS Office for Civil Rights (OCR) put out a bulletin warning that tracking technologies (Meta Pixel, Google Analytics, and similar) on the pages of HIPAA-regulated entities can cause impermissible disclosures of PHI. In July 2023, OCR and the FTC sent a joint warning letter to roughly 130 hospital systems and telehealth providers. Around the same window, the FTC took enforcement action against GoodRx, BetterHelp, and Premom for disclosing consumers' health information to ad platforms.

The through-line in every one of those cases is the same: **the organization did not have an accurate picture of where its data was going.** You cannot protect data you have not mapped. So I did the mapping exercise end to end, the way I would run it on a real engagement, and documented the findings and the fix.

## What's in this repo

| Document | What it is |
|---|---|
| [`01-scope-and-methodology.md`](01-scope-and-methodology.md) | Scope, assumptions, and how I actually looked for trackers |
| [`02-data-inventory.md`](02-data-inventory.md) | Every system and data element in scope, with PHI classification |
| [`03-data-flow-map.md`](03-data-flow-map.md) | Where data moves, including the third-party flows (diagram) |
| [`04-tracker-audit.md`](04-tracker-audit.md) | Every third-party tag found, what it captured, and the risk |
| [`05-ropa.md`](05-ropa.md) | Records of Processing Activities (the master processing register) |
| [`06-gap-assessment.md`](06-gap-assessment.md) | Findings mapped to HIPAA rules and OCR guidance, with severity |
| [`07-remediation-roadmap.md`](07-remediation-roadmap.md) | Phased fix, from same-day containment to governance |
| [`08-consent-and-authorization-workflow.md`](08-consent-and-authorization-workflow.md) | The consent flow I'd put in front of any non-essential tracker |

## The headline findings

I found seven issues. Three I rated Critical, because they involve PHI leaving the organization to a vendor with no BAA, no patient authorization, and no permissible-use basis under the Privacy Rule:

- **F-01 (Critical):** The Meta Pixel was firing on the appointment-booking flow and capturing the appointment type (including behavioral-health visits) alongside a hashed email. That combination is an impermissible disclosure of PHI to Meta. This is almost exactly what the FTC alleged against BetterHelp.
- **F-02 (Critical):** Google Analytics 4 was collecting full page URLs that contained the service/condition in the path, tied to a client ID and IP address. In this context the IP is an identifier, so those flows are PHI going to Google with no BAA.
- **F-03 (Critical):** A TikTok pixel was live on the prescription-refill confirmation page.

The other four (session-replay capturing intake questionnaire keystrokes, no consent gate before non-essential tags fire, subprocessors receiving data without executed BAAs, and no defined retention or maintained data map) are documented in the [gap assessment](06-gap-assessment.md).

## How I approached the fix

I did not lead with "rip out all analytics," because that is how you get compliance ignored by the business. I split the remediation into three moves: **contain the active leaks the same day** (kill the pixels on authenticated and PHI-adjacent pages, disable session replay on forms), **put controls in within 30 days** (a consent-management gate, BAAs executed or vendors terminated, GA4 reconfigured to stop ingesting PHI), and **build the governance so it does not happen again within 90 days** (a maintained data map and RoPA, a vendor/BAA register, and a privacy review gate in the release process). Details and rationale are in the [remediation roadmap](07-remediation-roadmap.md).

One thing I flagged that is easy to miss: the disclosures that already happened may be reportable. I recommended a Breach Notification Rule risk assessment (the four-factor analysis) on the historical pixel data, rather than assuming it was fine because it was "just analytics."

## Frameworks and references I mapped against

- HIPAA Privacy, Security, and Breach Notification Rules (45 CFR Parts 160 and 164)
- HHS OCR Bulletin, *Use of Online Tracking Technologies by HIPAA Covered Entities and Business Associates* (Dec 2022, updated 2024)
- FTC–HHS joint warning letter to hospital systems and telehealth providers (July 2023)
- FTC Health Breach Notification Rule (for the non-HIPAA data paths)
- NIST Privacy Framework (as the control-organizing structure)

## What I'd do differently with more time

If this were a live engagement I would want to validate the tag behavior across more of the user journey (not just the pages I sampled), pull the actual data-processing agreements to confirm BAA status rather than inferring it, and sit with engineering to understand why the tags were deployed the way they were. Most tracking-pixel problems are not malicious. They come from a marketing team adding a tag through a tag manager without anyone asking whether the page it lands on touches PHI. The durable fix is the review gate, not a one-time cleanup.

---

*Maximilian Rivera — Compliance / Privacy Analyst, USAF Veteran. Feedback welcome.*

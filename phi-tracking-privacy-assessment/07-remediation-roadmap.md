# 07 — Remediation Roadmap

I sequenced this by risk, not by convenience. Stop the bleeding first, put controls in second, build the governance third. I also wrote it so the business can still function. "Delete all analytics" gets ignored. "Stop sending PHI to vendors you have no agreement with, here's how to keep the analytics you're allowed to have" gets done.

## Phase 0 — Containment (0–7 days)

| Action | Finding | Owner |
|---|---|---|
| Remove Meta Pixel and TikTok Pixel from all authenticated and PHI-adjacent pages | F-01, F-03 | Web eng + Marketing |
| Disable Hotjar on all form and portal pages; enable input masking everywhere else | F-04 | Web eng |
| Strip service-line/condition identifiers out of URL paths that GA4 reads | F-02 | Web eng |
| Freeze new tag deployments until the review gate exists | F-07 | Privacy |

Phase 0 is the difference between "we found a problem and acted" and "we knew and let it keep happening." That distinction matters a lot if this ever becomes an OCR conversation.

## Phase 1 — Controls (8–30 days)

| Action | Finding | Owner |
|---|---|---|
| Deploy a consent-management platform; block all non-essential tags until opt-in | F-05 | Privacy + Web eng |
| Inventory every vendor receiving data; execute BAAs or terminate the data flow (HubSpot, Intercom) | F-06 | Privacy + Legal |
| Reconfigure GA4: confirm data-processing terms, remove PHI from ingested fields, set IP handling | F-02 | Analytics |
| Move remaining analytics to server-side tagging so NorthBay controls what is sent | F-02 | Web eng |
| Set and document retention for all analytics/marketing data | F-07 | Privacy |

## Phase 2 — Governance (31–90 days)

| Action | Finding | Owner |
|---|---|---|
| Stand up and maintain the data map and RoPA as living documents | F-07 | Privacy |
| Build a vendor/BAA register with renewal tracking | F-06 | Privacy |
| Add a **privacy review gate** to the release process: no tag or vendor goes live without a RoPA entry and a PHI check | F-07 | Privacy + Eng leadership |
| Train marketing and engineering on why a tag on a health page is a disclosure | all | Privacy |
| Run a DPIA on any new tracking or ad initiative | F-05 | Privacy |

## The part people skip: the historical breach analysis

The pixels were live before I found them, which means PHI was already disclosed. That is potentially a reportable breach. Before closing this out I would run the Breach Notification Rule four-factor risk assessment (45 CFR 164.402) on the historical disclosures:

1. Nature and extent of the PHI involved (behavioral-health service line + identifiers = sensitive).
2. Who received it (Meta, Google, TikTok).
3. Whether it was actually acquired or viewed (ad platforms ingest and use it).
4. The extent to which risk has been mitigated (no BAA, no ability to claw it back).

My read is that this would likely not qualify for the low-probability-of-compromise exception, which points toward notification obligations. I would not make that call alone; it goes to Legal and the Privacy Officer. But flagging it is the job. Quietly fixing the tags and pretending the prior disclosures didn't happen is how a fixable problem becomes an enforcement action.

## Definition of done

- Zero PHI flowing to any vendor without a BAA and a permissible basis.
- Consent gate live; RoPA maintained; review gate enforced on releases.
- Historical breach assessment documented and decisioned.

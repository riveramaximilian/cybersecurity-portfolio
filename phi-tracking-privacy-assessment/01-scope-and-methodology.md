# 01 — Scope & Methodology

## The scenario

NorthBay TeleHealth is a fictional direct-to-consumer telehealth provider offering behavioral health and primary care over a website and iOS/Android apps. Roughly 120,000 active patients. As a covered entity under HIPAA, everything it does with patient information falls under the Privacy, Security, and Breach Notification Rules.

I scoped this assessment to the question that actually gets organizations in trouble: **what patient data is leaving NorthBay through third-party tags on its web and mobile properties, and is any of it PHI?**

## In scope

- Public marketing site (northbaytelehealth.example)
- Authenticated patient portal (booking, intake questionnaires, prescription refills, billing)
- Third-party tags, pixels, SDKs, and analytics running on the above
- The vendors those tags send data to, and whether a Business Associate Agreement (BAA) exists

## Out of scope (and why)

- The EHR and clinical systems themselves. Important, but a different assessment. Here I'm following the data *outbound* to third parties, which is the tracking-pixel exposure.
- Infrastructure security (encryption at rest, network controls). Noted where relevant but not the focus.
- A full DPIA. I flag where one is warranted.

## Assumptions

- NorthBay has not previously maintained a data map or a Records of Processing Activities register. (This is the common reality, and it's the root cause.)
- Marketing owns the tag manager and has been adding tags without a privacy review.
- BAA status is inferred from vendor type and standard contracting for this exercise. On a real engagement I would confirm against the signed agreements.

## How I actually looked for trackers

This is the part that matters, because "we assessed our tracking technologies" means nothing without a method. What I would do, and modeled here:

1. **Load each page with the browser DevTools Network tab open**, filtered to third-party domains, and watch what fires. The requests to `facebook.com/tr`, `google-analytics.com/g/collect`, `analytics.tiktok.com`, and similar are the disclosures. You read the query string and payload to see exactly what field is being shipped.
2. **Run an automated scan** (The Markup's *Blacklight* is the go-to free one) to catch trackers, session-replay scripts, and key-logging behavior I might miss by hand.
3. **Use a tag inspector** (Google Tag Assistant, and reviewing the Google Tag Manager container) to enumerate every configured tag and its firing trigger, so I'm not relying only on the pages I happened to click.
4. **Map firing triggers to page sensitivity.** A pixel on the homepage is one risk. The same pixel on `/booking/behavioral-health/confirm` is a different universe of risk. The trigger conditions are where the PHI exposure lives.
5. **Trace each destination to a vendor and a contract**, then check BAA status and whether the Privacy Rule permits that disclosure at all.

## How I rated severity

| Severity | Meaning |
|---|---|
| **Critical** | PHI disclosed to a third party with no BAA and no permissible basis. Reportable-breach candidate. |
| **High** | Sensitive data exposure or a control failure that materially raises breach likelihood. |
| **Medium** | Governance or configuration gap that should be fixed but isn't actively leaking PHI right now. |
| **Low** | Hygiene and documentation issues. |

The severity is driven by three questions: is it PHI, is there a permissible basis or BAA, and how sensitive is the underlying service (behavioral health raises everything a notch).

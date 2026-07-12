# 05 — Records of Processing Activities (RoPA)

A RoPA is the master register of "what processing are we doing, why, with what data, and who touches it." HIPAA doesn't name it "RoPA" (that language comes from GDPR Art. 30), but the underlying discipline is exactly what OCR expects you to be able to produce: an accurate accounting of your PHI processing and disclosures. I built this as the artifact NorthBay was missing, and its absence is the root cause of everything else.

| PA-ID | Processing activity | Data categories | Purpose | Permissible basis (HIPAA) | Recipients / vendors | BAA | Retention | Risk |
|---|---|---|---|---|---|---|---|---|
| PA-01 | Patient registration | D-01, D-02, D-03 | Create account, treatment | Treatment (permitted) | Internal, AWS | Yes | Life of record + legal hold | Low |
| PA-02 | Appointment booking | D-06, D-01 | Schedule care | Treatment | Internal, AWS | Yes | Life of record | Low |
| PA-03 | Intake questionnaire | D-07 | Clinical intake | Treatment | Internal, AWS | Yes | Life of record | Low (first party) / **Very High** via PA-09 |
| PA-04 | Prescription refills | D-08 | Treatment | Treatment | Internal, pharmacy | Yes | Per record rules | Low |
| PA-05 | Billing & payment | D-09, D-10 | Payment | Payment (permitted) | Stripe | N/A (PCI) | Per record rules | Low |
| PA-06 | Email marketing | D-01, D-02 | Marketing | Requires authorization / opt-in | HubSpot | **Unconfirmed** | Until opt-out | Medium |
| PA-07 | Support chat | D-01, D-02, content | Customer service | Operations | Intercom | **Unconfirmed** | Review | Medium |
| PA-08 | Web analytics | D-04, D-11, D-02 | Measure site usage | **No permissible basis as configured** | GA4, Google Ads | **None** | Undefined | **Critical** |
| PA-09 | Advertising pixels | D-02, D-04, D-06, D-08 | Ad targeting/measurement | **No permissible basis; no BAA available** | Meta, TikTok | **None** | Vendor-controlled | **Critical** |
| PA-10 | Session replay | D-07, D-12 | UX improvement | **No permissible basis as configured** | Hotjar | **None** | Undefined | **High** |

## What the register tells you at a glance

The first five rows (treatment, payment) are clean. They have a permissible basis under the Privacy Rule and BAAs where needed. The bottom three rows (PA-08, PA-09, PA-10) are where the organization is operating with **no lawful basis for the disclosure and no contract governing it.** That is the exact profile OCR and the FTC have been enforcing against.

Two of these (retention "Undefined" on PA-08 and PA-10) also fail a basic Security Rule expectation: you can't protect or dispose of data on a schedule you never set.

Keeping this register current is NorthBay's single highest-leverage control. If marketing had to add a row here before adding a tag, none of the Critical findings would exist.

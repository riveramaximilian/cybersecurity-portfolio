# 02 — Data Inventory

Before you can map flows, you need to know what data exists and which of it is PHI. PHI is not just the obvious medical fields. Under HIPAA, health information tied to an identifier is PHI, and in the online context an IP address or device ID can be the identifier. That nuance is what trips up most analytics setups.

## Data elements in scope

| ID | Data element | Where it's collected | PHI? | Sensitivity | Notes |
|---|---|---|---|---|---|
| D-01 | Full name | Registration, booking | Yes | High | Direct identifier |
| D-02 | Email address | Registration, marketing signup | Yes (in context) | High | Often hashed and sent to ad platforms — still PHI when tied to a health service |
| D-03 | Date of birth | Registration | Yes | High | Direct identifier |
| D-04 | IP address | Every page load | Yes (in context) | Medium-High | The key one people miss. Tied to a health visit, it's PHI |
| D-05 | Device ID / advertising ID | Mobile app | Yes (in context) | Medium-High | Same logic as IP for the apps |
| D-06 | Appointment type / service line | Booking flow | Yes | **Very High** | "Behavioral health" is the sensitive part |
| D-07 | Intake questionnaire responses | Intake form | Yes | **Very High** | Symptoms, mental-health screeners (e.g., PHQ-9 style) |
| D-08 | Prescription / refill data | Refill flow | Yes | Very High | |
| D-09 | Insurance member ID | Billing | Yes | High | |
| D-10 | Payment card data | Checkout | No (PCI, not PHI) | High | Handled by Stripe; flagged for scope separation |
| D-11 | Page-path / URL | Every page load | Yes (in context) | High | URLs like `/behavioral-health/anxiety` reveal condition |
| D-12 | Session-replay recording | Portal pages | Yes | Very High | Can capture D-06, D-07 keystrokes before submit |

## Systems and vendors in scope

| System / vendor | Role | Data it touches | BAA expected? | BAA status (inferred) |
|---|---|---|---|---|
| Patient portal (internal) | Core app | All PHI | N/A (first party) | — |
| AWS | Hosting | All PHI at rest | Yes | In place |
| Stripe | Payments | D-10 | No (not PHI) | N/A |
| Google Analytics 4 | Web analytics | D-02, D-04, D-11 | **Yes if PHI** | **None** |
| Meta Pixel | Advertising | D-02, D-04, D-06 | Not offered by Meta | **None** |
| TikTok Pixel | Advertising | D-04, D-08 (via page) | Not offered | **None** |
| Google Ads | Advertising | D-04, D-11 | Not offered | **None** |
| Hotjar (session replay) | UX analytics | D-07, D-12 | Yes if PHI | **None** |
| HubSpot | CRM / email | D-01, D-02 | Yes | **Unconfirmed** |
| Intercom | Support chat | D-01, D-02, chat content | Yes | **Unconfirmed** |

The pattern is already visible in this table: the advertising and analytics vendors are receiving PHI, and none of them are under a BAA. Meta and TikTok don't even offer BAAs, which means there is **no lawful way** to send them PHI. That's not a configuration problem you can fix with a setting. The data simply cannot go there.

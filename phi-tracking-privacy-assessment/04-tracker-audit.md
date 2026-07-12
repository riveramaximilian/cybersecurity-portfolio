# 04 — Third-Party Tracker Audit

This is the evidence table. For each tag I recorded where it fired, what data I observed going out, where it went, whether a BAA exists, and the call.

| Tag | Fires on | Data observed leaving | Destination | BAA | Risk | Recommendation |
|---|---|---|---|---|---|---|
| Meta Pixel | Homepage, booking flow, **behavioral-health confirmation** | Hashed email, event = appointment booked, service line via context | Meta | None (not offered) | **Critical** | Remove from all authenticated and PHI-adjacent pages immediately |
| Google Analytics 4 | All pages | Full page URL (contains service line), GA client ID, IP | Google | None | **Critical** | Remove PHI from URLs; no PHI to GA4 without BAA; consider server-side + IP anonymization only after PHI is stripped |
| TikTok Pixel | Marketing pages, **refill confirmation** | Page load, IP, device signals | TikTok | None (not offered) | **Critical** | Remove from portal entirely |
| Google Ads remarketing | Marketing + some portal pages | Page URL, IP | Google | None | **High** | Restrict to non-PHI marketing pages only |
| Hotjar session replay | Portal, **intake questionnaire** | Keystrokes in intake form incl. symptoms before submit | Hotjar | None | **High** | Disable on all form and PHI pages; mask inputs |
| HubSpot tracking | Marketing site | Email, name, page views | HubSpot | Unconfirmed | **Medium** | Confirm/execute BAA; limit to marketing context |
| Intercom | Portal chat | Name, email, chat content | Intercom | Unconfirmed | **Medium** | Confirm/execute BAA |

## Notes that matter for the fix

- **"Hashed" is not "anonymized."** Marketing teams often believe that hashing the email before sending it to Meta makes it safe. It does not. Meta hashes on its side too and matches the hash to the user. A hashed identifier tied to a health event is still a disclosure of PHI.
- **Meta and TikTok cannot be made compliant here.** They do not sign BAAs. So the only remediation for those two on PHI-adjacent pages is removal. There is no configuration that makes it lawful.
- **GA4 is salvageable, but only after the PHI is stripped from what it ingests.** The service line has to come out of the URL path, and you have to confirm what a signed Google data-processing arrangement does and does not cover. Analytics is not automatically forbidden. Sending PHI to it is.
- **Session replay is the sleeper risk.** Hotjar was recording what patients typed into the intake questionnaire *before they hit submit*. That's symptom and mental-health data captured keystroke by keystroke. Input masking exists specifically for this and was not turned on.

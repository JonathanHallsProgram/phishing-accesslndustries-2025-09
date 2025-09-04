# phishing-accesslndustries-2025-09


**Status:** Confirmed phishing / brand impersonation  
**Date observed:** 2025-09-04 (America/Toronto)  
**Reporter:** Jonathan Halls

This repo documents a phishing email impersonating **Access Industries** using the look‑alike domain **accesslndustries[.]com** (lowercase **L**). Message referenced a “Service Support Engineer” role and mentioned “Stella Contracting Inc.” while routing through **Zoho Recruit / ZeptoMail**.

> ⚠️ **Privacy note**: All artifacts are sanitized (PII removed). Do **not** upload raw unredacted `.eml` files to public repos.

---

## Summary

- **Vector:** Email (multi-part plain/html) via Zoho Recruit  
- **Theme:** Job offer / interview scheduling  
- **Brand abuse:** Access Industries (real domain: `accessindustries.com`)  
- **Look‑alike:** `accesslndustries[.]com` (L vs I)  
- **Action taken:** Reported to the real company and provider; confirmed phishing by phone on 2025-09-04.

## Key Findings

- Authentication (SPF/DKIM/DMARC) passed for **viazohorecruit.com** (the mail service), **not** for Access Industries.  
- **Reply‑To** pointed to `careers@accesslndustries[.]com`.  
- **Cross‑brand confusion** (mentions “Stella Contracting Inc.”) — typical in job-impersonation lures.

## IOCs

See [`/iocs/indicators.csv`](iocs/indicators.csv) and STIX 2.1 bundle [`/iocs/stix2.json`](iocs/stix2.json).

## Timeline

- **2025-09-04 07:43 PDT** — Message received.  
- **2025-09-04** — Verified via phone with Access Industries: phishing/impersonation.  
- **2025-09-04** — Abuse notifications sent (brand + provider).

## Artifacts (sanitized)

- [`/artifacts/email_header_redacted.txt`](artifacts/email_header_redacted.txt) — selected headers (PII removed).  
- [`/artifacts/body_excerpt_redacted.md`](artifacts/body_excerpt_redacted.md) — minimal redacted content for context.

## Notifications

- [`/reports/notification-access-industries.md`](reports/notification-access-industries.md)  
- [`/reports/notification-zoho.md`](reports/notification-zoho.md)

## Responsible Disclosure / Ethics

- Only artifacts sent to the reporter’s inbox or publicly visible OSINT were used.  
- No interaction with attacker infrastructure beyond passive collection.  
- No execution of files/links; no probing.

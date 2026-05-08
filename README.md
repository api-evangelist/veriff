# Veriff (veriff)

Veriff is an AI-driven identity verification platform offering document, biometric, age, and proof-of-address verification, plus PEP/sanctions screening, ongoing monitoring, and Identity Fraud Protection. The Veriff Public API exposes session creation, media upload, decisions, attempts, watchlist screening, persons, and webhook delivery, with web and mobile SDKs hosting the capture experience.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=veriff-api-evangelist&utm_content=repo)

## Type

- **x-type:** company

## Tags

- KYC, Identity Verification, Biometrics, Fraud Prevention, AML, SaaS

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

| API | Description |
|---|---|
| Veriff Sessions API | Create, retrieve, mark submitted, and cancel verification sessions; parent resource. |
| Veriff Media API | Upload document images, selfies, and supporting media to a session. |
| Veriff Decisions API | Retrieve final session decision (status, reason, person data, risk metadata). |
| Veriff Attempts API | List individual attempts within a session for resubmission flows. |
| Veriff Persons API | Retrieve structured person data extracted from the verified document. |
| Veriff Watchlist Screening API | PEP / sanctions / adverse-media screening and ongoing monitoring. |
| Veriff Webhook Delivery | Server-to-server signed delivery of decision events (HMAC SHA-256). |
| Veriff Web (InContext / Hosted) SDK | Browser-based capture UI hosted in-page or on Veriff. |
| Veriff iOS SDK | Native iOS capture SDK. |
| Veriff Android SDK | Native Android capture SDK. |

## Authentication

- `X-AUTH-CLIENT` - API key from the Veriff Customer Portal
- `X-HMAC-SIGNATURE` - HMAC SHA-256 of the request body using the shared secret

## Common Properties

- [Website](https://www.veriff.com/)
- [Documentation](https://devdocs.veriff.com/)
- [GitHub](https://github.com/Veriff)
- [Plans](plans/veriff-plans-pricing.yml) - API Commons Plans 0.1
- [RateLimits](rate-limits/veriff-rate-limits.yml) - API Commons Rate Limits 0.1
- [FinOps](finops/veriff-finops.yml) - FOCUS-aligned FinOps Framework 1.0

## Plans

- **Free Trial** - 15 days, up to 50 live sessions, no credit card.
- **Essential** - $0.80/verification, $49/month minimum; full automation, 3-month retention.
- **Plus** - $1.39/verification, $99/month minimum; hybrid AI + specialist, 6-month retention.
- **Premium** - $1.89/verification, $209/month minimum; custom branding, bulk export, session deletion via API.
- **Enterprise** - Custom; volume discounts at 1,000+ verifications/month.
- **Add-Ons** - Extended 2-year retention (+$0.30), PEP/Sanctions Screening (+$0.64), Ongoing Monitoring (+$0.09).

## Rate Limits

- 429 Too Many Requests on dynamic per-API-key throttle; numeric ceiling not published.
- HMAC SHA-256 signature required on every request and verified on every webhook.
- Webhook delivery retries on receiver failure; persistent failures pause the subscription.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com

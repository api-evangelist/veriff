# Veriff (veriff)

Veriff is an AI-driven identity verification platform offering document, biometric, age, and proof-of-address verification, plus PEP/sanctions screening, ongoing monitoring, and Identity Fraud Protection. The Veriff Public API exposes session creation, media upload, decisions, attempts, watchlist screening, persons, and webhook delivery, with web and mobile SDKs hosting the capture experience.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/apis.yml)

## Tags

- KYC
- Identity Verification
- Biometrics
- Fraud Prevention
- AML
- SaaS

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-19

## APIs

### Veriff Sessions API

Creates and manages verification sessions. POST /sessions starts a verification and returns a session URL the end user opens via the SDK or hosted page. GET and PATCH endpoints retrieve the session, mark it as submitted (signal that all media has been uploaded), and cancel sessions. The session is the parent resource for media, decisions, attempts, and persons.

- **Human URL:** [https://devdocs.veriff.com/](https://devdocs.veriff.com/)
- **Base URL:** `https://stationapi.veriff.com/v1`

#### Tags

- Sessions
- Verification
- Onboarding

#### Properties

- [Documentation](https://devdocs.veriff.com/)
- [OpenAPI](openapi/veriff-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Media API

Uploads document images, selfies, and supporting media to a session and lists the media already attached. Used by custom flows that do not embed the Veriff SDK and capture media themselves.

- **Human URL:** [https://devdocs.veriff.com/](https://devdocs.veriff.com/)
- **Base URL:** `https://stationapi.veriff.com/v1`

#### Tags

- Media
- Uploads
- Documents

#### Properties

- [Documentation](https://devdocs.veriff.com/)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Decisions API

Retrieves the final verification decision for a submitted session - status (approved, declined, resubmission, expired), reason, code, person data extracted from the document, and risk metadata. Available as a pull endpoint and via webhook.

- **Human URL:** [https://devdocs.veriff.com/](https://devdocs.veriff.com/)
- **Base URL:** `https://stationapi.veriff.com/v1`

#### Tags

- Decisions
- Verification Results

#### Properties

- [Documentation](https://devdocs.veriff.com/)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Attempts API

Lists individual attempts within a session - useful when a session results in resubmission. Each attempt carries its own captured media and reason metadata.

- **Human URL:** [https://devdocs.veriff.com/](https://devdocs.veriff.com/)
- **Base URL:** `https://stationapi.veriff.com/v1`

#### Tags

- Attempts
- Resubmission

#### Properties

- [Documentation](https://devdocs.veriff.com/)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Persons API

Retrieves the person record extracted from a session decision - structured fields (first name, last name, date of birth, document number, nationality) and document metadata used for downstream KYC and CRM enrolment.

- **Human URL:** [https://devdocs.veriff.com/](https://devdocs.veriff.com/)
- **Base URL:** `https://stationapi.veriff.com/v1`

#### Tags

- Persons
- Identity Data

#### Properties

- [Documentation](https://devdocs.veriff.com/)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Watchlist Screening API

Runs and retrieves PEP, sanctions, adverse-media, and ongoing-monitoring screening tied to a verification session or to a stand-alone identity payload.

- **Human URL:** [https://www.veriff.com/products/aml](https://www.veriff.com/products/aml)
- **Base URL:** `https://stationapi.veriff.com/v1`

#### Tags

- AML
- Sanctions
- PEP
- Watchlist

#### Properties

- [Documentation](https://www.veriff.com/products/aml)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Webhook Delivery

Server-to-server delivery of decision and event notifications. Veriff signs each payload via the customer's shared secret using the X-HMAC-SIGNATURE header so receivers can verify authenticity. Customers configure the URL in the Veriff Customer Portal.

- **Human URL:** [https://devdocs.veriff.com/](https://devdocs.veriff.com/)
- **Base URL:** `customer-configured`

#### Tags

- Webhooks
- Events
- HMAC

#### Properties

- [Documentation](https://devdocs.veriff.com/)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Web (InContext / Hosted) SDK

Browser-based capture experience that embeds verification inside the customer's site (InContext) or runs as a Veriff-hosted page. Requires a session token issued by the Sessions API.

- **Human URL:** [https://github.com/Veriff](https://github.com/Veriff)
- **Base URL:** `https://github.com/Veriff`

#### Tags

- Web SDK
- JavaScript
- Capture

#### Properties

- [Documentation](https://github.com/Veriff)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff iOS SDK

Native iOS SDK that drives capture and streams media to Veriff. Initialised with a session URL.

- **Human URL:** [https://github.com/Veriff/veriff-ios](https://github.com/Veriff/veriff-ios)
- **Base URL:** `https://github.com/Veriff/veriff-ios`

#### Tags

- iOS SDK
- Mobile
- Capture

#### Properties

- [Documentation](https://github.com/Veriff/veriff-ios)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Veriff Android SDK

Native Android SDK for capture and media upload. Initialised with a session URL from the Sessions API.

- **Human URL:** [https://github.com/Veriff/veriff-android](https://github.com/Veriff/veriff-android)
- **Base URL:** `https://github.com/Veriff/veriff-android`

#### Tags

- Android SDK
- Mobile
- Capture

#### Properties

- [Documentation](https://github.com/Veriff/veriff-android)
- [Postman Collection](collections/veriff.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/veriff.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/veriff)
- [Website](https://www.veriff.com/)
- [Documentation](https://devdocs.veriff.com/)
- [Git Hub](https://github.com/Veriff)
- [Plans](plans/veriff-plans-pricing.yml)
- [Rate Limits](rate-limits/veriff-rate-limits.yml)
- [Fin Ops](finops/veriff-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

# Veriff (veriff)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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

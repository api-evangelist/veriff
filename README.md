# Veriff

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
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

**Areas:** KYC · Identity Verification · Biometrics · Fraud Prevention · AML · Software-as-a-Service

## Veriff on APIs.io

Everything profiled for Veriff is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/veriff/](https://apis.io/providers/veriff/)** — or go straight to one of the APIs or properties below.

### APIs (15)

- [Veriff Media API](https://apis.io/apis/veriff/media/) — Uploads document images, selfies, and supporting media to a session and lists the media already attached. Used by custom flows that do not embed the Veriff…
- [Veriff Decisions API](https://apis.io/apis/veriff/decisions/) — Retrieves the final verification decision for a submitted session - status (approved, declined, resubmission, expired), reason, code, person data extracted…
- [Veriff Attempts API](https://apis.io/apis/veriff/attempts/) — Lists individual attempts within a session - useful when a session results in resubmission. Each attempt carries its own captured media and reason metadata.
- [Veriff Persons API](https://apis.io/apis/veriff/persons/) — Retrieves the person record extracted from a session decision - structured fields (first name, last name, date of birth, document number, nationality) and…
- [Veriff Watchlist Screening API](https://apis.io/apis/veriff/watchlist-screening/) — Runs and retrieves PEP, sanctions, adverse-media, and ongoing-monitoring screening tied to a verification session or to a stand-alone identity payload.
- [Veriff Webhook Delivery](https://apis.io/apis/veriff/webhooks/) — Server-to-server delivery of decision and event notifications. Veriff signs each payload via the customer's shared secret using the X-HMAC-SIGNATURE header…
- [Veriff Web (InContext / Hosted) SDK](https://apis.io/apis/veriff/web-sdk/) — Browser-based capture experience that embeds verification inside the customer's site (InContext) or runs as a Veriff-hosted page. Requires a session token…
- [Veriff iOS SDK](https://apis.io/apis/veriff/ios-sdk/) — Native iOS SDK that drives capture and streams media to Veriff. Initialised with a session URL.
- [Veriff Android SDK](https://apis.io/apis/veriff/android-sdk/) — Native Android SDK for capture and media upload. Initialised with a session URL from the Sessions API.
- [Veriff Attempts API](https://apis.io/apis/veriff/veriff-attempts-api/) — The Attempts API from Veriff — 2 operation(s) for attempts.
- [Veriff Decisions API](https://apis.io/apis/veriff/veriff-decisions-api/) — The Decisions API from Veriff — 1 operation(s) for decisions.
- [Veriff Media API](https://apis.io/apis/veriff/veriff-media-api/) — The Media API from Veriff — 2 operation(s) for media.
- [Veriff Persons API](https://apis.io/apis/veriff/veriff-persons-api/) — The Persons API from Veriff — 1 operation(s) for persons.
- [Veriff Sessions API](https://apis.io/apis/veriff/veriff-sessions-api/) — The Sessions API from Veriff — 4 operation(s) for sessions.
- [Veriff Watchlist API](https://apis.io/apis/veriff/veriff-watchlist-api/) — The Watchlist API from Veriff — 1 operation(s) for watchlist.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Veriff Agentic Access](https://apis.io/agentic-access/veriff/veriff-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [Veriff Public API](https://apis.io/collections/veriff/open-veriff/)
- [Veriff Public Attempts API](https://apis.io/collections/veriff/open-veriff-attempts-api/)
- [Veriff Public Attempts Decisions API](https://apis.io/collections/veriff/open-veriff-decisions-api/)
- [Veriff Public Attempts Media API](https://apis.io/collections/veriff/open-veriff-media-api/)
- [Veriff Public Attempts Persons API](https://apis.io/collections/veriff/open-veriff-persons-api/)
- [Veriff Public Attempts Sessions API](https://apis.io/collections/veriff/open-veriff-sessions-api/)
- [Veriff Public Attempts Watchlist API](https://apis.io/collections/veriff/open-veriff-watchlist-api/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Veriff Authentication](https://apis.io/security/veriff/veriff-authentication/)
- [Veriff Domain Security](https://apis.io/security/veriff/veriff-domain-security/)
- [Veriff Vulnerability Disclosure](https://apis.io/security/veriff/veriff-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Veriff Plans Pricing](https://apis.io/plans/veriff/veriff-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Veriff Rate Limits](https://apis.io/rate-limits/veriff/veriff-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Veriff Finops](https://apis.io/finops/veriff/veriff-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.veriff.com/)
- [Documentation](https://devdocs.veriff.com/)
- [Blog](https://www.veriff.com/press)

## API Evangelist rating

**Kin Score 25.1** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 42.9 |
| Contract governance | 0.0 |
| Operational transparency | 13.2 |
| Developer ergonomics | 23.8 |
| Access clarity | 7.9 |

**Agent readiness 17.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 17.0** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/veriff/](https://apis.io/providers/veriff/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Veriff: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/veriff/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).

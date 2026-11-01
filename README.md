# Zonos

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

Zonos is a cross-border trade technology company headquartered in St. George, Utah, United States, that sells customs and trade compliance as an API. Its products calculate landed cost (duty, tax, brokerage and carrier fees), classify goods to HS codes with AI, screen parties and items against restricted and denied lists, rate and label international parcels, generate customs documents, submit postal PDDP declarations to destination posts, and file CBP entries for consolidated air consignments. It sits in the middle of the chain — between merchants, carriers, postal operators and freight consolidators on one side and customs authorities on the other — and is one of the few organizations in this tier whose integration surface is genuinely public rather than a customer-contract portal. A single unified GraphQL endpoint at https://api.zonos.com/graphql answers unauthenticated introspection (1,396 types, 170 queries, 153 mutations, harvested 2026-07-30), the reference is browsable without login at https://zonos.com/developer, and a legacy REST v1 layer remains documented but is declared end-of-life. Calling anything real still requires a credential token from the Zonos Dashboard, which is self-serve only for Shopify merchants; every other platform is routed through sales and an account agreement.

**Areas:** Logistics · Supply Chain · United States · Customs · Trade Compliance · Landed Cost · Duty and Tax · HS Classification · Cross-Border Commerce · Parcel · Postal · Track and Trace

## Zonos on APIs.io

Everything profiled for Zonos is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/zonos/](https://apis.io/providers/zonos/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Zonos Graph (GraphQL API)](https://apis.io/apis/zonos/zonos-graph-graphql-api/) — The Zonos Graph is the company's supported integration surface — a single GraphQL endpoint covering landed cost, classification, country of origin, export…
- [Zonos Landed Cost REST API (legacy)](https://apis.io/apis/zonos/zonos-landed-cost-rest-api/) — Legacy REST endpoint that returns a complete breakdown of the duties, taxes and fees making up a total landed cost for a shipment. Requires a…
- [Zonos Classify REST API (legacy)](https://apis.io/apis/zonos/zonos-classify-rest-api/) — Legacy REST endpoints for harmonizing a catalog to HS codes one item at a time or in bulk, with a group identifier for retrieving bulk results. Documented…
- [Zonos Rating REST API (legacy)](https://apis.io/apis/zonos/zonos-rating-rest-api/) — Legacy REST endpoint returning international shipping rates for carriers and service levels. Documented path is /v1/shipment_rating. Declared end-of-life in…
- [Zonos Order Complete REST API (legacy)](https://apis.io/apis/zonos/zonos-order-complete-rest-api/) — Legacy REST endpoint that accepts the details of a shopper's completed order and returns the Zonos-specific order ID. Documented path is /v1/orders.…
- [Zonos Checkout REST API (legacy)](https://apis.io/apis/zonos/zonos-checkout-rest-api/) — Legacy REST integration surface for Zonos Checkout, listed on the Zonos REST API reference index. No base URL or endpoint path was resolvable from the…

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://zonos.com/)
- [Documentation](https://zonos.com/docs)
- [API reference](https://zonos.com/developer)
- [Pricing](https://zonos.com/pricing)
- [Sign up](https://account.zonos.com/register)
- [Support](https://zonos.com/contact-support)
- [Blog](https://zonos.com/all-posts)
- [GitHub](https://github.com/Zonos)
- [Status](https://status.zonos.com)

## API Evangelist rating

**Kin Score 23.5** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 26.3 |
| Developer ergonomics | 52.4 |
| Access clarity | 23.7 |

**Agent readiness 8.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | unknown |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 5.9** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/zonos/](https://apis.io/providers/zonos/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Zonos: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/zonos/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).

# Zonos (zonos)

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

Zonos is a cross-border trade technology company headquartered in St. George, Utah, United States, that sells customs and trade compliance as an API — landed cost, AI HS-code classification, restricted-goods and denied-party screening, international checkout, rating, labels, customs documents, postal PDDP submission, and CBP entry filing. It sits between merchants, carriers, postal operators and freight consolidators on one side and customs authorities on the other. Its supported integration surface is a single public GraphQL endpoint whose schema answers unauthenticated introspection; a legacy REST v1 layer is documented but declared end-of-life.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/zonos/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zonos/refs/heads/main/apis.yml)

## Tags

- Logistics
- Supply Chain
- United States
- Customs
- Trade Compliance
- Landed Cost
- Duty and Tax
- HS Classification
- Cross-Border Commerce
- Parcel
- Postal
- Track and Trace
- Standards

## Timestamps

- **Created:** 2026-07-30
- **Modified:** 2026-07-30

## APIs

### Zonos Graph (GraphQL API)

The Zonos Graph is the company's supported integration surface — a single GraphQL endpoint covering landed cost, classification, country of origin, export control, item and party restriction screening, carts and checkout sessions, orders, shipments, ratings, labels, cartonization, customs documents and customs specs, manifests, consignments and consolidations, CBP entries, postal PDDP submissions, store credit and webhooks. Public introspection returned 1,396 types, 170 queries and 153 mutations on 2026-07-30 with no credential presented. There is no subscription type; asynchronous delivery is by webhook.

- **Human URL:** [https://zonos.com/developer](https://zonos.com/developer)
- **Base URL:** `https://api.zonos.com/graphql`

#### Tags

- GraphQL
- Landed Cost
- Customs
- Trade Compliance
- Classification
- Shipping
- Webhooks

#### Properties

- [GraphQL](graphql/zonos-graphql-schema.json) — introspection response, harvested verbatim 2026-07-30 (HTTP 200)
- [API Reference](https://zonos.com/developer)
- [Documentation](https://zonos.com/docs)
- [Why GraphQL](https://zonos.com/docs/supply-chain/why-graphql)
- [Webhooks](https://zonos.com/docs/supply-chain/webhooks)
- [Rate Limiting](https://zonos.com/docs/supply-chain/rate-limiting)
- [Idempotency](https://zonos.com/docs/supply-chain/idempotency)
- [API Errors](https://zonos.com/docs/supply-chain/api-errors)
- [OAuth](https://zonos.com/docs/supply-chain/oauth)
- [Retrieve GraphQL key](https://zonos.com/docs/account/retrieve-graphql-key)
- [TypeScript SDK](https://github.com/Zonos/fe-10-typescript-sdk)
- [PHP SDK](https://github.com/Zonos/zonos-php-sdk)

### Zonos Landed Cost REST API (legacy)

Legacy REST endpoint returning a complete breakdown of duties, taxes and fees making up a total landed cost. Requires a `zonos-version` request header. Declared end-of-life in favor of the Graph.

- **Human URL:** [https://zonos.com/docs/api-reference/landed-cost-rest-api](https://zonos.com/docs/api-reference/landed-cost-rest-api)
- **Base URL:** `https://api.zonos.com/v1/landed_cost`

### Zonos Classify REST API (legacy)

Legacy REST endpoints for harmonizing a catalog to HS codes, one item at a time or in bulk. Declared end-of-life in favor of the Graph.

- **Human URL:** [https://zonos.com/docs/api-reference/classify-rest-api](https://zonos.com/docs/api-reference/classify-rest-api)
- **Base URL:** `https://api.zonos.com/v1/classify`

### Zonos Rating REST API (legacy)

Legacy REST endpoint returning international shipping rates for carriers and service levels.

- **Human URL:** [https://zonos.com/docs/api-reference/rating-rest-api](https://zonos.com/docs/api-reference/rating-rest-api)
- **Base URL:** `https://api.zonos.com/v1/shipment_rating`

### Zonos Order Complete REST API (legacy)

Legacy REST endpoint that accepts a shopper's completed order and returns the Zonos-specific order ID.

- **Human URL:** [https://zonos.com/docs/api-reference/order-complete-rest-api](https://zonos.com/docs/api-reference/order-complete-rest-api)
- **Base URL:** `https://api.zonos.com/v1/orders`

### Zonos Checkout REST API (legacy)

Legacy REST integration surface for Zonos Checkout, listed on the REST reference index. No base URL was resolvable from the public reference page on 2026-07-30, so none is asserted.

- **Human URL:** [https://zonos.com/docs/api-reference/checkout-rest-api](https://zonos.com/docs/api-reference/checkout-rest-api)

## Interoperability

See [review.yml](review.yml) for the full evidence block. In short:

- **Standard conformance:** WCO Harmonized System (explicit `WcoVersion` enum, `WCO_1997` through `WCO_2072`), US CBP ACE CATAIR PGA message sets (APHIS PG10/PG14, EPA, FWS Form 3-177), UPU postal operator codes and the ITMATT declaration status, GS1 GTIN/UPC as an item identifier, and the EU/UK tax-identifier regimes (EORI, IOSS, VOEC). **No DCSA, no IATA ONE Record, no GS1 EPCIS, no UN/CEFACT, no eFTI, and no EDIFACT or ANSI X12 reference anywhere in the harvested schema.**
- **Interface shape:** `standard-plus-proprietary` — the vocabulary inside is standards-based, but the contract itself is a Zonos-proprietary GraphQL graph that nobody else implements.
- **Event model:** `webhook-push` — 23 `WebhookType` values, created with the `webhookCreate` mutation; no GraphQL subscription type exists.
- **EDI legacy:** No EDI referenced. This is a REST/GraphQL-native trade-compliance vendor, not an EDI house with a REST veneer.
- **Access gate:** Self-serve for Shopify merchants at `account.zonos.com/register`; every other platform requires a sign-up form, an account agreement and an onboarding representative.

## Common Properties

- [Website](https://zonos.com/)
- [Documentation](https://zonos.com/docs)
- [API Reference](https://zonos.com/developer)
- [GraphQL Schema](graphql/zonos-graphql-schema.json)
- [Authentication](https://zonos.com/docs/account/retrieve-graphql-key)
- [OAuth](https://zonos.com/docs/supply-chain/oauth)
- [Rate Limits](https://zonos.com/docs/supply-chain/rate-limiting)
- [Webhooks](https://zonos.com/docs/supply-chain/webhooks)
- [Pricing](https://zonos.com/pricing)
- [Sign Up](https://account.zonos.com/register)
- [Dashboard](https://dashboard.zonos.com)
- [Status](https://status.zonos.com)
- [GitHub Organization](https://github.com/Zonos)
- [LinkedIn](https://www.linkedin.com/company/zonos)
- [Blog](https://zonos.com/all-posts)
- [llms.txt](https://zonos.com/llms.txt)

## Maintainers

- Kin Lane — kin@apievangelist.com

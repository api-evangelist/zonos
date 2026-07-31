# Zonos (zonos)

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

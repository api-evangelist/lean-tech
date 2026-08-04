# Lean Technologies (lean-tech)

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

Lean Technologies is a Middle East Open Banking and Open Finance infrastructure provider founded in 2019 and headquartered in the UAE. Lean offers regulated Account Information (AIS), Payment Initiation (PIS), payouts, refunds, account and name verifications, and derived insights across the UAE and Saudi Arabia, with verification coverage extending to 27+ countries globally. Lean holds an In-Principle Approval from the Central Bank of UAE for Open Finance Services (August 2025), a Major Payment Institution licence from the Saudi Central Bank (SAMA), and an FSP licence from the Abu Dhabi Global Market FSRA (no. 200033). The platform is SOC 2 Type II and ISO 27001:2022 certified and has processed AED 16B+ across 2M+ linked accounts. Investors include Sequoia, General Catalyst, Breyer Capital, Shorooq, Raed, BCV, and Liberty City.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lean-tech/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lean-tech/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Open Banking
- Open Finance
- MENA
- UAE
- Saudi Arabia
- Payments
- Pay by Bank
- A2A
- Account Information
- Payment Initiation
- Verifications
- Identity
- Fintech

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Lean Authentication API

OAuth 2.0 client-credentials token issuance for Lean APIs. Generates API access tokens (scope=api) for server-to-server calls and customer-scoped access tokens (scope=customer.<customer_id>) for the LinkSDK. Production auth endpoint is auth.leantech.me; sandbox endpoints are regional (auth.sandbox.sa.leantech.me, auth.sandbox.ae.leantech.me).

- **Human URL:** [https://docs.leantech.me/docs/authentication](https://docs.leantech.me/docs/authentication)

#### Tags

- Authentication
- OAuth
- Open Banking

#### Properties

- [Documentation](https://docs.leantech.me/docs/authentication)
- [OpenAPI](openapi/lean-authentication-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-authentication-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-authentication-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Lean Customers API

Manage end-user customer records that Lean uses to anchor data and payment consents. Create customers with an app_user_id, list customers, and retrieve a customer by ID or by app_user_id.

- **Human URL:** [https://docs.leantech.me/reference/customers](https://docs.leantech.me/reference/customers)

#### Tags

- Customers
- Open Banking
- End Users

#### Properties

- [Documentation](https://docs.leantech.me/reference/customers)
- [OpenAPI](openapi/lean-customers-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-customers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-customers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/lean-customer-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Lean Entities API

Entities represent a customer's authenticated connection to a single bank, returned after a successful LinkSDK consent. List entities for a customer, retrieve a single entity by ID, or query entities across a date range.

- **Human URL:** [https://docs.leantech.me/reference/entities](https://docs.leantech.me/reference/entities)

#### Tags

- Entities
- Open Banking
- Consents

#### Properties

- [Documentation](https://docs.leantech.me/reference/entities)
- [OpenAPI](openapi/lean-entities-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-entities-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-entities-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Lean Data API

Raw bank-account data retrieval (v2) returning accounts, transactions, balances, beneficiaries, standing orders, scheduled payments, direct debits, and identity, plus manual data refresh triggers and refresh status. Available after an Account Information consent has been collected via the LinkSDK.

- **Human URL:** [https://docs.leantech.me/reference/data-api](https://docs.leantech.me/reference/data-api)

#### Tags

- Open Banking
- Account Information
- Transactions
- Balances
- Identity

#### Properties

- [Documentation](https://docs.leantech.me/reference/data-api)
- [OpenAPI](openapi/lean-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/lean-account-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/lean-transaction-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/lean-tech-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Lean Insights API

Derived analytics over an entity's transaction history — income detection, expense categorisation, and cashflow summaries — for underwriting, affordability, and BFM use cases.

- **Human URL:** [https://docs.leantech.me/reference/insights](https://docs.leantech.me/reference/insights)

#### Tags

- Open Banking
- Insights
- Income
- Expenses
- Cashflows

#### Properties

- [Documentation](https://docs.leantech.me/reference/insights)
- [OpenAPI](openapi/lean-insights-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-insights-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-insights-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Lean Banks API

List the banks Lean currently supports for Data and Payments per region, including identifiers, logos, and supported product surfaces (AIS, PIS, AOF, payouts).

- **Human URL:** [https://docs.leantech.me/reference/banks](https://docs.leantech.me/reference/banks)

#### Tags

- Open Banking
- Banks
- Coverage

#### Properties

- [Documentation](https://docs.leantech.me/reference/banks)
- [OpenAPI](openapi/lean-banks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-banks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-banks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Lean Verifications API

Account Verification confirms ownership and validity of a bank account by IBAN or local account number across 27+ countries (UAE, KSA, GB, US, EU, BR, IN, ID, NG, ZA, and more). Name Verification compares a supplied name against a payee record. Used for fraud reduction, payout pre-checks, and Confirmation of Payee.

- **Human URL:** [https://docs.leantech.me/reference/verifications](https://docs.leantech.me/reference/verifications)

#### Tags

- Verifications
- Account Verification
- Name Verification
- KYC

#### Properties

- [Documentation](https://docs.leantech.me/reference/verifications)
- [OpenAPI](openapi/lean-verifications-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-verifications-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-verifications-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Lean Payments API

Single Instant Payment ("Pay by Bank") and Account-on-File (AOF) payment initiation, plus consent management. Create payment intents, retrieve payments by intent or payment id, list payment intents, and manage long-lived AOF consents with balance and history endpoints.

- **Human URL:** [https://docs.leantech.me/reference/payments](https://docs.leantech.me/reference/payments)

#### Tags

- Open Banking
- Payments
- Pay by Bank
- PIS
- A2A

#### Properties

- [Documentation](https://docs.leantech.me/reference/payments)
- [OpenAPI](openapi/lean-payments-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-payments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-payments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/lean-payment-intent-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Lean Payment Sources API

Tokenized representation of a customer's funding bank account once linked. List payment sources for a customer, retrieve a single source by ID, and delete a payment source to revoke its associated AOF consent.

- **Human URL:** [https://docs.leantech.me/reference/payment-sources](https://docs.leantech.me/reference/payment-sources)

#### Tags

- Open Banking
- Payment Sources
- Tokenization

#### Properties

- [Documentation](https://docs.leantech.me/reference/payment-sources)
- [OpenAPI](openapi/lean-payment-sources-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-payment-sources-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-payment-sources-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Lean Payouts API

Initiate outbound bank-to-bank payouts from corporate accounts to consumer or business beneficiaries. Create payout payments, list payouts, retrieve a payout intent, get per-payment history, and manage payout destinations (the beneficiary records that receive funds).

- **Human URL:** [https://docs.leantech.me/reference/payouts](https://docs.leantech.me/reference/payouts)

#### Tags

- Open Banking
- Payouts
- Disbursements
- A2A

#### Properties

- [Documentation](https://docs.leantech.me/reference/payouts)
- [OpenAPI](openapi/lean-payouts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-payouts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-payouts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/lean-payout-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Lean Refunds API

Issue full or partial refunds against prior Pay by Bank payments. List refunds, create a new refund, process queued refunds, and retrieve the canonical list of refund reason codes.

- **Human URL:** [https://docs.leantech.me/reference/refunds](https://docs.leantech.me/reference/refunds)

#### Tags

- Open Banking
- Refunds
- Payouts

#### Properties

- [Documentation](https://docs.leantech.me/reference/refunds)
- [OpenAPI](openapi/lean-refunds-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lean-refunds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lean-refunds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/leantech)
- [Portal](https://www.leantech.me)
- [Documentation](https://docs.leantech.me)
- [Documentation](https://docs.leantech.me/reference)
- [Console](https://dev.leantech.me)
- [Status Page](https://status.leantech.me)
- [Support](https://help.leantech.me)
- [Documentation](https://docs.leantech.me/docs/authentication)
- [Source Code](https://github.com/leantechnologies)
- [Postman Collection](https://github.com/leantechnologies/lean-postman) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [SDK](https://github.com/leantechnologies/link-sdk-react-native)
- [SDK](https://github.com/leantechnologies/link-sdk-ios-distribution)
- [SDK](https://github.com/leantechnologies/link-sdk-flutter)
- [Sample Code](https://github.com/leantechnologies/integration-snippets)
- [Plans](plans/lean-tech-plans-pricing.yml)
- [Rate Limits](rate-limits/lean-tech-rate-limits.yml)
- [Fin Ops](finops/lean-tech-finops.yml)
- [Vocabulary](vocabulary/lean-tech-vocabulary.yml)
- [Spectral Rules](rules/lean-tech-rules.yml)

## Maintainers

**FN:** API Evangelist
**Email:** info@apievangelist.com

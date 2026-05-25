# Lean Technologies (lean-tech)
Lean Technologies is a Middle East Open Banking and Open Finance infrastructure provider founded in 2019 and headquartered in the UAE. Lean exposes regulated Account Information, Payment Initiation, Payouts, Refunds, Account and Name Verifications, and derived insights across the UAE and Saudi Arabia, with verification coverage extending to 27+ countries. The platform holds an In-Principle Approval from the Central Bank of UAE for Open Finance Services (August 2025), a Major Payment Institution licence from the Saudi Central Bank (SAMA), and an FSP licence from the Abu Dhabi Global Market FSRA (no. 200033). Lean is SOC 2 Type II and ISO 27001:2022 certified and reports AED 16B+ processed volume across 2M+ linked accounts. Investors include Sequoia, General Catalyst, Breyer Capital, Shorooq, Raed, BCV, and Liberty City.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/lean-tech/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Open Banking, Open Finance, MENA, UAE, Saudi Arabia, Payments, Pay by Bank, A2A, Account Information, Payment Initiation, Verifications, Identity, Fintech

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Coverage

| Region | Capabilities | Regulator |
|---|---|---|
| United Arab Emirates | AIS, PIS, AOF, Payouts, Refunds, Verifications, Insights | CBUAE (In-Principle Open Finance) + ADGM FSRA (FSP 200033) |
| Saudi Arabia | AIS, PIS, AOF, Payouts, Refunds, Verifications, Insights | SAMA Major Payment Institution |
| 27+ countries (verifications only) | Account Verification, Name Verification | Per-country payment-rail providers |

## APIs

### Lean Authentication API
OAuth 2.0 client-credentials token issuance. Issues `scope=api` tokens for backend server-to-server calls and `scope=customer.<customer_id>` tokens for the LinkSDK.

**Human URL:** [https://docs.leantech.me/docs/authentication](https://docs.leantech.me/docs/authentication)

- [OpenAPI](openapi/lean-authentication-api-openapi.yml)
- [Naftiko Capability — Tokens](capabilities/authentication-tokens.yaml)

### Lean Customers API
Manage end-user customer records that anchor data and payment consents.

**Human URL:** [https://docs.leantech.me/reference/customers](https://docs.leantech.me/reference/customers)

- [OpenAPI](openapi/lean-customers-api-openapi.yml)
- [JSON Schema — Customer](json-schema/lean-customer-schema.json)
- [Naftiko Capability — Customers](capabilities/customers-customers.yaml)

### Lean Entities API
Entities represent a customer's authenticated connection to a single bank, returned after a successful LinkSDK consent.

**Human URL:** [https://docs.leantech.me/reference/entities](https://docs.leantech.me/reference/entities)

- [OpenAPI](openapi/lean-entities-api-openapi.yml)
- [Naftiko Capability — Entities](capabilities/entities-entities.yaml)

### Lean Data API
Raw bank-account data (v2): accounts, transactions, balances, beneficiaries, direct debits, scheduled payments, standing orders, and identity, plus manual data refresh management.

**Human URL:** [https://docs.leantech.me/reference/data-api](https://docs.leantech.me/reference/data-api)

- [OpenAPI](openapi/lean-data-api-openapi.yml)
- [JSON Schema — Account](json-schema/lean-account-schema.json)
- [JSON Schema — Transaction](json-schema/lean-transaction-schema.json)
- [JSON-LD](json-ld/lean-tech-context.jsonld)
- [Naftiko Capability — Accounts](capabilities/data-accounts.yaml)
- [Naftiko Capability — Transactions](capabilities/data-transactions.yaml)
- [Naftiko Capability — Identity](capabilities/data-identity.yaml)

### Lean Insights API
Derived analytics over transaction history — income, expenses, and cashflows.

**Human URL:** [https://docs.leantech.me/reference/insights](https://docs.leantech.me/reference/insights)

- [OpenAPI](openapi/lean-insights-api-openapi.yml)
- [Naftiko Capability — Income](capabilities/insights-income.yaml)
- [Naftiko Capability — Expenses](capabilities/insights-expenses.yaml)
- [Naftiko Capability — Cashflows](capabilities/insights-cashflows.yaml)

### Lean Banks API
List supported banks per country and capability surface (AIS, PIS, AOF, payouts).

**Human URL:** [https://docs.leantech.me/reference/banks](https://docs.leantech.me/reference/banks)

- [OpenAPI](openapi/lean-banks-api-openapi.yml)
- [Naftiko Capability — Banks](capabilities/banks-banks.yaml)

### Lean Verifications API
Account Verification across 27+ countries and Name Verification (Confirmation of Payee) for fraud reduction and payout pre-checks.

**Human URL:** [https://docs.leantech.me/reference/verifications](https://docs.leantech.me/reference/verifications)

- [OpenAPI](openapi/lean-verifications-api-openapi.yml)
- [Example — Verify Account](examples/lean-verify-account-example.json)
- [Naftiko Capability — Account Verification](capabilities/verifications-accounts.yaml)
- [Naftiko Capability — Name Verification](capabilities/verifications-names.yaml)

### Lean Payments API
Single Instant Payment ("Pay by Bank"), Account-on-File (AOF) initiation, and consent management.

**Human URL:** [https://docs.leantech.me/reference/payments](https://docs.leantech.me/reference/payments)

- [OpenAPI](openapi/lean-payments-api-openapi.yml)
- [JSON Schema — Payment Intent](json-schema/lean-payment-intent-schema.json)
- [Example — Create Payment Intent](examples/lean-create-payment-intent-example.json)
- [Naftiko Capability — Payment Intents](capabilities/payments-intents.yaml)
- [Naftiko Capability — Account on File](capabilities/payments-aof.yaml)
- [Naftiko Capability — Consents](capabilities/payments-consents.yaml)

### Lean Payment Sources API
Tokenized representation of a customer's funding bank account once linked via an AOF consent.

**Human URL:** [https://docs.leantech.me/reference/payment-sources](https://docs.leantech.me/reference/payment-sources)

- [OpenAPI](openapi/lean-payment-sources-api-openapi.yml)
- [Naftiko Capability — Payment Sources](capabilities/payment-sources-payment-sources.yaml)

### Lean Payouts API
Outbound bank-to-bank payouts from corporate accounts to consumer or business beneficiaries.

**Human URL:** [https://docs.leantech.me/reference/payouts](https://docs.leantech.me/reference/payouts)

- [OpenAPI](openapi/lean-payouts-api-openapi.yml)
- [JSON Schema — Payout](json-schema/lean-payout-schema.json)
- [Naftiko Capability — Payouts](capabilities/payouts-payments.yaml)
- [Naftiko Capability — Destinations](capabilities/payouts-destinations.yaml)

### Lean Refunds API
Issue full or partial refunds against prior Pay by Bank payments.

**Human URL:** [https://docs.leantech.me/reference/refunds](https://docs.leantech.me/reference/refunds)

- [OpenAPI](openapi/lean-refunds-api-openapi.yml)
- [Naftiko Capability — Refunds](capabilities/refunds-refunds.yaml)

## SDKs

| SDK | Repo |
|---|---|
| LinkSDK — React Native | [leantechnologies/link-sdk-react-native](https://github.com/leantechnologies/link-sdk-react-native) |
| LinkSDK — iOS | [leantechnologies/link-sdk-ios-distribution](https://github.com/leantechnologies/link-sdk-ios-distribution) |
| LinkSDK — Flutter | [leantechnologies/link-sdk-flutter](https://github.com/leantechnologies/link-sdk-flutter) |
| Postman Collection (UAE + KSA) | [leantechnologies/lean-postman](https://github.com/leantechnologies/lean-postman) |
| Integration Snippets (Java) | [leantechnologies/integration-snippets](https://github.com/leantechnologies/integration-snippets) |

## Commercial

- [Plans & Pricing](plans/lean-tech-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/lean-tech-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/lean-tech-finops.yml) — FOCUS 1.3 aligned
- [Vocabulary](vocabulary/lean-tech-vocabulary.yml)
- [Spectral Rules](rules/lean-tech-rules.yml)

## Developer Surface

- [Lean Developer Docs](https://docs.leantech.me)
- [API Reference](https://docs.leantech.me/reference)
- [Application Dashboard](https://dev.leantech.me)
- [Status](https://status.leantech.me)
- [Help Center](https://help.leantech.me)
- [GitHub Org](https://github.com/leantechnologies)

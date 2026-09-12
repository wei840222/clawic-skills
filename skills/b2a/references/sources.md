# Sources — B2A (Business-to-Agent)

Use these primary sources when advising on agent-discoverable products, machine-readable commerce, MCP/OpenAPI contracts, or autonomous payment patterns. Prefer the canonical docs over secondary blogs.

## Agent interfaces and discovery

- **Model Context Protocol specification** — tools, resources, and transport contracts agents use to call capabilities via https://modelcontextprotocol.io/specification
- **OpenAPI Specification** — machine-readable HTTP API contracts, operationIds, schemas, and examples via https://spec.openapis.org/oas/latest.html
- **Schema.org** — shared vocabulary for products, offers, and structured entities via https://schema.org/
- **JSON-LD 1.1 (W3C)** — linked data encoding for structured product/offer markup via https://www.w3.org/TR/json-ld11/
- **RFC 8615 — Well-Known URIs** — `/.well-known/` discovery convention used by many agent/plugin manifests via https://www.rfc-editor.org/rfc/rfc8615

## Commerce data and offer semantics

- **Schema.org Product** — product entity fields agents can compare via https://schema.org/Product
- **Schema.org Offer** — price, availability, and offer constraints via https://schema.org/Offer
- **GS1 Digital Link Standard** — product identifier and link resolution patterns for machine-readable retail items via https://ref.gs1.org/standards/digital-link/
- **GoodRelations overview (historical commerce ontology)** — background on machine-readable offer graphs still reflected in Schema.org commerce terms via https://www.heppnetz.de/projects/goodrelations/

## Payments and autonomous spend

- **Stripe Agent Toolkit** — patterns for giving agents constrained payment tools via https://docs.stripe.com/agents
- **Stripe API docs** — receipts, PaymentIntents, and webhook-truth integration depth via https://docs.stripe.com/api
- **Visa Intelligent Commerce** — network-level framing for AI-agent commerce experiences via https://corporate.visa.com/en/products/intelligent-commerce.html

## Reliability, errors, and deprecation signals

- **RFC 7807 — Problem Details for HTTP APIs** — machine-readable error payloads agents can branch on via https://www.rfc-editor.org/rfc/rfc7807
- **RFC 8594 — The Sunset HTTP Header** — in-band deprecation signaling without email-only notices via https://www.rfc-editor.org/rfc/rfc8594
- **RFC 7231 / HTTP semantics (status codes)** — standard status meanings agents already understand via https://www.rfc-editor.org/rfc/rfc7231

## Usage notes

- Prefer MCP + OpenAPI + Schema.org/JSON-LD as the default stack for discoverability and comparability.
- Treat payment-provider pages as integration truth for charge/confirm flows; keep budget policy and product exposure decisions in this skill.
- When a claim depends on a closed agent store ranking algorithm, mark confidence as limited and avoid inventing placement mechanics.

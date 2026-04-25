# CloudZero (cloudzero)

CloudZero is a cloud cost intelligence and FinOps platform that automates the collection, allocation, and analysis of infrastructure spend to uncover waste and improve unit economics. The CloudZero API V2 is REST-oriented, uses API key authentication, and exposes endpoints for querying billing costs and dimensions, managing insights and budgets, sending unit metric and allocation telemetry, and ingesting cost data from any source via the AnyCost framework.

**APIs.json:** [apis.yml](https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party
- **x-type:** company

## Tags

Budgets, Cloud Cost Management, Cost Allocation, Cost Optimization, FinOps, Telemetry, Unit Economics

## Timestamps

- **Created:** 2026-01-02
- **Modified:** 2026-04-23

## APIs

### CloudZero API
The aggregate V2 REST API. Endpoints for billing, insights, budgets, allocation telemetry, unit metric telemetry, and AnyCost ingestion. Authentication uses an API key header.

- Base URL: `https://api.cloudzero.com`
- [Documentation](https://docs.cloudzero.com/reference/introduction)
- [OpenAPI](openapi/cloudzero-api-openapi.yml)
- [Authorization](https://docs.cloudzero.com/reference/authorization)

### CloudZero Billing API
Cost and dimension data over a date range with selectable dimensions (account, service, region, custom dimensions) and metrics (real_cost, billed_cost). Pagination via page and page_size.

- Base URL: `https://api.cloudzero.com/v2/billing`

### CloudZero Insights API
Store and surface actionable cost insights and recommendations. List, create, update, and delete insights with assigned owners, severity, status, and estimated savings.

- Base URL: `https://api.cloudzero.com/v2/insights`

### CloudZero Budgets API
Manage cost-and-usage budgets, alert thresholds, and actuals tracking. List, create, update, and delete budgets and surface current consumption against limits.

- Base URL: `https://api.cloudzero.com/v2/budgets`

### CloudZero Allocation Telemetry API
Send, edit, and delete allocation telemetry data for splitting cloud cost across custom allocation dimensions via named streams. Sum, replace, and delete operations.

- Base URL: `https://api.cloudzero.com/v1/telemetry/allocation`

### CloudZero Unit Metric Telemetry API
Ingest business metrics that drive unit-economics calculations: cost per customer, cost per transaction, cost per tenant.

- Base URL: `https://api.cloudzero.com/v1/telemetry`

### CloudZero AnyCost API
Ingest cost data from any source using the AnyCost Stream Adaptor and Common Bill Format (CBF). Upload normalized billing drops alongside native AWS, Azure, and GCP integrations.

- Base URL: `https://api.cloudzero.com/v2/connections/billing/anycost`

## Common Properties

- [Website](https://www.cloudzero.com/)
- [Portal](https://app.cloudzero.com/)
- [Documentation](https://docs.cloudzero.com/)
- [Pricing](https://www.cloudzero.com/pricing/)
- [Status](https://status.cloudzero.com/)
- [GitHub](https://github.com/Cloudzero)

## Artifacts

- [OpenAPI](openapi/cloudzero-api-openapi.yml)
- [JSON Schema: Cost](json-schema/cloudzero-cost.json)
- [JSON Schema: Insight](json-schema/cloudzero-insight.json)
- [JSON Schema: Budget](json-schema/cloudzero-budget.json)
- [JSON Schema: Telemetry Record](json-schema/cloudzero-telemetry-record.json)
- [JSON Schema: Billing Drop](json-schema/cloudzero-billing-drop.json)
- [JSON-LD Context](json-ld/cloudzero-context.jsonld)
- [Spectral Rules](rules/cloudzero-rules.yml)
- [Naftiko Capabilities](capabilities/cloud-cost-finops.yaml)

## Maintainers

- **FN:** Kin Lane
- **Email:** kin@apievangelist.com

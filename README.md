# CloudZero (cloudzero)

CloudZero is a cloud cost intelligence and FinOps platform that automates the collection, allocation, and analysis of infrastructure spend to uncover waste and improve unit economics. The CloudZero API V2 is REST-oriented, uses API key authentication, and exposes endpoints for querying billing costs and dimensions, managing insights and budgets, sending unit metric and allocation telemetry, and ingesting cost data from any source via the AnyCost framework.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Budgets
- Cloud Cost Management
- Cost Allocation
- Cost Optimization
- FinOps
- Telemetry
- Unit Economics

## Timestamps

- **Created:** 2026-01-02
- **Modified:** 2026-05-19

## APIs

### CloudZero API

The CloudZero API V2 enables you to automate the collection, allocation, and analysis of your infrastructure spend. It provides endpoints for querying billing costs and dimensions, managing insights and budgets, sending unit metric and allocation telemetry data, and ingesting cost data from any source via the AnyCost framework.

- **Human URL:** [https://docs.cloudzero.com/reference/introduction](https://docs.cloudzero.com/reference/introduction)
- **Base URL:** `https://api.cloudzero.com`

#### Tags

- Billing
- Budgets
- Cloud Costs
- Cost Allocation
- FinOps
- Insights
- Telemetry
- Unit Economics

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/introduction)
- [OpenAPI](openapi/cloudzero-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authorization](https://docs.cloudzero.com/reference/authorization)
- [JSON Schema](json-schema/cloudzero-cost.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cloudzero-insight.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cloudzero-budget.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cloudzero-telemetry-record.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cloudzero-billing-drop.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/cloudzero-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/cloudzero-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)

### CloudZero Billing API

The Billing API exposes cost and dimension data for analysis. Endpoints under /v2/billing return cost rows over a date range with selectable dimensions (account, service, region, custom dimension) and metrics (real_cost, billed_cost). Pagination uses page and page_size query parameters.

- **Human URL:** [https://docs.cloudzero.com/reference/billing](https://docs.cloudzero.com/reference/billing)
- **Base URL:** `https://api.cloudzero.com/v2/billing`

#### Tags

- Billing
- Cost Reporting
- Dimensions

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/billing)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CloudZero Insights API

The Insights API stores and surfaces actionable cost insights and recommendations. Endpoints under /v2/insights support listing, creating, updating, and deleting insight records, including assigned owners, severity, status, and estimated savings.

- **Human URL:** [https://docs.cloudzero.com/reference/insights](https://docs.cloudzero.com/reference/insights)
- **Base URL:** `https://api.cloudzero.com/v2/insights`

#### Tags

- Cost Optimization
- Insights
- Recommendations

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/insights)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CloudZero Budgets API

The Budgets API manages cost-and-usage budgets, alerts, thresholds, and actuals tracking. Endpoints under /v2/budgets list, create, update, and delete budgets and surface current consumption against limits.

- **Human URL:** [https://docs.cloudzero.com/reference/budgets](https://docs.cloudzero.com/reference/budgets)
- **Base URL:** `https://api.cloudzero.com/v2/budgets`

#### Tags

- Alerts
- Budgets
- FinOps

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/budgets)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CloudZero Allocation Telemetry API

Allocation Telemetry sends, edits, and deletes allocation telemetry data for splitting cloud cost across custom allocation dimensions. Endpoints under /v1/telemetry/allocation/{stream_name} support sum, replace, and delete operations against a named telemetry stream.

- **Human URL:** [https://docs.cloudzero.com/reference/allocation-telemetry](https://docs.cloudzero.com/reference/allocation-telemetry)
- **Base URL:** `https://api.cloudzero.com/v1/telemetry/allocation`

#### Tags

- Allocation
- Cost Splitting
- Telemetry

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/allocation-telemetry)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CloudZero Unit Metric Telemetry API

Unit Metric Telemetry ingests business metrics that drive unit-economics calculations (cost per customer, cost per transaction, cost per tenant). Endpoints under /v1/telemetry/{stream_name} support submitting records, deleting, and replacing values for named streams.

- **Human URL:** [https://docs.cloudzero.com/reference/unit-metric-telemetry](https://docs.cloudzero.com/reference/unit-metric-telemetry)
- **Base URL:** `https://api.cloudzero.com/v1/telemetry`

#### Tags

- Telemetry
- Unit Economics
- Unit Metrics

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/unit-metric-telemetry)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CloudZero AnyCost API

AnyCost ingests cost data from any source using the AnyCost Stream Adaptor and Common Bill Format (CBF). Endpoints under /v2/connections/billing/anycost/{connection_id}/billing_drops accept uploads of normalized billing drops alongside native AWS, Azure, and GCP integrations.

- **Human URL:** [https://docs.cloudzero.com/reference/anycost](https://docs.cloudzero.com/reference/anycost)
- **Base URL:** `https://api.cloudzero.com/v2/connections/billing/anycost`

#### Tags

- AnyCost
- Billing Drop
- CBF
- Common Bill Format
- Ingestion

#### Properties

- [Documentation](https://docs.cloudzero.com/reference/anycost)
- [Postman Collection](collections/cloudzero-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudzero-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/cloudzero)
- [Website](https://www.cloudzero.com/)
- [Portal](https://app.cloudzero.com/)
- [Documentation](https://docs.cloudzero.com/)
- [Pricing](https://www.cloudzero.com/pricing/)
- [Status Page](https://status.cloudzero.com/)
- [Git Hub](https://github.com/Cloudzero)
- [Terms of Service](https://www.cloudzero.com/terms-of-service/)
- [Privacy](https://www.cloudzero.com/privacy-policy/)
- [Integrations](https://www.cloudzero.com/integrations/)
- [L L Ms Txt](https://docs.cloudzero.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

# Restaurant365 (restaurant365)
Restaurant365 is a cloud-based restaurant accounting, inventory, and operations platform serving thousands of restaurant locations across the United States. Its developer offering centers on the R365 API, which lets approved third-party vendors and partners connect to a customer's R365 database to retrieve data and create or push records such as AP invoices and general ledger entries. A complementary OData connector exposes sales, transaction, location, GL account, employee, and labor data for use in external reporting and business-intelligence tools. API access is provisioned per customer through R365 Support, with bearer-token authentication on the R365 API and Domain\Username basic authentication on the OData connector.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/restaurant365/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Restaurant, Accounting, Inventory, Operations, Invoices, Reporting, OData

## Timestamps

- **Created:** 2026-06-02
- **Modified:** 2026-06-03

## APIs

### R365 API
The R365 API lets approved third-party services and vendors connect to a Restaurant365 customer database to retrieve data and create or push records, including AP invoices, GL-coded AP invoices, and general ledger journal entries. A username and password are first exchanged at /APIv1/Authenticate for a bearer token, which is then sent on every subsequent request. Access is provisioned per customer by contacting R365 Support to enable a vendor.

**Human URL:** [https://docs.restaurant365.com/docs/r365-api](https://docs.restaurant365.com/docs/r365-api)

**Base URL:** `https://yourcompany.restaurant365.com`

#### Tags:

 - Invoices, General Ledger, Accounting

#### Properties

- [Documentation](https://docs.restaurant365.com/docs/r365-api)
- [Documentation](https://docs.restaurant365.com/docs/r365-api-connector)
- [OpenAPI](openapi/restaurant365-r365-api-openapi.yml)
- [Authentication](https://docs.restaurant365.com/docs/r365-api-connector)
- [JSONSchema](json-schema/r365-api-ap-invoice-schema.json)
- [JSONSchema](json-schema/r365-api-journal-entry-schema.json)
- [JSONStructure](json-structure/r365-api-ap-invoice-structure.json)
- [JSONStructure](json-structure/r365-api-journal-entry-structure.json)
- [JSONLD](json-ld/restaurant365-r365-api-context.jsonld)
- [Example](examples/r365-api-authenticate-example.json)
- [Example](examples/r365-api-create-ap-invoices-example.json)
- [Example](examples/r365-api-create-ap-invoices-gl-example.json)
- [Example](examples/r365-api-create-journal-entries-example.json)

#### Naftiko Capabilities

- [r365-api-authentication.yaml](capabilities/r365-api-authentication.yaml) — Authentication (1 tool)
- [r365-api-ap-invoices.yaml](capabilities/r365-api-ap-invoices.yaml) — AP Invoices (1 tool)
- [r365-api-general-ledger.yaml](capabilities/r365-api-general-ledger.yaml) — General Ledger (2 tools)

### Restaurant365 OData Connector
The Restaurant365 OData connector exposes R365 data to OData-compatible reporting and BI tools through read-only views for companies, locations, GL accounts, items, job titles, employees, POS employees, labor detail, payroll summary, transactions, transaction detail, sales, and deleted entities. Most views support $filter, $orderby, $select, $skip, and $top. Sales views are limited to a 31-day date range per request and do not support $select or $count.

**Human URL:** [https://docs.restaurant365.com/docs/restaurant365-odata-connector](https://docs.restaurant365.com/docs/restaurant365-odata-connector)

**Base URL:** `https://odata.restaurant365.net/api/v2/views/`

#### Tags:

 - OData, Reporting, Sales

#### Properties

- [Documentation](https://docs.restaurant365.com/docs/restaurant365-odata-connector)
- [OpenAPI](openapi/restaurant365-odata-connector-openapi.yml)
- [Authentication](https://docs.restaurant365.com/docs/restaurant365-odata-connector)
- [JSONSchema](json-schema/odata-connector-transaction-schema.json)
- [JSONSchema](json-schema/odata-connector-sales-employee-schema.json)
- [JSONSchema](json-schema/odata-connector-gl-account-schema.json)
- [JSONSchema](json-schema/odata-connector-employee-schema.json)
- [JSONStructure](json-structure/odata-connector-transaction-structure.json)
- [JSONStructure](json-structure/odata-connector-sales-employee-structure.json)
- [JSONLD](json-ld/restaurant365-odata-connector-context.jsonld)
- [Example](examples/odata-connector-list-transactions-example.json)
- [Example](examples/odata-connector-list-sales-employee-example.json)

#### Naftiko Capabilities

- [odata-connector-metadata.yaml](capabilities/odata-connector-metadata.yaml) — Metadata (1 tool)
- [odata-connector-reference-data.yaml](capabilities/odata-connector-reference-data.yaml) — Reference Data (5 tools)
- [odata-connector-labor.yaml](capabilities/odata-connector-labor.yaml) — Labor (4 tools)
- [odata-connector-transactions.yaml](capabilities/odata-connector-transactions.yaml) — Transactions (2 tools)
- [odata-connector-sales.yaml](capabilities/odata-connector-sales.yaml) — Sales (3 tools)
- [odata-connector-audit.yaml](capabilities/odata-connector-audit.yaml) — Audit (1 tool)

## Common Properties

- [Website](https://www.restaurant365.com)
- [Documentation](https://docs.restaurant365.com/docs/r365-api)
- [Pricing](https://www.restaurant365.com/pricing/)
- [Plans](plans/restaurant365-plans-pricing.yml)
- [RateLimits](rate-limits/restaurant365-rate-limits.yml)
- [SpectralRules](rules/restaurant365-rules.yml)
- [Vocabulary](vocabulary/restaurant365-vocabulary.yml)
- [Blog](https://www.restaurant365.com/blog/)
- [GitHubOrganization](https://github.com/restaurant365)
- [LinkedIn](https://www.linkedin.com/company/restaurant365-cloud-erp-for-restaurants)
- [LLMsTxt](https://docs.restaurant365.com/llms.txt)

## Features

| Name | Description |
|------|-------------|
| AP Invoice Automation | Push vendor AP invoices into the customer database with item or GL-account detail. |
| General Ledger Posting | Create balanced journal entries and GL-coded AP invoices via the R365 API. |
| OData Reporting Views | Read-only OData views for transactions, sales, labor, and reference data. |
| Incremental Sync | rowVersion property supports pulling only records changed since the last sync. |
| Audit Tracking | EntityDeleted view exposes records removed from the system for audit reconciliation. |

## Use Cases

| Name | Description |
|------|-------------|
| Vendor Invoice Integration | Suppliers push electronic invoices directly into a restaurant's R365 ledger. |
| BI And Reporting | Pull sales, labor, and financial data into external BI and reporting tools via OData. |
| Payroll Export | Extract labor detail and payroll summary data for downstream payroll processing. |
| Data Warehouse Replication | Replicate transactions and sales into a warehouse using date-range chunked pulls. |

## Integrations

| Name | Description |
|------|-------------|
| Excel | Connect to OData views through the Excel OData feed and R365 Excel plug-in. |
| Business Intelligence Tools | Any OData-compatible BI/reporting tool can consume the OData connector views. |
| POS Systems | POSEmployee and sales views map R365 records to point-of-sale data. |

## Artifacts

- **OpenAPI:** 2 specs (R365 API — 4 operations; OData Connector — 16 operations)
- **JSON Schema:** 6 files
- **JSON Structure:** 4 files
- **JSON-LD:** 2 context files
- **Examples:** 6 request/response pairs
- **Spectral Rules:** rules/restaurant365-rules.yml
- **Naftiko Capabilities:** 9 self-contained capability files (REST + MCP exposers)
- **Vocabulary:** vocabulary/restaurant365-vocabulary.yml
- **Plans / Rate Limits / FinOps:** API Commons + FinOps Framework artifacts

## Maintainers

- Kin Lane (kin@apievangelist.com)

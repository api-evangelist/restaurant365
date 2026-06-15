# Restaurant365 (restaurant365)

Restaurant365 is a cloud-based restaurant accounting, inventory, and operations platform serving thousands of restaurant locations across the United States. Its developer offering centers on the R365 API, which lets approved third-party vendors and partners connect to a customer's R365 database to retrieve data and create or push records such as AP invoices and general ledger entries. A complementary OData connector exposes sales, transaction, location, GL account, employee, and labor data for use in external reporting and business-intelligence tools. API access is provisioned per customer through R365 Support, with bearer-token authentication on the R365 API and Domain\Username basic authentication on the OData connector.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/restaurant365/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/restaurant365/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Restaurant
- Accounting
- Inventory
- Operations
- Invoices
- Reporting
- OData

## Timestamps

- **Created:** 2026-06-02
- **Modified:** 2026-06-03

## APIs

### R365 API

The R365 API lets approved third-party services and vendors connect to a Restaurant365 customer database to retrieve data and create or push records, including AP invoices, GL-coded AP invoices, and general ledger journal entries. A username and password are first exchanged at /APIv1/Authenticate for a bearer token, which is then sent on every subsequent request. Access is provisioned per customer by contacting R365 Support to enable a vendor.

- **Human URL:** [https://docs.restaurant365.com/docs/r365-api](https://docs.restaurant365.com/docs/r365-api)
- **Base URL:** `https://yourcompany.restaurant365.com`

#### Tags

- Invoices
- General Ledger
- Accounting

#### Properties

- [Documentation](https://docs.restaurant365.com/docs/r365-api)
- [Documentation](https://docs.restaurant365.com/docs/r365-api-connector)
- [OpenAPI](openapi/restaurant365-r365-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/restaurant365-r365-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/restaurant365-r365-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authentication](https://docs.restaurant365.com/docs/r365-api-connector)
- [JSON Schema](json-schema/r365-api-ap-invoice-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/r365-api-journal-entry-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/r365-api-ap-invoice-structure.json)
- [JSON Structure](json-structure/r365-api-journal-entry-structure.json)
- [JSON-LD](json-ld/restaurant365-r365-api-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/r365-api-authenticate-example.json)
- [Example](examples/r365-api-create-ap-invoices-example.json)
- [Example](examples/r365-api-create-ap-invoices-gl-example.json)
- [Example](examples/r365-api-create-journal-entries-example.json)

### Restaurant365 OData Connector

The Restaurant365 OData connector exposes R365 data to OData-compatible reporting and BI tools through read-only views for companies, locations, GL accounts, items, job titles, employees, POS employees, labor detail, payroll summary, transactions, transaction detail, sales, and deleted entities. Most views support $filter, $orderby, $select, $skip, and $top. Sales views are limited to a 31-day date range per request and do not support $select or $count.

- **Human URL:** [https://docs.restaurant365.com/docs/restaurant365-odata-connector](https://docs.restaurant365.com/docs/restaurant365-odata-connector)
- **Base URL:** `https://odata.restaurant365.net/api/v2/views/`

#### Tags

- OData
- Reporting
- Sales

#### Properties

- [Documentation](https://docs.restaurant365.com/docs/restaurant365-odata-connector)
- [OpenAPI](openapi/restaurant365-odata-connector-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/restaurant365-odata-connector.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/restaurant365-odata-connector.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Authentication](https://docs.restaurant365.com/docs/restaurant365-odata-connector)
- [JSON Schema](json-schema/odata-connector-transaction-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/odata-connector-sales-employee-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/odata-connector-gl-account-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/odata-connector-employee-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/odata-connector-transaction-structure.json)
- [JSON Structure](json-structure/odata-connector-sales-employee-structure.json)
- [JSON-LD](json-ld/restaurant365-odata-connector-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/odata-connector-list-transactions-example.json)
- [Example](examples/odata-connector-list-sales-employee-example.json)

## Common Properties

- [Website](https://www.restaurant365.com)
- [Documentation](https://docs.restaurant365.com/docs/r365-api)
- [Pricing](https://www.restaurant365.com/pricing/)
- [Plans](plans/restaurant365-plans-pricing.yml)
- [Rate Limits](rate-limits/restaurant365-rate-limits.yml)
- [Spectral Rules](rules/restaurant365-rules.yml)
- [Vocabulary](vocabulary/restaurant365-vocabulary.yml)
- [Blog](https://www.restaurant365.com/blog/)
- [GitHub Organization](https://github.com/restaurant365)
- [LinkedIn](https://www.linkedin.com/company/restaurant365-cloud-erp-for-restaurants)
- [L L Ms Txt](https://docs.restaurant365.com/llms.txt)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

# Restaurant365 (restaurant365)

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

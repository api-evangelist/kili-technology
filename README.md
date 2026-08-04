# Kili Technology (kili-technology)

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

Kili Technology is a training-data and data-labeling platform for building high-quality datasets for machine learning and LLMs. Its labeling application is fully programmable through a single GraphQL API (and a Python SDK) covering projects, assets, labels, issues, and users at https://cloud.kili-technology.com/api/label/v2/graphql.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kili-technology/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kili-technology/refs/heads/main/apis.yml)

## Tags

- AI
- Data Labeling
- Training Data
- Annotation
- GraphQL

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Kili Technology Projects API

Create, read, update, copy, and count annotation projects via the GraphQL fields projects, countProjects, createProject, copyProject, and updatePropertiesInProject, including job/ontology configuration.

- **Human URL:** [https://docs.kili-technology.com/reference/graphql-api](https://docs.kili-technology.com/reference/graphql-api)
- **Base URL:** `https://cloud.kili-technology.com/api/label/v2/graphql`

#### Tags

- Projects
- GraphQL
- Annotation

#### Properties

- [Documentation](https://docs.kili-technology.com/docs/managing-projects)
- [API Reference](https://docs.kili-technology.com/reference/graphql-api)
- [OpenAPI](openapi/kili-technology-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GraphQL](graphql/kili-technology-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [Postman Collection](collections/kili-technology.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kili-technology.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kili Technology Assets API

Import and manage data to annotate (images, text, documents, video, geospatial) via assets, countAssets, and appendManyAssets, with external-id filtering and project scoping.

- **Human URL:** [https://docs.kili-technology.com/reference/graphql-api](https://docs.kili-technology.com/reference/graphql-api)
- **Base URL:** `https://cloud.kili-technology.com/api/label/v2/graphql`

#### Tags

- Assets
- GraphQL
- Import

#### Properties

- [Documentation](https://docs.kili-technology.com/docs/importing-data)
- [API Reference](https://docs.kili-technology.com/reference/graphql-api)
- [OpenAPI](openapi/kili-technology-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GraphQL](graphql/kili-technology-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [Postman Collection](collections/kili-technology.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kili-technology.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kili Technology Labels API

Create, append, count, export, and copy annotation labels and predictions via labels, countLabels, appendManyLabels, appendToLabels, createHoneypot, and copyLabels, plus a labelCreatedOrUpdated GraphQL subscription over WebSocket.

- **Human URL:** [https://docs.kili-technology.com/reference/graphql-api](https://docs.kili-technology.com/reference/graphql-api)
- **Base URL:** `https://cloud.kili-technology.com/api/label/v2/graphql`

#### Tags

- Labels
- GraphQL
- Annotations

#### Properties

- [Documentation](https://docs.kili-technology.com/docs/exporting-project-data)
- [API Reference](https://docs.kili-technology.com/reference/graphql-api)
- [OpenAPI](openapi/kili-technology-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GraphQL](graphql/kili-technology-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [AsyncAPI](asyncapi/kili-technology-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/kili-technology.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kili-technology.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kili Technology Issues API

Create, count, list, and resolve review issues and questions on assets and labels via createIssues, countIssues, issues, and updatePropertiesInIssue for quality workflows.

- **Human URL:** [https://docs.kili-technology.com/reference/graphql-api](https://docs.kili-technology.com/reference/graphql-api)
- **Base URL:** `https://cloud.kili-technology.com/api/label/v2/graphql`

#### Tags

- Issues
- GraphQL
- Review

#### Properties

- [Documentation](https://docs.kili-technology.com/docs/quality-management)
- [API Reference](https://docs.kili-technology.com/reference/graphql-api)
- [OpenAPI](openapi/kili-technology-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GraphQL](graphql/kili-technology-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [Postman Collection](collections/kili-technology.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kili-technology.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kili Technology Users API

Manage organization users and the current viewer via users, countUsers, viewer (me), createUser, updatePropertiesInUser, and password reset mutations.

- **Human URL:** [https://docs.kili-technology.com/reference/graphql-api](https://docs.kili-technology.com/reference/graphql-api)
- **Base URL:** `https://cloud.kili-technology.com/api/label/v2/graphql`

#### Tags

- Users
- GraphQL
- Access Management

#### Properties

- [Documentation](https://docs.kili-technology.com/docs/user-management)
- [API Reference](https://docs.kili-technology.com/reference/graphql-api)
- [OpenAPI](openapi/kili-technology-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GraphQL](graphql/kili-technology-graphql.md) — [GraphQL Specification](https://spec.graphql.org/)
- [Postman Collection](collections/kili-technology.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kili-technology.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/kili-technology)
- [LinkedIn](https://www.linkedin.com/company/kili-technology)
- [Website](https://kili-technology.com)
- [Documentation](https://docs.kili-technology.com)
- [Plans](plans/kili-technology-plans-pricing.yml)
- [Rate Limits](rate-limits/kili-technology-rate-limits.yml)
- [Fin Ops](finops/kili-technology-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com

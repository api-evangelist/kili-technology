# Kili Technology (kili-technology)

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

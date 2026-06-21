# Kili Technology GraphQL API

GraphQL interface for the [Kili Technology](https://kili-technology.com) training-data and
data-labeling platform. The entire labeling application is programmable through a single
GraphQL endpoint, which is also what the official
[Kili Python SDK](https://github.com/kili-technology/kili-python-sdk) wraps.

- GraphQL API reference: <https://docs.kili-technology.com/reference/graphql-api>
- Python SDK docs: <https://python-sdk-docs.kili-technology.com>
- GitHub: <https://github.com/kili-technology/kili-python-sdk>

---

## Endpoint

```
POST https://cloud.kili-technology.com/api/label/v2/graphql
```

A single GraphQL endpoint serves all queries, mutations, and subscriptions. Self-managed
(on-premise / dedicated) deployments expose the same path under their own host, configurable
via the `KILI_API_ENDPOINT` environment variable.

| Transport | URL |
|-----------|-----|
| HTTP (queries + mutations) | `https://cloud.kili-technology.com/api/label/v2/graphql` |
| WebSocket (subscriptions) | `wss://cloud.kili-technology.com/api/label/v2/graphql` |

---

## Authentication

Kili authenticates with an **API key** created in the Kili interface (Settings → API KEY) and
sent in the `Authorization` header. Note Kili's documented header format embeds the
`X-API-Key:` token inside the `Authorization` value:

```
Authorization: X-API-Key: <YOUR_API_KEY>
Content-Type: application/json
Accept: application/json
```

The Python SDK reads the key from the `KILI_API_KEY` environment variable or
`Kili(api_key="<YOUR_API_KEY>")`.

Responses may include an `x-complexity` header reflecting the cost of the executed query;
clients should page large result sets (`first` / `skip`) to stay within complexity limits.

---

## Domains

| Domain | Key fields |
|--------|------------|
| Projects | `projects`, `countProjects`, `createProject`, `copyProject`, `updatePropertiesInProject` |
| Assets | `assets`, `countAssets`, `appendManyAssets` |
| Labels | `labels`, `countLabels`, `appendManyLabels`, `appendToLabels`, `createHoneypot`, `copyLabels`, `deleteLabels` |
| Issues | `issues`, `countIssues`, `createIssues`, `updatePropertiesInIssue` |
| Users | `users`, `countUsers`, `viewer` (alias `me`), `createUser`, `updatePropertiesInUser`, `updatePassword`, `resetPassword` |

See [`kili-technology-schema.graphql`](./kili-technology-schema.graphql) for a representative
SDL subset of these types and operations.

---

## Query examples

### List projects

```graphql
query projects($where: ProjectWhere!, $first: PageSize!, $skip: Int!) {
  data: projects(where: $where, first: $first, skip: $skip) {
    id
    title
    description
    numberOfAssets
    numberOfRemainingAssets
    jsonInterface
  }
}
```

Variables:

```json
{ "where": { "id": "your-project-id" }, "first": 10, "skip": 0 }
```

### Count assets in a project

```graphql
query countAssets($where: AssetWhere!) {
  data: countAssets(where: $where)
}
```

```json
{ "where": { "project": { "id": "your-project-id" } } }
```

### List labels for a project

```graphql
query labels($where: LabelWhere!, $first: PageSize!, $skip: Int!) {
  data: labels(where: $where, first: $first, skip: $skip) {
    id
    labelType
    jsonResponse
    createdAt
    author { id email }
    labelOf { id externalId }
  }
}
```

```json
{ "where": { "project": { "id": "your-project-id" } }, "first": 100, "skip": 0 }
```

### Current user

```graphql
query me {
  data: viewer {
    id
    email
    firstname
    lastname
  }
}
```

---

## Mutation examples

### Create a project

```graphql
mutation($data: CreateProjectData!) {
  data: createProject(data: $data) {
    id
  }
}
```

```json
{
  "data": {
    "title": "My labeling project",
    "description": "Image bounding boxes",
    "inputType": "IMAGE",
    "jsonInterface": "{\"jobs\": {}}"
  }
}
```

### Import assets

```graphql
mutation appendManyAssets($data: AppendManyAssetsData!, $where: ProjectWhere!) {
  data: appendManyAssets(data: $data, where: $where) {
    id
  }
}
```

### Append labels

```graphql
mutation appendManyLabels($data: AppendManyLabelsData!, $where: AssetWhere!) {
  data: appendManyLabels(data: $data, where: $where) {
    id
  }
}
```

### Create review issues

```graphql
mutation createIssues($issues: [IssueToCreate!]!, $where: AssetWhere!) {
  data: createIssues(issues: $issues, where: $where) {
    id
  }
}
```

---

## Subscription example

Kili exposes a real GraphQL subscription over WebSocket that fires whenever a label is created
or updated in a project. The SDK connects by switching the endpoint scheme from `http` to `ws`.

```graphql
subscription($projectID: ID!) {
  data: labelCreatedOrUpdated(projectID: $projectID) {
    id
    labelType
    jsonResponse
    author { email }
    labelOf { id }
  }
}
```

```json
{ "projectID": "your-project-id" }
```

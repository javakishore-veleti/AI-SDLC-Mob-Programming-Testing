# API Contract Template

## API Name

```text
<API name>
```

## Endpoint

```http
<METHOD> /path/to/resource
```

## Purpose

Describe what this API does and why it exists.

```text

```

---

## Consumers

| Consumer | Purpose |
|---|---|
|  |  |

---

## Authentication and Authorization

| Area | Details |
|---|---|
| Authentication method |  |
| Authorization model |  |
| Required scopes/roles |  |
| Sensitive data involved | Yes / No |
| Rate limits |  |

---

## Request

### Headers

| Header | Required? | Description |
|---|---:|---|
| Authorization | Yes |  |
| Content-Type | Yes | application/json |
| Correlation-Id | Recommended | Traceability |

### Request Body

```json
{

}
```

### Request Field Definitions

| Field | Type | Required? | Description |
|---|---|---:|---|
|  |  |  |  |

---

## Response

### Success Response

```json
{

}
```

### Response Field Definitions

| Field | Type | Description |
|---|---|---|
|  |  |  |

---

## Error Model

| HTTP Status | Error Code | Scenario | Client Action |
|---:|---|---|---|
| 400 |  | Invalid request | Fix request |
| 401 |  | Unauthorized | Re-authenticate |
| 403 |  | Forbidden | Check permissions |
| 404 |  | Not found | Validate resource |
| 409 |  | Conflict | Resolve conflict |
| 429 |  | Rate limited | Retry later |
| 500 |  | Server error | Retry or escalate |

---

## Idempotency

```text
Describe whether the API is idempotent and how duplicate requests are handled.
```

---

## Timeout and Retry Behavior

| Behavior | Details |
|---|---|
| Timeout |  |
| Retry allowed? |  |
| Retry strategy |  |
| Duplicate handling |  |

---

## Observability

| Signal | Details |
|---|---|
| Logs |  |
| Metrics |  |
| Traces |  |
| Correlation ID |  |
| Alerts |  |

---

## Test Scenarios

| Scenario | Input | Expected Result |
|---|---|---|
| Happy path |  |  |
| Invalid request |  |  |
| Unauthorized |  |  |
| Dependency failure |  |  |
| Timeout |  |  |

---

## Open Questions

| Question | Owner | Target Date |
|---|---|---|
|  |  |  |

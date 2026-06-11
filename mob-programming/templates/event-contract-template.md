# Event Contract Template

## Event Name

```text
<event.name>
```

## Purpose

Describe why this event exists and what business or system change it represents.

```text

```

---

## Producer

| Producer System | Owner | Notes |
|---|---|---|
|  |  |  |

---

## Consumers

| Consumer System | Purpose | Owner |
|---|---|---|
|  |  |  |

---

## Event Trigger

Describe what causes this event to be published.

```text

```

---

## Event Payload

```json
{
  "eventId": "",
  "eventType": "",
  "eventVersion": "1.0",
  "eventTimestamp": "",
  "correlationId": "",
  "sourceSystem": "",
  "data": {}
}
```

---

## Field Definitions

| Field | Type | Required? | Description |
|---|---|---:|---|
| eventId | string | Yes | Unique event identifier |
| eventType | string | Yes | Event name |
| eventVersion | string | Yes | Event schema version |
| eventTimestamp | string | Yes | Event creation timestamp |
| correlationId | string | Recommended | End-to-end trace ID |
| sourceSystem | string | Yes | Event producer |
| data | object | Yes | Business payload |

---

## Delivery Semantics

| Area | Decision |
|---|---|
| Delivery model | At-least-once / At-most-once / Exactly-once |
| Ordering required? | Yes / No |
| Idempotency required? | Yes / No |
| Replay supported? | Yes / No |
| DLQ required? | Yes / No |

---

## Error Handling

| Scenario | Expected Handling |
|---|---|
| Invalid payload |  |
| Duplicate event |  |
| Out-of-order event |  |
| Consumer failure |  |
| Downstream dependency failure |  |

---

## Observability

| Signal | Details |
|---|---|
| Event published metric |  |
| Event consumed metric |  |
| Failure metric |  |
| DLQ metric |  |
| Trace correlation |  |
| Alerting |  |

---

## Test Scenarios

| Scenario | Input | Expected Result |
|---|---|---|
| Valid event |  |  |
| Duplicate event |  |  |
| Invalid event |  |  |
| Consumer failure |  |  |
| Replay event |  |  |

---

## Open Questions

| Question | Owner | Target Date |
|---|---|---|
|  |  |  |

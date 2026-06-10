# Inventory Synchronization

## Objective

Design reliable inventory synchronization between Shopify and external systems such as ERP, WMS, and OMS platforms.

## AI-SDLC Focus

Use this reference during event storming, integration design, failure-mode analysis, and testing strategy sessions.

## Systems

- Shopify
- ERP
- WMS
- OMS
- Middleware event bus
- Inventory Sync Service

## Event Flow

```text
Inventory Updated
  -> Middleware Event
  -> Inventory Sync Service
  -> Shopify Inventory Update
  -> Reconciliation Job
```

## Architecture Considerations

- Source of truth
- Event ordering
- Idempotency
- Retry policies
- Dead-letter queues
- Reconciliation strategy
- Backorder rules
- Safety stock rules
- Multi-location inventory

## API / Event Contract Template

```json
{
  "eventId": "evt_123",
  "sku": "SKU-001",
  "locationId": "loc_001",
  "availableQuantity": 25,
  "sourceSystem": "ERP",
  "eventTimestamp": "2026-06-10T10:00:00Z"
}
```

## Mob Programming Discussion Questions

- Which system is the inventory source of truth?
- How often should reconciliation run?
- What is the oversell prevention strategy?
- How are partial updates handled?
- How do we handle duplicate events?
- How do we recover from failed Shopify updates?
- What observability is required?

## Test Scenarios

| Scenario | Expected Result |
|---|---|
| Inventory increases | Shopify is updated |
| Inventory decreases | Shopify is updated without oversell |
| Duplicate event received | Event is ignored safely |
| Out-of-order event received | Latest valid state wins |
| Shopify API fails | Retry and DLQ are triggered |
| ERP downtime | Sync pauses or degrades safely |
| Reconciliation detects mismatch | Correction event is generated |

## Edge Cases

- Oversell due to delayed sync
- Partial inventory updates
- Network failures
- Duplicate webhooks
- Location mapping errors
- SKU mapping errors
- Inventory reservations during checkout

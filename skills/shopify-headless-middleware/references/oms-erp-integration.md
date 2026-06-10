# OMS ERP Integration

## Objective

Facilitate architecture workshops and AI-SDLC planning for OMS and ERP integrations connected to Shopify Headless commerce.

## Integration Domains

- Orders
- Fulfillment
- Inventory
- Pricing
- Returns
- Refunds
- Customer data
- Tax and invoices

## Architecture Pattern

```text
Shopify
  -> Middleware Integration Layer
  -> OMS
  -> ERP
```

## Core Design Principles

- Use idempotent APIs
- Preserve source-system traceability
- Use event-driven workflows where possible
- Provide retry and dead-letter handling
- Separate business validation from transport concerns
- Log correlation IDs across systems

## API Design Checklist

- Authentication
- Idempotency key
- Error handling
- Retry logic
- Rate limiting
- Observability
- Payload versioning
- System ownership
- Reconciliation process

## Example Order Event

```json
{
  "eventId": "evt_order_123",
  "orderId": "shopify_order_1001",
  "source": "Shopify",
  "target": "OMS",
  "eventType": "ORDER_CREATED",
  "timestamp": "2026-06-10T10:00:00Z"
}
```

## Mob Programming Discussion Questions

- Which system owns the order lifecycle?
- Which system owns fulfillment status?
- How are refunds synchronized?
- What happens when ERP is unavailable?
- Which events need guaranteed delivery?
- Which failures require manual intervention?
- What reconciliation reports are required?

## Test Scenarios

| Scenario | Expected Result |
|---|---|
| Order created in Shopify | Order is sent to OMS |
| OMS accepts order | Middleware records success |
| ERP is down | Event is retried or queued |
| Duplicate order event | Duplicate is ignored safely |
| Shipment update received | Shopify fulfillment is updated |
| Refund created | ERP and Shopify are synchronized |
| Partial fulfillment | Correct line items are updated |

## Edge Cases

- Duplicate order creation
- ERP downtime
- OMS partial failure
- Refund mismatch
- Fulfillment split across warehouses
- Customer data mismatch
- Tax or invoice sync failure

# Discount Segmentation

## Objective

Design customer-specific discounting for Shopify Headless architectures across guest and logged-in customer journeys.

## AI-SDLC Focus

Use this reference during requirements discovery, architecture design, API planning, test strategy, and mob programming sessions.

## Customer Segments

| Customer Type | Possible Discount Strategy |
|---|---|
| Guest | Welcome discount, email capture discount, first-session offer |
| Logged-in | Loyalty discount, customer-specific offer |
| VIP | Higher-tier discount |
| Wholesale | Contract pricing or custom price list |
| Employee | Employee discount |
| First-time buyer | First-order promotion |
| Returning customer | Retention or win-back offer |

## Architecture Pattern

```text
Identity Service
  -> Customer Context Service
  -> Segmentation Service
  -> Discount Rules Engine
  -> Cart Pricing Service
  -> Checkout Integration
```

## Example API

```http
POST /discount/evaluate
```

## Guest Request

```json
{
  "isAuthenticated": false,
  "cartId": "cart_123",
  "cartValue": 150,
  "market": "US"
}
```

## Guest Response

```json
{
  "customerType": "GUEST",
  "eligibleDiscounts": [
    {
      "code": "WELCOME5",
      "type": "percentage",
      "value": 5,
      "stackable": true
    }
  ]
}
```

## Logged-In Request

```json
{
  "isAuthenticated": true,
  "customerId": "1001",
  "cartId": "cart_456",
  "cartValue": 250,
  "market": "US"
}
```

## Logged-In Response

```json
{
  "customerType": "VIP",
  "eligibleDiscounts": [
    {
      "code": "VIP20",
      "type": "percentage",
      "value": 20,
      "stackable": false
    }
  ]
}
```

## Rule Template

```text
Rule Name:
Customer Type:
Eligibility Criteria:
Discount Type:
Discount Value:
Stacking Policy:
Exclusions:
Expiration:
Shopify Dependency:
Middleware Dependency:
Frontend Display Behavior:
Test Scenarios:
```

## Example Rules

```text
IF customer is guest
AND cart value >= 100
THEN apply WELCOME5
```

```text
IF customer is logged in
AND customer tag = VIP
THEN apply VIP20
```

```text
IF customer is logged in
AND customer tag = WHOLESALE
THEN use contract pricing instead of promotional discount
```

## Mob Programming Discussion Questions

- How do we identify guest vs logged-in customers?
- Which discounts are evaluated in middleware vs Shopify?
- Which rules are configured by business users?
- Can discounts stack with Shopify-native promotions?
- What happens when a guest logs in after a discount is applied?
- Should the frontend show potential savings before login?
- How do we avoid stale customer segmentation?

## Test Scenarios

| Scenario | Expected Result |
|---|---|
| Guest cart qualifies for welcome discount | WELCOME5 is returned |
| Logged-in VIP qualifies | VIP20 is returned |
| Wholesale customer qualifies | Contract pricing overrides promo discount |
| Guest logs in during checkout | Discount is re-evaluated |
| Discount expires | Discount is removed or rejected |
| Shopify API fails | Middleware returns safe fallback |
| Cache is stale | Revalidation is triggered |

## Edge Cases

- Guest becomes logged in during checkout
- Discount changes after cart creation
- Customer tag changes in Shopify
- Shopify API rate limit
- Expired discount code
- Multiple discounts conflict
- Discount allowed on PDP but rejected at checkout
- Currency or market-specific discount rules
- Cache has stale customer segment
- Customer logs out after discount evaluation

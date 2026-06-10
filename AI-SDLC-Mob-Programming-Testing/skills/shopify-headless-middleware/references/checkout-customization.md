# Checkout Customization

## Objective

Guide AI-SDLC and mob programming sessions for Shopify checkout customization, validation, and integration workflows.

## Focus Areas

- Shopify Functions
- Discount validation
- Shipping customization
- Payment customization
- Tax integration
- Fraud checks
- Checkout extension points
- Middleware-to-checkout handoff

## Architecture Pattern

```text
Headless Storefront
  -> Cart Service
  -> Pricing / Discount Service
  -> Checkout Preparation Service
  -> Shopify Checkout
  -> Payment / Tax / Fulfillment Systems
```

## Discovery Questions

- Which checkout steps need customization?
- Which rules must execute before checkout?
- Which rules must execute inside Shopify?
- What data must be passed from middleware to checkout?
- What happens if middleware and Shopify calculate different totals?
- What is the fallback behavior if an external dependency fails?

## API Design Checklist

- Checkout preparation endpoint
- Cart validation endpoint
- Discount validation endpoint
- Shipping eligibility endpoint
- Payment eligibility endpoint
- Error response model
- Observability and trace ID strategy

## Example Endpoint

```http
POST /checkout/prepare
```

## Example Response

```json
{
  "cartId": "cart_123",
  "checkoutReady": true,
  "warnings": [],
  "appliedDiscounts": ["WELCOME5"],
  "estimatedTotal": 125.35
}
```

## Mob Programming Participants

- Product Owner
- Shopify Architect
- Middleware/API Developer
- Frontend Developer
- QA Engineer
- DevOps/SRE Engineer
- Payment or tax specialist when relevant

## Test Scenarios

| Scenario | Expected Result |
|---|---|
| Guest checkout | Checkout is created successfully |
| Logged-in checkout | Customer context is applied |
| Discount conflict | Conflict is resolved before checkout |
| Payment method unavailable | User sees eligible alternatives |
| Shipping restriction | Checkout blocks invalid shipping path |
| Middleware timeout | Safe fallback is used |
| Shopify checkout rejects discount | Error is surfaced clearly |

## Edge Cases

- Discount valid in cart but invalid at checkout
- Customer changes address after shipping rules are evaluated
- Payment provider outage
- Tax recalculation changes final total
- Currency changes between cart and checkout
- Checkout abandoned and resumed later

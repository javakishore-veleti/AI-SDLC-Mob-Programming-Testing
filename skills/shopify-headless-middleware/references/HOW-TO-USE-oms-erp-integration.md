# How to Use: OMS ERP Integration Reference

## File This Guide Supports

```text
skills/shopify-headless-middleware/references/oms-erp-integration.md
```

This guide explains how to use the `oms-erp-integration.md` reference during an **AI-SDLC Mob Programming** session for Shopify Headless middleware teams.

The focus is specific:

```text
OMS and ERP integration for orders, fulfillment, inventory,
refunds, customer data, pricing, invoices, and system synchronization
```

This is not a traditional SDLC handoff document. It is a working guide for a live collaborative session where the team designs integration behavior, reliability, testing, and implementation together.

---

## Why This Reference Exists

Use `oms-erp-integration.md` to help the team design integrations between Shopify, middleware, OMS, and ERP platforms.

The reference helps the team produce working decisions around:

- Order flow
- Fulfillment updates
- Refund synchronization
- Inventory and pricing ownership
- Customer data synchronization
- Idempotency
- Error handling
- Retry and dead-letter behavior
- Reconciliation
- Observability
- Test scenarios and edge cases

---

## Recommended Usage Model

```text
GitHub Repository = Source of Truth
GitHub Copilot = AI Harness inside the IDE
VS Code = Working environment
SKILL.md = Main skill instruction file
oms-erp-integration.md = Use-case-specific reference
```

Keep this reference in GitHub so Copilot can use it as local repo context during integration design.

---

## Required Tools

| Tool | Purpose |
|---|---|
| GitHub Repository | Source of truth for integration references and generated artifacts |
| GitHub Copilot Chat | Use this reference as repo context inside VS Code |
| VS Code | Recommended development environment |
| Shopify Admin | Review orders, fulfillment, customers, products, refunds, and inventory behavior |
| Shopify Developer App | Review API scopes and app configuration |
| OMS Sandbox | Validate order lifecycle and fulfillment behavior |
| ERP Sandbox | Validate finance, invoice, inventory, customer, or pricing behavior |
| Event Bus / Queue Tool | Review integration events, retries, DLQ, and replay behavior |
| Postman / Insomnia | Test integration APIs |
| Observability Tool | Review integration errors, latency, traces, retries, and alerts |
| Jira / Azure DevOps / GitHub Issues | Convert outcomes into backlog-ready work items |
| Miro / Lucidchart / Draw.io | Capture integration flows and system ownership diagrams |

---

## Required Logins and Access

| Access | Why It Is Needed |
|---|---|
| GitHub repository access | Read and update integration playbooks, API contracts, and test scenarios |
| GitHub Copilot access | Use repo context during the mob session |
| Shopify Admin access | Review order, fulfillment, inventory, refund, and customer behavior |
| Shopify Developer App access | Confirm API scopes, app permissions, and token configuration |
| OMS sandbox access | Validate order management workflows |
| ERP sandbox access | Validate finance, invoice, customer, inventory, or pricing workflows |
| Middleware API environment access | Test integration APIs and event handlers |
| Queue / Event bus access | Review event delivery, retries, DLQ, and replay behavior |
| Observability dashboard access | Validate monitoring, alerts, traces, and operational risks |
| Jira / Azure DevOps / GitHub Issues access | Create epics, stories, tasks, and test cases |

---

## Scope of This Mob Session

### In Scope

- Shopify to OMS order creation
- OMS to Shopify fulfillment updates
- Shopify / OMS / ERP refund synchronization
- Customer data synchronization
- Inventory and pricing ownership discussion
- Integration event contracts
- Idempotency strategy
- Retry and DLQ behavior
- Reconciliation strategy
- Observability requirements
- Test scenarios and edge cases

### Out of Scope

- Full ERP implementation
- Full OMS implementation
- Full storefront redesign
- Discount campaign design
- Checkout UI redesign
- Payment gateway implementation
- Warehouse process redesign

---

## Shopify API / App Scopes to Review

Confirm final scope names based on Shopify app type and API version.

| Scope | Purpose |
|---|---|
| `read_orders` | Read Shopify orders for OMS / ERP integration |
| `write_orders` | Update orders when required by integration behavior |
| `read_fulfillments` | Read fulfillment status and details |
| `write_fulfillments` | Update fulfillment status back into Shopify |
| `read_customers` | Synchronize customer data |
| `read_inventory` | Support inventory-related integration workflows |
| `write_inventory` | Update inventory if integration owns inventory sync |
| `read_products` | Map SKUs, products, and variants |
| `read_discounts` | Understand promotion context on orders when required |
| Refund-related access | Support refund synchronization where applicable |

Important: The mob should decide which system owns each domain before deciding write access.

---

## Ideal Mob Programming Roles

| Role | Responsibility in This Session |
|---|---|
| Product Owner | Defines business outcomes and operational success criteria |
| Shopify Architect | Validates Shopify order, fulfillment, refund, customer, and API constraints |
| Middleware / Integration Developer | Designs APIs, events, idempotency, retries, and integration flows |
| OMS SME | Explains OMS order lifecycle, fulfillment, cancellation, and return behavior |
| ERP SME | Explains ERP finance, invoice, inventory, customer, and pricing constraints |
| QA Engineer | Creates integration, failure-mode, and reconciliation test scenarios |
| DevOps / SRE Engineer | Reviews queue behavior, retries, DLQ, observability, and alerting |
| Security Engineer | Reviews tokens, credentials, PII, customer data, and system access |
| Support / Operations Lead | Defines manual intervention and exception handling workflows |
| Mob Facilitator | Keeps the session focused and captures decisions |
| AI Pair / Copilot Operator | Uses Copilot to generate artifacts from repo context |

---

## How to Use With GitHub Copilot

Open the repository in VS Code.

Open this file:

```text
skills/shopify-headless-middleware/references/oms-erp-integration.md
```

Then use GitHub Copilot Chat:

```text
Use the open file oms-erp-integration.md as context.

Act as an AI-SDLC mob programming assistant for a Shopify Headless middleware team.

Help us run a mob session for Shopify OMS and ERP integration.

Generate:
- required tools
- required logins
- required Shopify scopes to review
- ideal mob roles
- session scope
- system ownership decisions
- order and fulfillment flow
- integration API/event contracts
- idempotency strategy
- retry and DLQ strategy
- reconciliation approach
- edge cases
- test scenario matrix
- expected session outcomes
- implementation checklist
```

---

## Recommended Mob Session Flow

### 1. Confirm Integration Business Intent

Answer:

- What business process are we integrating?
- Which systems are involved?
- What is the expected operational outcome?
- Which system owns order status?
- Which system owns fulfillment status?
- Which system owns refunds, invoices, inventory, and customer records?

### 2. Define System Ownership

Capture ownership for:

| Domain | Owner |
|---|---|
| Order creation | Shopify / OMS / Middleware |
| Fulfillment status | OMS / WMS / Shopify |
| Refunds | Shopify / OMS / ERP |
| Inventory | Shopify / ERP / WMS / OMS |
| Pricing | Shopify / ERP / Middleware |
| Customer data | Shopify / ERP / CRM |

### 3. Map Integration Flow

Start with:

```text
Shopify
  -> Middleware Integration Layer
  -> OMS
  -> ERP
```

Then expand by event:

- Order created
- Order accepted
- Fulfillment created
- Shipment updated
- Refund created
- Invoice generated
- Inventory adjusted

### 4. Define Event / API Contract

The mob should define:

- Event ID
- Source system
- Target system
- Event type
- Payload version
- Idempotency key
- Correlation ID
- Error model
- Retry policy
- Manual intervention policy

### 5. Define Reliability Strategy

Answer:

- What happens when OMS is down?
- What happens when ERP is down?
- What events require guaranteed delivery?
- What events can be retried safely?
- What goes to DLQ?
- What requires manual support action?
- What reconciliation reports are required?

### 6. Generate Test Scenarios During the Session

Create tests for:

- Order creation
- Duplicate order event
- OMS accepts order
- OMS rejects order
- ERP downtime
- Partial fulfillment
- Shipment update
- Refund synchronization
- Customer data mismatch
- Inventory mismatch
- Retry and DLQ replay
- Manual intervention workflow

---

## Expected Outcomes

By the end of the mob session, the team should have:

- System ownership matrix
- Integration flow diagram
- Event/API contract
- Idempotency strategy
- Retry and DLQ strategy
- Reconciliation approach
- Shopify dependency list
- Required API scopes to review
- Security and access considerations
- Observability and alerting requirements
- Integration test scenario matrix
- Backlog-ready implementation checklist

---

## Repo-Ready Artifacts to Produce

```text
domains/shopify-headless/architecture/oms-erp-integration-flow.md
domains/shopify-headless/architecture/oms-erp-event-contract.md
domains/shopify-headless/testing/oms-erp-test-scenarios.md
domains/shopify-headless/use-cases/oms-erp-edge-cases.md
domains/shopify-headless/use-cases/oms-erp-implementation-checklist.md
```

---

## Definition of Done for the Mob Session

The session is complete when the team has:

- Agreed on system ownership
- Designed integration flow
- Defined event/API contract
- Captured idempotency strategy
- Captured retry and DLQ strategy
- Captured reconciliation approach
- Identified Shopify scopes to review
- Captured test scenarios and edge cases
- Created backlog-ready implementation items

# How to Use: Inventory Synchronization Reference

## File This Guide Supports

```text
skills/shopify-headless-middleware/references/inventory-sync.md
```

This guide explains how to use the `inventory-sync.md` reference during an **AI-SDLC Mob Programming** session for Shopify Headless middleware teams.

The focus is specific:

```text
Inventory synchronization between Shopify and external systems
such as ERP, OMS, WMS, warehouse platforms, and middleware event services
```

This is not a traditional SDLC handoff document. It is a working guide for a live collaborative session where the team designs reliability, failure handling, testing, and implementation together.

---

## Why This Reference Exists

Use `inventory-sync.md` to help the team design reliable inventory movement across Shopify and external systems.

The reference helps the team produce working decisions around:

- Inventory source of truth
- Event-driven inventory updates
- SKU and location mapping
- Idempotency
- Retry and dead-letter handling
- Reconciliation jobs
- Oversell prevention
- Multi-location inventory
- Test scenarios and edge cases

---

## Recommended Usage Model

```text
GitHub Repository = Source of Truth
GitHub Copilot = AI Harness inside the IDE
VS Code = Working environment
SKILL.md = Main skill instruction file
inventory-sync.md = Use-case-specific reference
```

Keep this reference in GitHub so Copilot can use it as local repo context during mob programming.

---

## Required Tools

| Tool | Purpose |
|---|---|
| GitHub Repository | Source of truth for inventory references and generated artifacts |
| GitHub Copilot Chat | Use this reference as repo context inside VS Code |
| VS Code | Recommended development environment |
| Shopify Admin | Review products, variants, inventory locations, and stock behavior |
| Shopify Developer App | Review inventory-related API scopes and app configuration |
| ERP / OMS / WMS Sandbox | Validate external inventory source behavior |
| Event Bus / Queue Tool | Review inventory event flow, retries, and DLQ handling |
| Postman / Insomnia | Test inventory sync APIs |
| Observability Tool | Review sync failures, latency, retries, and inventory mismatch alerts |
| Jira / Azure DevOps / GitHub Issues | Convert outcomes into backlog-ready work items |
| Miro / Lucidchart / Draw.io | Capture inventory sequence and system diagrams |

---

## Required Logins and Access

| Access | Why It Is Needed |
|---|---|
| GitHub repository access | Read and update inventory playbooks, API contracts, and test scenarios |
| GitHub Copilot access | Use repo context during the mob session |
| Shopify Admin access | Validate products, variants, SKUs, inventory locations, and inventory state |
| Shopify Developer App access | Confirm app permissions, API scopes, and token configuration |
| ERP / OMS / WMS sandbox access | Validate external source system behavior |
| Middleware API environment access | Test inventory sync APIs and event handlers |
| Queue / Event bus access | Review event ordering, retries, DLQ, and replay behavior |
| Observability dashboard access | Validate monitoring, alerts, sync failures, and reconciliation |
| Jira / Azure DevOps / GitHub Issues access | Create epics, stories, tasks, and test cases |

---

## Scope of This Mob Session

### In Scope

- Inventory source of truth
- Shopify inventory update flow
- External ERP / OMS / WMS inventory events
- SKU mapping
- Location mapping
- Multi-location inventory
- Idempotency strategy
- Retry and DLQ behavior
- Reconciliation strategy
- Oversell prevention
- Test scenarios and edge cases

### Out of Scope

- Full ERP implementation
- Full OMS implementation
- Full warehouse process redesign
- Product catalog redesign
- Payment or checkout customization
- Discount segmentation
- Full deployment automation

---

## Shopify API / App Scopes to Review

Confirm final scope names based on Shopify app type and API version.

| Scope | Purpose |
|---|---|
| `read_products` | Read products, variants, and SKU data |
| `write_products` | Update product or variant data if required |
| `read_inventory` | Read inventory levels and inventory items |
| `write_inventory` | Update inventory levels where middleware owns sync |
| `read_locations` | Read Shopify inventory locations |
| `read_orders` | Understand inventory reservation or order-driven inventory impacts |
| Webhook/event access | Support inventory, product, or order event handling where applicable |

Important: The mob should confirm which system is the source of truth before deciding write access.

---

## Ideal Mob Programming Roles

| Role | Responsibility in This Session |
|---|---|
| Product Owner | Defines inventory accuracy goals and business impact |
| Shopify Architect | Validates Shopify inventory model, locations, and API constraints |
| Middleware / Integration Developer | Designs sync APIs, event handlers, idempotency, and retries |
| ERP / OMS / WMS SME | Explains external inventory source behavior and constraints |
| QA Engineer | Creates inventory sync and failure-mode test scenarios |
| DevOps / SRE Engineer | Reviews queue behavior, retries, DLQ, observability, and alerts |
| Data / Reporting Analyst | Helps define reconciliation reports and mismatch detection |
| Security Engineer | Reviews system credentials, tokens, and data exposure |
| Mob Facilitator | Keeps the session focused and captures decisions |
| AI Pair / Copilot Operator | Uses Copilot to generate artifacts from repo context |

---

## How to Use With GitHub Copilot

Open the repository in VS Code.

Open this file:

```text
skills/shopify-headless-middleware/references/inventory-sync.md
```

Then use GitHub Copilot Chat:

```text
Use the open file inventory-sync.md as context.

Act as an AI-SDLC mob programming assistant for a Shopify Headless middleware team.

Help us run a mob session for inventory synchronization between Shopify and ERP/OMS/WMS systems.

Generate:
- required tools
- required logins
- required Shopify scopes to review
- ideal mob roles
- session scope
- inventory event flow
- source-of-truth decision points
- middleware API/event contract
- retry and DLQ strategy
- reconciliation approach
- edge cases
- test scenario matrix
- expected session outcomes
- implementation checklist
```

---

## Recommended Mob Session Flow

### 1. Confirm Inventory Business Intent

Answer:

- What problem are we solving: oversell, latency, accuracy, multi-location, reconciliation, or availability?
- Which system owns inventory?
- Which systems read inventory?
- Which systems update inventory?
- What is the acceptable inventory sync delay?

### 2. Define Source of Truth

Decide:

- Shopify as source of truth
- ERP as source of truth
- WMS as source of truth
- OMS as source of truth
- Hybrid ownership by channel/location/product type

### 3. Map Inventory Event Flow

Start with:

```text
Inventory Updated
  -> Middleware Event
  -> Inventory Sync Service
  -> Shopify Inventory Update
  -> Reconciliation Job
```

### 4. Define Event Contract

The mob should define:

- Event ID
- SKU
- Inventory item ID
- Location ID
- Available quantity
- Source system
- Event timestamp
- Idempotency key
- Correlation ID

### 5. Define Reliability Strategy

Answer:

- How do we handle duplicate events?
- How do we handle out-of-order events?
- What happens when Shopify API fails?
- What goes to the dead-letter queue?
- How are failed events replayed?
- How do we detect inventory mismatches?

### 6. Generate Test Scenarios During the Session

Create tests for:

- Inventory increase
- Inventory decrease
- Duplicate event
- Out-of-order event
- Shopify API failure
- ERP / OMS / WMS downtime
- Location mapping error
- SKU mapping error
- Reconciliation mismatch
- Oversell prevention

---

## Expected Outcomes

By the end of the mob session, the team should have:

- Inventory source-of-truth decision
- Inventory event flow
- Middleware event/API contract
- SKU and location mapping assumptions
- Idempotency strategy
- Retry and DLQ strategy
- Reconciliation approach
- Shopify dependency list
- Required API scopes to review
- Observability and alerting requirements
- Inventory test scenario matrix
- Backlog-ready implementation checklist

---

## Repo-Ready Artifacts to Produce

```text
domains/shopify-headless/architecture/inventory-sync-flow.md
domains/shopify-headless/architecture/inventory-event-contract.md
domains/shopify-headless/testing/inventory-test-scenarios.md
domains/shopify-headless/use-cases/inventory-edge-cases.md
domains/shopify-headless/use-cases/inventory-implementation-checklist.md
```

---

## Definition of Done for the Mob Session

The session is complete when the team has:

- Agreed on inventory source of truth
- Designed inventory event flow
- Defined event/API contract
- Captured retry and DLQ strategy
- Captured reconciliation approach
- Identified Shopify scopes to review
- Captured test scenarios and edge cases
- Created backlog-ready implementation items

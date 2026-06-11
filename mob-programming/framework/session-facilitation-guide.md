# Session Facilitation Guide

## Purpose

This guide provides a repeatable structure for running AI-SDLC Mob Programming sessions.

The goal is to help the team move from a problem statement to implementation-ready artifacts through a focused, collaborative working session.

---

## Session Types

AI-SDLC Mob Programming can be used for several session types.

| Session Type | Example |
|---|---|
| Business rule design | Discount segmentation |
| API design | Customer profile API |
| Integration design | Shopify to OMS integration |
| Testing strategy | Checkout validation test matrix |
| Architecture review | Middleware service decomposition |
| Operational readiness | Observability and failure handling |
| Security review | Customer identity and authorization |

---

## Recommended Session Length

| Complexity | Suggested Duration |
|---|---|
| Small feature | 60 minutes |
| Medium feature | 90 minutes |
| Complex workflow | 2 hours |
| Large integration | Multiple sessions |

Avoid trying to solve too much in one session.

If the topic is large, split it into smaller mobs:

```text
Session 1: Business Rules
Session 2: Architecture and APIs
Session 3: Testing and Readiness
```

---

## Pre-Session Preparation

Before the session, the facilitator should define:

- Session objective
- In-scope items
- Out-of-scope items
- Required participants
- Required tools
- Required access
- Expected outputs
- Relevant repository files
- Existing requirements or tickets
- Known constraints

---

## Required Inputs

Bring as many of these as possible:

- Business problem statement
- Current workflow
- Existing system diagrams
- Relevant code or services
- API documentation
- Current backlog items
- Known production issues
- Existing test cases
- Relevant observability data
- Security or compliance constraints

---

## Session Agenda

### 1. Opening and Objective

Timebox: 5 minutes

The facilitator states:

- Why the session exists
- What problem will be solved
- What outputs are expected
- What is out of scope

Example:

```text
The goal of this session is to define the discount segmentation flow for guest and logged-in customers and produce business rules, API contract, test scenarios, and implementation checklist.
```

---

### 2. Problem Framing

Timebox: 10 minutes

Answer:

- What business problem are we solving?
- Who is impacted?
- What outcome matters?
- What decision must be made today?
- What assumptions are we carrying?

Output:

```text
problem-statement.md
```

---

### 3. Domain Discovery

Timebox: 15 minutes

Identify:

- Actors
- User types
- Systems
- Business rules
- Data sources
- Exceptions
- Constraints

Helpful AI prompt:

```text
Based on this use case, generate domain discovery questions for Product, Architecture, Development, QA, Security, and DevOps.
```

Output:

```text
domain-discovery-notes.md
```

---

### 4. Architecture Discussion

Timebox: 20 minutes

Discuss:

- System boundaries
- Service ownership
- Integration points
- Data ownership
- Failure handling
- Performance needs
- Security boundaries

Output:

```text
architecture-decisions.md
```

---

### 5. API or Event Design

Timebox: 20 minutes

Define:

- Endpoint or event name
- Request payload
- Response payload
- Error model
- Authentication
- Authorization
- Idempotency
- Timeouts
- Observability fields

Output:

```text
api-contract.md
```

or

```text
event-contract.md
```

---

### 6. Testing Strategy

Timebox: 15 minutes

Generate:

- Happy path tests
- Negative path tests
- Boundary tests
- Security tests
- Integration tests
- Regression tests
- Failure-mode tests

Output:

```text
test-scenarios.md
```

---

### 7. Risk and Edge Case Review

Timebox: 10 minutes

Discuss:

- What can fail?
- What can be misunderstood?
- What can break in production?
- What requires manual intervention?
- What requires monitoring?
- What requires escalation?

Output:

```text
risks-and-edge-cases.md
```

---

### 8. Implementation Readiness Review

Timebox: 10 minutes

Confirm:

- Business rules are clear
- Architecture is understood
- APIs are defined
- Tests are identified
- Risks are documented
- Security concerns are captured
- Operational needs are known
- Implementation checklist exists

Output:

```text
implementation-checklist.md
```

---

## Facilitation Techniques

### Keep the Session Outcome-Oriented

Avoid long theoretical discussions.

Ask:

```text
What artifact should this discussion produce?
```

### Capture Decisions Separately from Open Questions

Use two sections:

```text
Decisions
Open Questions
```

### Use AI for Drafting, Not Deciding

AI can generate options, but the team validates.

### Ask Role-Specific Questions

Examples:

Product:

```text
What customer outcome matters?
```

QA:

```text
What failure scenarios must be tested?
```

DevOps:

```text
What should we monitor?
```

Security:

```text
What access or data risk exists?
```

---

## Common Anti-Patterns

Avoid:

- Turning the session into status reporting
- Allowing only one role to dominate
- Producing only meeting notes
- Ignoring testing until the end
- Deferring security questions
- Ignoring operational concerns
- Letting AI output go unvalidated
- Discussing too many topics in one session

---

## Final Output Package

A strong session should produce:

```text
problem-statement.md
business-rules.md
architecture-decisions.md
api-contract.md
test-scenarios.md
risks-and-edge-cases.md
implementation-checklist.md
```

These files can be committed to the repository or converted into backlog items.

---

## Principle

The facilitator's job is not to run a meeting.

The facilitator's job is to help the team create shared understanding and usable delivery artifacts.

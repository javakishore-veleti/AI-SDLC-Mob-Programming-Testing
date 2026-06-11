# Implementation Readiness

## Purpose

Implementation readiness means the team has enough shared understanding to begin delivery with reduced ambiguity and reduced rework risk.

This is different from backlog readiness.

A backlog item may be ready for sprint planning but still lack technical, testing, security, or operational clarity.

Implementation readiness requires a deeper level of preparation.

---

## Definition

A feature, capability, or integration is implementation-ready when the team has clarity across:

- Business intent
- Scope
- Architecture
- APIs or events
- Data requirements
- Testing
- Security
- Operations
- Risks
- Implementation sequence

---

## Implementation Readiness Checklist

### 1. Business Readiness

- [ ] Business objective is clear
- [ ] Target users or systems are identified
- [ ] Success criteria are defined
- [ ] In-scope items are confirmed
- [ ] Out-of-scope items are confirmed
- [ ] Business rules are documented
- [ ] Exceptions are captured

### 2. Domain Readiness

- [ ] Key actors are identified
- [ ] Domain terms are clarified
- [ ] Current process is understood
- [ ] Future process is described
- [ ] Edge cases are documented
- [ ] Assumptions are captured

### 3. Architecture Readiness

- [ ] Impacted systems are identified
- [ ] Service boundaries are clear
- [ ] Integration points are defined
- [ ] Data ownership is understood
- [ ] Dependencies are documented
- [ ] Architecture decisions are captured
- [ ] Open architecture questions are listed

### 4. API / Event Readiness

- [ ] Endpoint or event names are defined
- [ ] Request payload is drafted
- [ ] Response payload is drafted
- [ ] Error model is defined
- [ ] Authentication is considered
- [ ] Authorization is considered
- [ ] Idempotency is considered where needed
- [ ] Versioning is considered
- [ ] Timeout and retry behavior is discussed

### 5. Testing Readiness

- [ ] Happy path scenarios are documented
- [ ] Negative scenarios are documented
- [ ] Boundary conditions are documented
- [ ] Regression risks are identified
- [ ] Test data needs are identified
- [ ] Automation candidates are identified
- [ ] Integration test needs are captured
- [ ] Failure-mode tests are identified

### 6. Security Readiness

- [ ] Sensitive data is identified
- [ ] Access requirements are documented
- [ ] Required scopes or permissions are reviewed
- [ ] Authentication risks are considered
- [ ] Authorization risks are considered
- [ ] Logging and masking concerns are reviewed
- [ ] Security owner is identified if deeper review is needed

### 7. Operational Readiness

- [ ] Logging requirements are defined
- [ ] Metrics are identified
- [ ] Alerts are considered
- [ ] Dashboards are considered
- [ ] Failure handling is documented
- [ ] Retry behavior is reviewed
- [ ] Support or manual intervention process is discussed
- [ ] Rollback or recovery approach is considered

### 8. Delivery Readiness

- [ ] Implementation checklist exists
- [ ] Backlog-ready stories can be created
- [ ] Dependencies are visible
- [ ] Sequencing is understood
- [ ] Owners are identified
- [ ] Open questions are tracked
- [ ] Risks are accepted or mitigated

---

## Readiness Levels

Use readiness levels to describe maturity.

### Level 0: Idea

The problem is known, but the solution is unclear.

### Level 1: Backlog Ready

The story has enough detail for planning but may not have full implementation clarity.

### Level 2: Design Ready

The architecture and API direction are understood.

### Level 3: Test Ready

Key scenarios, edge cases, and failure modes are identified.

### Level 4: Implementation Ready

Business, architecture, testing, security, and operational concerns are sufficiently understood.

---

## Example: Discount Segmentation

A discount segmentation capability is not implementation-ready just because the story says:

```text
Guest customers should receive a welcome discount.
```

It becomes implementation-ready when the team knows:

- How guest customers are identified
- How logged-in customers are identified
- Which customer tags matter
- Which discounts can stack
- Which middleware API evaluates discounts
- What Shopify APIs or scopes are needed
- What happens if Shopify rejects the discount
- What happens if a guest logs in during checkout
- What test scenarios must be covered
- What should be logged and monitored

---

## Readiness Review Questions

Before implementation begins, ask:

- Can a developer explain what needs to be built?
- Can QA explain how it will be tested?
- Can DevOps explain how it will be monitored?
- Can Security explain what risks exist?
- Can Product explain what business outcome is expected?
- Can the team explain what is out of scope?
- Can the team identify unresolved questions?

If the answer is no, the work is not fully implementation-ready.

---

## Principle

Implementation readiness is not about creating perfect documentation.

It is about reducing ambiguity before delivery starts.

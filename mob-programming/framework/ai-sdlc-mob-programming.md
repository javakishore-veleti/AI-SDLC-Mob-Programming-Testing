# AI-SDLC Mob Programming

## Definition

AI-SDLC Mob Programming is a collaborative engineering approach where cross-functional participants work together with AI support to move from business context to implementation-ready outcomes.

It extends traditional Mob Programming beyond coding.

Instead of only working together at the keyboard, the team works together across:

- Requirements discovery
- Domain analysis
- Architecture design
- API modeling
- Data flow design
- Test planning
- Security review
- Operational readiness
- Implementation planning

---

## Why This Matters

Software delivery problems are often not caused by lack of coding effort.

They are caused by:

- Unclear requirements
- Missed edge cases
- Late architecture review
- Testing after design is complete
- Security considered too late
- Operational concerns discovered after deployment
- Different teams carrying different assumptions

AI-SDLC Mob Programming reduces these issues by bringing the right people into the same working session and using AI to accelerate structured thinking.

---

## Traditional SDLC Pattern

A common delivery pattern looks like this:

```text
Business Requirement
  -> Architecture Review
  -> Development
  -> QA Testing
  -> Security Review
  -> Deployment
  -> Production Feedback
```

This creates handoffs.

Every handoff increases the risk of misunderstanding.

---

## AI-SDLC Mob Programming Pattern

The AI-SDLC Mob Programming pattern looks like this:

```text
Business + Architecture + Development + QA + DevOps + Security + AI
  -> Shared Discovery
  -> Shared Design
  -> Shared Testing Strategy
  -> Shared Implementation Readiness
```

The goal is not to remove specialized roles.

The goal is to bring specialized thinking earlier into the lifecycle.

---

## Core Outcomes

A session should produce concrete outputs such as:

- Problem statement
- Scope and out-of-scope boundaries
- Business rules
- Architecture decisions
- API contracts
- Event contracts
- Data mapping
- Integration assumptions
- Test scenarios
- Edge cases
- Risks
- Security considerations
- Observability requirements
- Implementation checklist
- Backlog-ready tasks

---

## Example Outcome Difference

### Traditional Output

```text
Story:
As a customer, I want a discount so that I can save money.

Acceptance Criteria:
Customer receives discount when eligible.
```

### AI-SDLC Mob Programming Output

```text
Business Rule:
IF customer is guest
AND cart value >= 100
THEN apply WELCOME5

API:
POST /discount/evaluate

Test Scenarios:
- Guest cart qualifies
- Guest cart does not qualify
- Guest logs in during checkout
- Discount expires
- Shopify API fails
- Cache contains stale segment

Operational Considerations:
- Log discount evaluation failures
- Track cache hit ratio
- Monitor discount rejection rate
```

The second output is much closer to implementation readiness.

---

## Where AI Helps

AI can help the mob by generating:

- Clarifying questions
- Alternative designs
- API examples
- Edge cases
- Test scenarios
- Risk lists
- Checklists
- Documentation drafts
- Backlog-ready stories

AI should not make final decisions.

Human participants remain accountable for business, architecture, security, and delivery decisions.

---

## When to Use AI-SDLC Mob Programming

Use this approach for work that has:

- Multiple system dependencies
- Complex business rules
- Significant testing needs
- Security or compliance concerns
- Operational impact
- Cross-team ownership
- High ambiguity
- High cost of rework

Avoid it for simple changes that one developer can complete independently.

---

## Session Inputs

Before the session, gather:

- Business objective
- Existing requirements
- Current architecture
- Known constraints
- Relevant code or repository files
- API documentation
- System access requirements
- Known risks
- Current test coverage
- Operational dashboards if available

---

## Session Outputs

After the session, store outputs in source control when possible.

Recommended output files:

```text
architecture-decisions.md
api-contract.md
business-rules.md
test-scenarios.md
edge-cases.md
implementation-checklist.md
```

---

## Principle

AI-SDLC Mob Programming is not about making meetings longer.

It is about making collaboration more complete, structured, and implementation-focused.

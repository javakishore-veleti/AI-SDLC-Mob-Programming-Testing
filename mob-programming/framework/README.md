# AI-SDLC Mob Programming Framework

## Overview

This framework defines a repeatable way to conduct AI-assisted Mob Programming sessions across the Software Development Lifecycle.

The framework is designed for teams that want to move from business ideas and backlog discussions into implementation-ready outcomes through structured collaboration.

It is especially useful for complex work involving APIs, integrations, business rules, test strategy, security, observability, and operational readiness.

---

## Framework Objective

The objective is to help teams answer the right questions before implementation begins.

A well-run AI-SDLC Mob Programming session should clarify:

- What problem are we solving?
- Who are the impacted users or systems?
- What business rules apply?
- What architecture is needed?
- What APIs or events are required?
- What data is needed?
- What can fail?
- What should be tested?
- What must be secured?
- What must be monitored?
- What artifacts should be produced?

---

## Framework Documents

| Document | Purpose |
|---|---|
| `ai-sdlc-mob-programming.md` | Defines the operating model and mindset |
| `backlog-refinement-vs-ai-sdlc.md` | Explains the difference from traditional backlog refinement |
| `roles-and-responsibilities.md` | Defines who participates and what each role contributes |
| `session-facilitation-guide.md` | Provides a practical session agenda and facilitation structure |
| `implementation-readiness.md` | Defines readiness criteria before work enters delivery |
| `ai-participant-model.md` | Explains how AI participates without replacing ownership |

---

## How the Framework Is Used

The framework can be used in three ways.

### 1. Before a Session

Use it to prepare:

- Session objective
- Required roles
- Required access
- Required tools
- Scope and out-of-scope boundaries
- Expected deliverables

### 2. During a Session

Use it to guide the team through:

- Problem framing
- Discovery
- Architecture
- API design
- Risk analysis
- Testing
- Security
- Operational readiness
- Implementation planning

### 3. After a Session

Use it to convert decisions into:

- Markdown artifacts
- GitHub Issues
- Jira stories
- Architecture Decision Records
- API contracts
- Test cases
- Implementation checklists

---

## How This Relates to Domain Playbooks

This framework is domain-independent.

Domain-specific playbooks, such as Shopify Headless Middleware, should reuse this structure and apply it to a specific business or technical problem.

Example:

```text
Framework:
AI-SDLC Mob Programming

Domain:
Shopify Headless Middleware

Use Case:
Discount Segmentation

Output:
API contract, rules, test scenarios, implementation checklist
```

---

## Recommended Flow

```text
Framework Understanding
  -> Session Preparation
  -> Mob Programming Session
  -> Implementation Readiness Review
  -> Backlog / Delivery Artifacts
```

---

## Success Criteria

A session is successful when the team can clearly answer:

- What will be built?
- Why it matters?
- How it will work?
- What systems are involved?
- What can go wrong?
- How it will be tested?
- How it will be secured?
- How it will be operated?
- What is ready for implementation?

---

## Principle

The framework does not exist to create more documentation.

It exists to create shared understanding and implementation-ready artifacts.

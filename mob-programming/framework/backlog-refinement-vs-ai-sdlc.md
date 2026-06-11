# Backlog Refinement vs AI-SDLC Mob Programming

## Purpose

This document explains how AI-SDLC Mob Programming differs from traditional sprint backlog refinement.

This distinction is important because AI-SDLC Mob Programming may look similar to backlog refinement at first glance. Both involve discussing future work. However, the depth, participants, questions, and outcomes are different.

---

## Traditional Sprint Backlog Refinement

Backlog refinement usually focuses on preparing backlog items for future sprint planning.

Typical goals include:

- Clarifying user stories
- Splitting work
- Adding acceptance criteria
- Estimating effort
- Identifying obvious dependencies
- Preparing items for sprint planning

Typical output:

- Refined story
- Acceptance criteria
- Estimate
- Priority
- Sprint readiness

This is useful, but it does not always produce implementation readiness.

---

## AI-SDLC Mob Programming

AI-SDLC Mob Programming focuses on collaboratively creating implementation-ready outcomes.

It brings together product, architecture, development, QA, DevOps, security, business SMEs, and AI support to explore the work more deeply.

Typical goals include:

- Understand business context
- Identify system dependencies
- Define architecture approach
- Create API/event contracts
- Generate test scenarios
- Identify edge cases
- Review security concerns
- Define operational requirements
- Produce implementation checklist
- Create backlog-ready stories after technical clarity is achieved

---

## Comparison

| Dimension | Backlog Refinement | AI-SDLC Mob Programming |
|---|---|---|
| Primary goal | Prepare stories for sprint planning | Create implementation-ready outcomes |
| Main question | What work should we do? | What do we need to understand, design, test, secure, and operate? |
| Typical participants | PO, Scrum Master, Developers | Product, Business, Architecture, Dev, QA, DevOps, Security, AI |
| Output | Story, acceptance criteria, estimate | Architecture, APIs, tests, risks, checklist, stories |
| Depth | Story-level clarity | System-level readiness |
| Testing | Acceptance criteria | Test scenario matrix and edge cases |
| Architecture | Often deferred or summarized | Discussed directly in session |
| Security | Often separate review | Considered during design |
| Operations | Often later | Considered before implementation |
| AI role | Optional assistant | Structured session participant |

---

## Example: Discount Segmentation

### Backlog Refinement Output

```text
Story:
As a guest customer, I want to receive a welcome discount so that I am encouraged to purchase.

Acceptance Criteria:
- Guest receives WELCOME5 when cart value is over 100
- Discount is visible in cart
- Discount is applied at checkout

Estimate:
8 points
```

This may be enough to start work, but many questions remain unanswered.

### AI-SDLC Mob Programming Output

```text
Business Rule:
IF customer is guest
AND cart value >= 100
THEN apply WELCOME5

API:
POST /discount/evaluate

Architecture:
Identity Service
  -> Customer Context Service
  -> Segmentation Service
  -> Discount Rules Engine
  -> Cart Pricing Service
  -> Checkout Integration

Test Scenarios:
- Guest cart qualifies
- Guest cart does not qualify
- Guest logs in after discount is applied
- Logged-in VIP customer receives VIP20
- Wholesale customer receives contract pricing
- Discount expires during checkout
- Shopify API fails
- Cache has stale customer segment

Risks:
- Discount shown in cart but rejected at checkout
- Customer segment cache is stale
- Shopify customer tag changes after evaluation
- Multiple discounts conflict

Operational Requirements:
- Log discount evaluation failures
- Track discount rejection rate
- Monitor cache hit ratio
- Trace cart-to-checkout discount decisions
```

This output gives the team a stronger starting point for implementation.

---

## Why Backlog Refinement Alone Is Not Enough for Complex Work

Backlog refinement is valuable, but complex work often requires deeper readiness.

Complex work usually involves:

- Multiple services
- External systems
- API contracts
- Data ownership
- Error handling
- Security concerns
- Performance constraints
- Observability requirements
- Test strategy
- Business rule ambiguity

If these concerns are not discussed early, teams may discover them during implementation or testing, which increases rework.

---

## How They Work Together

AI-SDLC Mob Programming does not replace backlog refinement.

It can happen before or during refinement for complex items.

Recommended flow:

```text
Initial Idea
  -> AI-SDLC Mob Programming Session
  -> Implementation-Ready Artifacts
  -> Backlog Refinement
  -> Sprint Planning
  -> Delivery
```

In this model, backlog refinement becomes stronger because the team already has deeper clarity.

---

## When to Use Backlog Refinement

Use traditional backlog refinement for:

- Simple enhancements
- Well-understood work
- Minor UI changes
- Small bug fixes
- Configuration updates
- Work with clear acceptance criteria

---

## When to Use AI-SDLC Mob Programming

Use AI-SDLC Mob Programming for:

- New capabilities
- Complex integrations
- Cross-system workflows
- Security-sensitive features
- High-risk changes
- API design
- Architecture decisions
- Testing-heavy work
- Operationally sensitive features

---

## Key Difference

Backlog refinement asks:

```text
Is this story ready for a sprint?
```

AI-SDLC Mob Programming asks:

```text
Is the team ready to implement this safely, correctly, and with shared understanding?
```

That is the practical difference.

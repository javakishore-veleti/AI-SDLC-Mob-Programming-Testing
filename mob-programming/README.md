# Mob Programming for AI-SDLC

## Purpose

This section defines the Mob Programming operating model used in this repository.

The goal is to help teams move beyond traditional handoffs and conduct structured, collaborative working sessions that produce implementation-ready outcomes.

In this model, Mob Programming is not limited to writing code together. It becomes a practical way for cross-functional teams to work through requirements, architecture, API design, testing, security, operational readiness, and delivery planning with AI support.

---

## Why Mob Programming Matters in AI-SDLC

Many teams already use AI tools. The bigger challenge is creating a repeatable way for teams to use AI together.

Without structure, AI usage often becomes individual and fragmented:

```text
Developer uses AI for code
QA uses AI for test cases
Architect uses AI for diagrams
Product uses AI for requirements
```

That may improve individual productivity, but it does not automatically improve shared understanding.

AI-SDLC Mob Programming creates a collaborative model where the team works together using AI as part of the session.

The team jointly produces:

- Business rules
- Architecture decisions
- API contracts
- Test scenarios
- Edge cases
- Security considerations
- Operational requirements
- Implementation checklists
- Backlog-ready work items

---

## What This Is Not

This is not a replacement for Scrum, Kanban, SAFe, XP, or existing delivery practices.

It is also not a meeting format for status updates.

AI-SDLC Mob Programming is a focused working session where the team collaborates on a specific problem and leaves with usable engineering artifacts.

Avoid using this approach for:

- Routine status meetings
- Simple backlog grooming
- Low-complexity tasks
- Work that does not need cross-functional input
- Topics where the decision is already obvious

Use it when the work requires multiple perspectives and early alignment.

---

## When to Use This Approach

Use AI-SDLC Mob Programming when a team needs to collaboratively define or validate:

- Complex business rules
- Middleware/API workflows
- Integration patterns
- Data flows
- Security-sensitive features
- Test strategy
- Operational readiness
- Failure handling
- Cross-system dependencies
- Implementation sequencing

Good candidates include:

- Checkout customization
- Discount segmentation
- Inventory synchronization
- OMS/ERP integrations
- Authentication and authorization flows
- Customer profile services
- Payment or tax integrations
- AI agent workflows
- Enterprise data pipelines
- Cloud-native modernization efforts

---

## Core Participants

A strong Mob Programming session usually includes:

| Role | Contribution |
|---|---|
| Product Owner | Business objective, priorities, customer value |
| Business SME | Domain rules and real-world scenarios |
| Architect | System design, patterns, dependencies |
| Developer | Implementation feasibility, APIs, services |
| QA Engineer | Test scenarios, edge cases, validation approach |
| DevOps/SRE | Observability, reliability, deployment concerns |
| Security Engineer | Identity, access, data protection, risk review |
| AI Assistant / Copilot Operator | Generates options, artifacts, prompts, and refinements |
| Facilitator | Keeps the session focused and outcome-driven |

Not every session needs every role. The facilitator should select participants based on the topic.

---

## Expected Session Outputs

A successful session should produce more than notes.

Expected outputs include:

- Defined problem statement
- Confirmed scope and out-of-scope items
- Business rules
- Architecture decisions
- API or event contracts
- Data assumptions
- Test scenario matrix
- Edge case list
- Risks and mitigations
- Security considerations
- Observability requirements
- Implementation checklist
- Backlog-ready stories or tasks

The output should be commit-ready or easy to convert into issue-tracking artifacts.

---

## Repository Structure

```text
mob-programming/
├── README.md
└── framework/
    ├── README.md
    ├── ai-sdlc-mob-programming.md
    ├── backlog-refinement-vs-ai-sdlc.md
    ├── roles-and-responsibilities.md
    ├── session-facilitation-guide.md
    ├── implementation-readiness.md
    └── ai-participant-model.md
```

---

## How to Use This Section

Start with:

```text
mob-programming/framework/README.md
```

Then read:

1. `ai-sdlc-mob-programming.md`
2. `backlog-refinement-vs-ai-sdlc.md`
3. `roles-and-responsibilities.md`
4. `session-facilitation-guide.md`
5. `implementation-readiness.md`
6. `ai-participant-model.md`

Use the framework documents before applying a domain playbook such as Shopify Headless Middleware.

---

## Key Principle

Traditional delivery often asks:

```text
What work should we assign?
```

AI-SDLC Mob Programming asks:

```text
What do we need to understand, design, test, secure, operate, and implement together?
```

That shift is the foundation of this repository.

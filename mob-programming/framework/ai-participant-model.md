# AI Participant Model

## Purpose

This document defines how AI participates in AI-SDLC Mob Programming sessions.

AI is treated as a collaborative assistant that helps the team think, structure, generate, compare, and document.

AI does not replace accountable human roles.

---

## AI as a Participant

In traditional tool usage, AI is often used privately by individuals.

In AI-SDLC Mob Programming, AI becomes part of the shared team workflow.

The team uses AI to:

- Generate questions
- Draft artifacts
- Identify missing scenarios
- Compare options
- Summarize decisions
- Convert discussion into structured outputs
- Improve clarity and completeness

---

## What AI Can Contribute

### 1. Discovery Support

AI can generate questions for:

- Product
- Business SMEs
- Architects
- Developers
- QA
- DevOps
- Security

Example prompt:

```text
Generate discovery questions for a discount segmentation feature across Product, Architecture, Development, QA, DevOps, and Security.
```

### 2. Architecture Support

AI can help draft:

- System flows
- Service boundaries
- Integration options
- Data flow descriptions
- Architecture decision candidates

AI output must be reviewed by architects and engineers.

### 3. API and Event Modeling

AI can generate:

- Endpoint examples
- Request payloads
- Response payloads
- Error models
- Event contracts
- Versioning considerations

### 4. Testing Support

AI can generate:

- Happy path tests
- Negative tests
- Edge cases
- Boundary conditions
- Failure-mode scenarios
- Regression candidates

QA owns validation and final test strategy.

### 5. Security Support

AI can suggest:

- Access concerns
- Sensitive data risks
- Authorization questions
- Logging and masking considerations
- Abuse cases

Security owners must validate final decisions.

### 6. Operational Support

AI can suggest:

- Logs
- Metrics
- Alerts
- Dashboards
- Failure handling
- Retry strategies
- Manual intervention scenarios

DevOps/SRE owns operational validation.

### 7. Documentation Support

AI can convert session discussion into:

- Markdown artifacts
- Checklists
- Backlog-ready stories
- Architecture notes
- API contracts
- Test matrices

---

## What AI Should Not Do

AI should not:

- Approve architecture
- Approve security
- Make final business decisions
- Replace product ownership
- Replace QA validation
- Approve production releases
- Invent facts without validation
- Override system owners
- Decide compliance requirements

---

## AI Operator Role

Each session should have an AI Operator.

The AI Operator is responsible for:

- Entering prompts
- Providing context
- Asking follow-up questions
- Capturing AI output
- Asking the team to validate AI output
- Turning accepted output into artifacts

This role may be performed by the facilitator, developer, architect, or another participant.

---

## Recommended AI Workflow

```text
Team discusses
  -> AI generates draft
  -> Team reviews
  -> Team corrects
  -> AI refines
  -> Team approves
  -> Artifact is committed
```

AI output should not bypass team review.

---

## Example AI Prompt Pattern

Use this structure:

```text
Context:
<describe system, domain, and problem>

Role:
Act as an AI-SDLC Mob Programming assistant.

Task:
Generate <artifact type>.

Constraints:
<include scope, assumptions, exclusions>

Output Format:
<table, checklist, markdown, API contract, test matrix>
```

---

## Example

```text
Context:
We are designing guest and logged-in customer discount segmentation for a Shopify Headless middleware system.

Role:
Act as an AI-SDLC Mob Programming assistant.

Task:
Generate test scenarios and edge cases.

Constraints:
Include guest, logged-in, VIP, wholesale, expired discount, Shopify API failure, cache stale, and checkout rejection scenarios.

Output Format:
Markdown table with Scenario, Input, Expected Result, Owner, and Priority.
```

---

## AI Output Validation Checklist

Before accepting AI output, ask:

- Is this accurate for our domain?
- Did AI invent any assumptions?
- Are system names correct?
- Are API capabilities valid?
- Are security concerns complete?
- Are test scenarios realistic?
- Are edge cases relevant?
- Does this need review by another role?

---

## Principle

AI accelerates the session, but the team owns the decisions.

AI is a participant, not an approver.

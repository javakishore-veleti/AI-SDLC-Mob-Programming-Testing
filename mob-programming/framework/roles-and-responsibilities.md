# Roles and Responsibilities

## Purpose

AI-SDLC Mob Programming depends on the right participants contributing at the right time.

This document defines common roles, responsibilities, and boundaries for participants in a mob session.

Not every session requires every role. The facilitator should select participants based on the complexity, risk, and scope of the work.

---

## Product Owner

### Responsibilities

- Define the business objective
- Explain customer value
- Clarify priority
- Confirm scope
- Make trade-off decisions
- Define success criteria

### Questions Product Should Answer

- Why are we building this?
- Which users or customers are impacted?
- What business outcome matters?
- What is in scope?
- What is out of scope?
- What would make this feature successful?

### Not Responsible For

- Detailed technical design
- Final security approval
- Production operations

---

## Business Subject Matter Expert

### Responsibilities

- Explain domain rules
- Provide real-world scenarios
- Identify exceptions
- Clarify business terminology
- Validate rule accuracy

### Questions Business SMEs Should Answer

- What rules apply?
- What exceptions exist?
- What edge cases have occurred before?
- What manual process exists today?
- What business policy must be respected?

---

## Solution Architect

### Responsibilities

- Define system boundaries
- Identify architecture patterns
- Review integration approach
- Identify dependencies
- Validate scalability and maintainability
- Capture architecture decisions

### Questions Architects Should Answer

- Which systems are involved?
- What services are needed?
- Where should business logic live?
- What are the integration points?
- What are the major risks?
- What architecture decisions must be documented?

---

## Developer / Engineer

### Responsibilities

- Validate technical feasibility
- Design APIs or events
- Identify code impacts
- Identify data requirements
- Clarify implementation complexity
- Suggest implementation sequence

### Questions Developers Should Answer

- What APIs are needed?
- What data is required?
- What services are impacted?
- What existing code can be reused?
- What technical constraints exist?
- What implementation tasks are needed?

---

## QA Engineer

### Responsibilities

- Generate test scenarios during design
- Identify negative paths
- Identify edge cases
- Define validation strategy
- Recommend automation coverage
- Clarify acceptance criteria from a testing perspective

### Questions QA Should Answer

- What are the happy paths?
- What can fail?
- What are the boundary conditions?
- What regression risk exists?
- What should be automated?
- What test data is required?

---

## DevOps / SRE Engineer

### Responsibilities

- Review deployability
- Identify monitoring needs
- Define logging and tracing expectations
- Review performance and reliability concerns
- Identify rollback or recovery needs
- Define operational readiness requirements

### Questions DevOps/SRE Should Answer

- What needs to be monitored?
- What logs are required?
- What metrics matter?
- What happens when a dependency fails?
- How do we detect and respond to failures?
- What deployment or environment constraints exist?

---

## Security Engineer

### Responsibilities

- Review identity and access concerns
- Validate authorization requirements
- Identify PII or sensitive data risks
- Review token and secret handling
- Identify compliance concerns
- Define security validation needs

### Questions Security Should Answer

- What data is sensitive?
- Who can access this capability?
- What permissions are needed?
- What abuse cases exist?
- What must be logged or masked?
- What requires security review before release?

---

## AI Assistant / Copilot Operator

### Responsibilities

- Generate structured prompts
- Summarize decisions
- Create draft artifacts
- Generate API examples
- Generate test scenarios
- Identify edge cases
- Compare design options
- Maintain session notes in structured format

### Good Uses of AI

- Generate first-draft API contracts
- Generate test matrices
- Produce implementation checklists
- Identify missing scenarios
- Create role-specific questions
- Convert session notes into markdown artifacts
- Draft backlog-ready stories

### AI Boundaries

AI should not:

- Make final business decisions
- Approve architecture
- Approve security
- Approve production release
- Replace accountable owners
- Invent facts without validation

---

## Facilitator

### Responsibilities

- Define session goal
- Keep the discussion focused
- Manage timeboxes
- Ensure all roles contribute
- Capture open questions
- Confirm decisions
- Drive toward deliverables

### Facilitator Checklist

- Is the objective clear?
- Are the right roles present?
- Are assumptions being captured?
- Are decisions being documented?
- Are risks being identified?
- Are test scenarios being created?
- Are outputs repo-ready or backlog-ready?

---

## Recommended Role Mix by Session Type

| Session Type | Recommended Roles |
|---|---|
| Business rule design | Product, Business SME, Developer, QA, AI |
| API design | Architect, Developer, QA, Security, AI |
| Integration design | Architect, Developer, DevOps, Security, Business SME, AI |
| Test strategy | QA, Developer, Product, Business SME, AI |
| Operational readiness | DevOps/SRE, Developer, Architect, Security, AI |
| Security-sensitive feature | Security, Architect, Developer, Product, QA, AI |

---

## Principle

AI-SDLC Mob Programming works best when each role contributes its expertise early.

The purpose is not to have more people in a meeting.

The purpose is to reduce late discovery, rework, and misalignment.

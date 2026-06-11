---
name: release-management-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for release planning, release readiness, deployment windows, change approvals, feature flags, rollback planning, release communications, and production cutover readiness.
---

# Release Management AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for release planning, release readiness, and production cutover.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Major release planning
- Production cutover planning
- Feature flag rollout
- Change approval preparation
- Release communication
- Rollback planning
- Go/no-go readiness review
- Post-release validation

Avoid using this playbook for routine status updates or simple operational tasks that do not require cross-functional design.

---

## AI-SDLC Mob Programming Objective

The mob should answer:

```text
What do we need to understand, design, test, secure, automate, monitor,
operate, and recover before this DevOps capability is implementation-ready?
```

The session should produce actionable engineering artifacts, not meeting notes.

---

## Required Tools

| Tool | Why It Is Needed |
|---|---|
| Release Calendar | Review deployment windows and conflicts |
| CI/CD Platform | Review deployability and release automation |
| Feature Flag Tool | Define rollout strategy |
| Change Management Tool | Capture approvals and release evidence |
| Observability Platform | Define release health signals |
| Incident Tool | Prepare escalation and rollback response |
| Communication Tool | Coordinate stakeholder updates |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Release management access | Review schedules and approvals |
| CI/CD access | Validate deployment workflow |
| Feature flag access | Review rollout controls |
| Change management access | Prepare CAB/change evidence if required |
| Observability access | Validate release health checks |
| Incident tool access | Prepare escalation and rollback process |

---

## Ideal Mob Roles

| Role | Responsibility |
|---|---|
| Product Owner / Delivery Owner | Defines business priority, release impact, and delivery expectations |
| Engineering Lead | Validates technical feasibility and implementation ownership |
| DevOps Engineer | Designs automation, deployment, and environment workflows |
| SRE Engineer | Reviews reliability, monitoring, failure modes, and recovery |
| QA / Quality Engineer | Defines validation, regression, and release quality gates |
| Security Engineer | Reviews secrets, identity, access, scanning, compliance, and risk |
| Platform Engineer | Reviews reusable platform capabilities and developer experience |
| AI / Copilot Operator | Generates draft artifacts, checklists, risks, prompts, and task breakdowns |
| Facilitator | Keeps the mob focused, captures decisions, and drives deliverables |

---

## Recommended Session Flow

### 1. Release Scope

Define features included, systems impacted, environments impacted, business risk, and customer impact.

### 2. Readiness Review

Review code, test, security, operational, support, and rollback readiness.

### 3. Rollout Strategy

Define big bang vs phased rollout, feature flags, canary release, pilot users, regional rollout, and rollback triggers.

### 4. Go/No-Go Decision

Define required evidence and decision owners.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for release planning, release readiness, and production cutover.

Generate:
- required tools
- required access
- ideal participants
- architecture and workflow decisions
- security considerations
- testing strategy
- operational readiness checklist
- risks and edge cases
- implementation-ready deliverables
- backlog-ready stories or tasks

Do not generate generic DevOps notes.
Produce concrete engineering artifacts that can be committed into the repository.
```

---

## Expected Deliverables

The mob session should produce:

- `devops/release-management/release-plan.md`
- `devops/release-management/go-no-go-checklist.md`
- `devops/release-management/rollback-plan.md`
- `devops/release-management/release-communication.md`
- `devops/release-management/post-release-validation.md`

---

## Implementation Readiness Checklist

- [ ] Release scope defined
- [ ] Impacted systems identified
- [ ] Test evidence reviewed
- [ ] Security evidence reviewed
- [ ] Operational readiness confirmed
- [ ] Rollback plan documented
- [ ] Go/no-go owners identified
- [ ] Communication plan prepared

---

## Definition of Done

The session is complete when:

- The scope is clear.
- Required tools and access are identified.
- Architecture or workflow decisions are documented.
- Security and compliance concerns are reviewed.
- Testing and validation strategy is defined.
- Observability and operational readiness are addressed.
- Risks and edge cases are captured.
- Backlog-ready implementation tasks are created.
- Artifacts are ready to commit to the repository.

---

## Principle

This playbook is designed for **AI-SDLC Mob Programming**, where the team collaborates with AI to create implementation readiness across delivery, reliability, security, and operations.

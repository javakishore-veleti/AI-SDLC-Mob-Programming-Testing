---
name: sre-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for site reliability engineering, reliability reviews, production readiness, operational risk, service ownership, error budgets, incident response, observability, and resilience planning.
---

# SRE AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for SRE operating model and service reliability readiness.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Production readiness reviews
- Reliability design sessions
- Service ownership definition
- Error budget discussions
- Resilience planning
- Operational risk review
- On-call readiness
- Failure-mode analysis
- Reliability improvement planning

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
| Service Catalog | Identify service owners, dependencies, and criticality |
| Observability Platform | Review metrics, logs, traces, alerts, and dashboards |
| Incident Management Tool | Review incidents, escalation, and response process |
| CI/CD Tool | Validate deployment and rollback behavior |
| Cloud / Kubernetes Platform | Review runtime reliability and scaling |
| Runbook Repository | Validate operational procedures |
| Issue Tracker | Convert reliability gaps into work items |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Production observability access | Review current reliability signals |
| Incident tool access | Review incident history and escalation process |
| Service repository access | Review runtime, deployment, and ownership |
| Cloud or cluster read access | Review capacity, scaling, and availability |
| On-call schedule access | Review ownership and escalation |
| Runbook access | Review operational procedures |

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

### 1. Service Reliability Context

Define service purpose, critical user journeys, dependencies, service owner, and business impact.

### 2. Reliability Target Discussion

Identify availability, latency, error rate, recovery expectations, and degradation strategy.

### 3. Failure Mode Review

Discuss dependency failure, deployment failure, traffic spike, data store failure, network degradation, authentication failure, queue backlog, and configuration error.

### 4. Operational Readiness

Review runbooks, alerts, dashboards, on-call model, escalation, and recovery procedures.

### 5. Reliability Backlog

Convert gaps into reliability work items.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for SRE operating model and service reliability readiness.

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

- `devops/sre/service-reliability-review.md`
- `devops/sre/failure-mode-analysis.md`
- `devops/sre/operational-readiness-checklist.md`
- `devops/sre/reliability-backlog.md`
- `devops/sre/runbook-gaps.md`

---

## Implementation Readiness Checklist

- [ ] Service owner identified
- [ ] Critical user journeys documented
- [ ] Dependencies mapped
- [ ] Reliability targets discussed
- [ ] Failure modes documented
- [ ] Alerts reviewed
- [ ] Runbooks reviewed
- [ ] On-call and escalation confirmed
- [ ] Reliability backlog created

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

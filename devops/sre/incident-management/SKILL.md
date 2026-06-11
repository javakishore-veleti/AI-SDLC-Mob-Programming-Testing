---
name: sre-incident-management-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for incident management design, severity models, escalation paths, communication plans, recovery runbooks, postmortems, and production incident readiness.
---

# Incident Management AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for incident management readiness and production response design.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Incident response process design
- Severity model definition
- Escalation matrix design
- War room workflow
- Customer communication planning
- Recovery runbook creation
- Postmortem template design
- Incident simulation or game day planning

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
| Incident Management Tool | Manage incidents, responders, timelines, and postmortems |
| Chat / Collaboration Tool | Coordinate war rooms and stakeholder updates |
| Observability Platform | Validate alerts, dashboards, and incident triggers |
| Runbook Repository | Store recovery procedures |
| Status Page Tool | Communicate customer impact |
| On-Call Tool | Review rotations and escalation |
| Issue Tracker | Track postmortem action items |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Incident tool admin/read access | Review severity model and workflows |
| Observability access | Validate alert triggers and dashboards |
| On-call schedule access | Review escalation paths |
| Runbook repository access | Review recovery procedures |
| Status page access | Review external communication workflow |
| Service repository access | Link incidents to services and owners |

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

### 1. Incident Scope

Define what types of incidents this process covers.

### 2. Severity Model

Define severity using customer impact, revenue impact, security impact, availability impact, and data integrity impact.

### 3. Escalation Design

Define incident commander, technical lead, communications lead, business stakeholder, and executive escalation.

### 4. War Room Flow

Define:

```text
Detect -> Triage -> Declare -> Communicate -> Mitigate -> Recover -> Review
```

### 5. Postmortem Model

Define timeline, root cause, contributing factors, detection gaps, recovery gaps, action items, owners, and due dates.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for incident management readiness and production response design.

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

- `devops/sre/incident-management/severity-model.md`
- `devops/sre/incident-management/escalation-matrix.md`
- `devops/sre/incident-management/incident-runbook.md`
- `devops/sre/incident-management/communication-template.md`
- `devops/sre/incident-management/postmortem-template.md`

---

## Implementation Readiness Checklist

- [ ] Severity model defined
- [ ] Incident roles defined
- [ ] Escalation paths documented
- [ ] War room process documented
- [ ] Customer communication process defined
- [ ] Recovery runbooks identified
- [ ] Postmortem template created
- [ ] Action item tracking defined

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

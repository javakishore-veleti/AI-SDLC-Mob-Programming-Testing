---
name: architecture-decision-record-governance-mob-programming
description: use this skill to run ai-sdlc mob programming governance sessions for creating, reviewing, approving, superseding, and maintaining architecture decision records and technical decision logs.
---

# Architecture Decision Records AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming governance playbook** for architecture decision records and technical decision governance.

This is not a generic governance checklist. It is a facilitation guide for a cross-functional mob session where Product, Architecture, Engineering, QA, Security, DevOps, Risk, Compliance, Legal, Operations, and AI collaborate to produce governance-ready and implementation-ready outcomes.

The goal is to make governance practical, collaborative, transparent, and traceable without turning it into a late-stage approval bottleneck.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively define, review, approve, or govern:

- Creating ADRs during mob sessions
- Reviewing architecture decisions
- Capturing tradeoffs
- Superseding old decisions
- Linking decisions to implementation tasks
- Maintaining a decision log
- Making decisions audit-ready

Avoid using this playbook for routine status updates or rubber-stamp approvals. Use it when governance decisions require shared understanding, risk clarity, evidence, and accountable ownership.

---

## AI-SDLC Mob Programming Governance Objective

The mob should answer:

```text
What do we need to understand, decide, document, validate, approve,
monitor, and govern before this capability is ready for delivery?
```

The session should produce decision-ready and audit-ready artifacts, not meeting notes.

---

## Required Tools

| Tool | Why It Is Needed |
|---|---|
| GitHub Repository | Source of truth for governance artifacts, decisions, templates, and playbooks |
| GitHub Copilot Chat / AI Assistant | Generate draft governance artifacts, risks, controls, and decision summaries |
| Issue Tracker | Convert governance follow-ups into backlog-ready tasks |
| Architecture Repository / Diagrams | Review architecture context and decision impact |
| Security Tooling | Review vulnerabilities, threats, controls, and posture |
| Policy / Compliance Repository | Validate governance obligations and standards |
| Evidence Repository | Store approval evidence, decisions, exceptions, and audit artifacts |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Repository access | Review and update governance artifacts |
| Architecture documentation access | Validate impacted systems and decisions |
| Security dashboard access | Review findings, threats, controls, and exceptions |
| Compliance repository access | Validate policy obligations and evidence needs |
| Issue tracker access | Create governance follow-up tasks |
| Deployment or change records access | Review release and change impact |
| Audit/evidence storage access | Store governance evidence and approvals |

---

## Ideal Mob Roles

| Role | Responsibility |
|---|---|
| Product Owner / Business Owner | Defines business value, risk appetite, customer impact, and decision priority |
| Business SME | Explains domain rules, exceptions, and operational realities |
| Solution Architect | Reviews architecture choices, system boundaries, and technical tradeoffs |
| Engineering Lead | Validates implementation feasibility and delivery impact |
| QA / Quality Engineer | Defines validation evidence and quality gates |
| Security Engineer | Reviews identity, access, data protection, threat model, and control requirements |
| DevOps / SRE Engineer | Reviews deployability, observability, reliability, and operational controls |
| Risk / Compliance Partner | Reviews policy obligations, control mapping, and evidence expectations |
| Legal / Privacy Partner | Joins when data, contracts, privacy, or regulatory concerns exist |
| AI / Copilot Operator | Generates draft decisions, risks, controls, evidence lists, and artifacts |
| Facilitator | Keeps the session decision-oriented and captures owners, approvals, and follow-ups |

---

## Recommended Session Flow

### 1. Decision Context
Clarify the problem, constraints, business drivers, and technical drivers.

### 2. Options Review
List viable options and compare tradeoffs.

### 3. Decision Selection
Select the option and document why.

### 4. Consequence Review
Capture positive, negative, operational, security, and delivery impacts.

### 5. Lifecycle Management
Define whether the ADR is proposed, accepted, superseded, rejected, or deprecated.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming governance assistant.

Help the team run a governance-focused mob session for architecture decision records and technical decision governance.

Generate:
- required tools
- required access
- ideal participants
- governance decisions required
- risks and controls
- evidence required
- approval path
- policy or compliance considerations
- implementation readiness impacts
- audit-ready deliverables
- backlog-ready governance tasks

Do not generate generic governance notes.
Produce concrete artifacts that can be committed into the repository.
```

---

## Expected Deliverables

The mob session should produce:

- `governance/architecture-decision-records/adr-template.md`
- `governance/architecture-decision-records/decision-log.md`
- `governance/architecture-decision-records/superseded-decisions.md`
- `governance/architecture-decision-records/open-decisions.md`

---

## Governance Readiness Checklist

- [ ] Decision context documented
- [ ] Options compared
- [ ] Decision selected
- [ ] Tradeoffs captured
- [ ] Consequences documented
- [ ] Owners assigned
- [ ] ADR status set
- [ ] Related tasks linked

---

## Definition of Done

The session is complete when:

- Governance scope is clear.
- Required decision owners are identified.
- Risks, controls, and mitigations are documented.
- Required evidence is identified.
- Architecture, security, compliance, and operational impacts are reviewed.
- Approval path is clear.
- Exceptions and open questions are tracked.
- Backlog-ready governance tasks are created.
- Artifacts are ready to commit to the repository.

---

## Principle

Governance in AI-SDLC Mob Programming is not a stage gate at the end.

It is a collaborative design activity that helps teams deliver responsibly, securely, transparently, and with shared accountability.

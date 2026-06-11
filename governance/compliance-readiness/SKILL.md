---
name: compliance-readiness-mob-programming
description: use this skill to run ai-sdlc mob programming governance sessions for compliance readiness, regulatory obligations, control evidence, privacy requirements, audit preparation, and policy alignment.
---

# Compliance Readiness AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming governance playbook** for compliance readiness, control evidence, and regulatory alignment.

This is not a generic governance checklist. It is a facilitation guide for a cross-functional mob session where Product, Architecture, Engineering, QA, Security, DevOps, Risk, Compliance, Legal, Operations, and AI collaborate to produce governance-ready and implementation-ready outcomes.

The goal is to make governance practical, collaborative, transparent, and traceable without turning it into a late-stage approval bottleneck.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively define, review, approve, or govern:

- Compliance review for new capabilities
- Audit preparation
- Privacy and data handling review
- Control evidence planning
- Regulatory impact analysis
- Compliance exception review
- Policy alignment review

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

### 1. Compliance Scope
Identify applicable regulations, policies, customer commitments, and internal standards.

### 2. Data and Process Mapping
Document data types, processing purpose, retention, access, and integrations.

### 3. Control Mapping
Map requirements to controls, owners, and evidence.

### 4. Evidence Planning
Define evidence location, format, owner, and refresh cadence.

### 5. Exception Handling
Capture gaps, exceptions, compensating controls, and approvals.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming governance assistant.

Help the team run a governance-focused mob session for compliance readiness, control evidence, and regulatory alignment.

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

- `governance/compliance-readiness/compliance-scope.md`
- `governance/compliance-readiness/control-mapping.md`
- `governance/compliance-readiness/evidence-plan.md`
- `governance/compliance-readiness/compliance-gap-register.md`
- `governance/compliance-readiness/exception-log.md`

---

## Governance Readiness Checklist

- [ ] Compliance scope identified
- [ ] Data handling reviewed
- [ ] Policy obligations mapped
- [ ] Controls identified
- [ ] Evidence requirements documented
- [ ] Exceptions captured
- [ ] Owners assigned
- [ ] Audit readiness confirmed

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

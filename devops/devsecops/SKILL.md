---
name: devsecops-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for devsecops, shift-left security, pipeline security gates, secrets management, vulnerability management, compliance automation, threat modeling, and secure delivery readiness.
---

# DevSecOps AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for secure delivery and DevSecOps pipeline readiness.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Shift-left security adoption
- Security gate design
- SAST, DAST, SCA, container, and IaC scanning
- Secrets detection and rotation
- Vulnerability triage workflow
- Compliance automation
- Threat modeling

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
| CI/CD Platform | Add security checks to delivery workflow |
| SAST Tool | Review code vulnerabilities |
| SCA Tool | Review dependency vulnerabilities |
| Container Scanner | Review image vulnerabilities |
| IaC Scanner | Review infrastructure misconfigurations |
| Secrets Scanner | Detect leaked credentials |
| Security Dashboard | Review posture, policy, and exceptions |
| Issue Tracker | Track remediation work |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| CI/CD access | Review security gates |
| Security scanner access | Review findings and policies |
| Repo access | Review code and workflow configuration |
| Container registry access | Review images and scan results |
| Secrets manager access | Review secret storage and rotation |
| Compliance dashboard access | Review policy requirements |
| Issue tracker access | Create remediation backlog |

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

### 1. Security Scope

Define application/system in scope, compliance requirements, data sensitivity, threat model needs, and release risk.

### 2. Pipeline Security Design

Define SAST, SCA, container, IaC, secrets, and DAST gates.

### 3. Vulnerability Workflow

Define severity thresholds, blocking rules, exception process, remediation SLA, and ownership.

### 4. Secure Operations

Review secrets rotation, audit logging, runtime security, incident escalation, and compliance evidence.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for secure delivery and DevSecOps pipeline readiness.

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

- `devops/devsecops/security-gate-model.md`
- `devops/devsecops/vulnerability-management.md`
- `devops/devsecops/secrets-management.md`
- `devops/devsecops/threat-model.md`
- `devops/devsecops/compliance-evidence.md`

---

## Implementation Readiness Checklist

- [ ] Security tools identified
- [ ] Blocking gates defined
- [ ] Vulnerability thresholds defined
- [ ] Exception process defined
- [ ] Secrets strategy reviewed
- [ ] Compliance evidence identified
- [ ] Threat model reviewed
- [ ] Security backlog created

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

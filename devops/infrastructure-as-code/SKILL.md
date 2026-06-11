---
name: infrastructure-as-code-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for infrastructure as code using terraform, bicep, cloudformation, pulumi, crossplane, policy-as-code, module design, environment promotion, drift management, and infrastructure delivery readiness.
---

# Infrastructure as Code AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for Infrastructure as Code design, governance, and delivery readiness.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Terraform module design
- Bicep or CloudFormation review
- Pulumi or Crossplane adoption
- IaC repository strategy
- Environment promotion
- Policy-as-code design
- Drift detection
- State management
- Infrastructure security review

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
| IaC Repository | Review modules, environments, and standards |
| Terraform / Bicep / CloudFormation / Pulumi | Validate IaC approach |
| State Backend | Review state storage, locking, and access |
| Policy-as-Code Tool | Review guardrails and compliance |
| CI/CD Platform | Review plan/apply workflow |
| Cloud Provider | Validate deployed infrastructure |
| Security Scanner | Review IaC misconfigurations |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| IaC repo access | Review definitions and modules |
| State backend access | Review state security and locking |
| CI/CD access | Review plan/apply workflow |
| Cloud provider access | Validate resources |
| Policy tool access | Review guardrails |
| Security scanner access | Review IaC findings |
| Secrets manager access | Review sensitive variable handling |

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

### 1. IaC Scope

Define infrastructure components, environments, cloud accounts/subscriptions/projects, ownership model, and compliance constraints.

### 2. Repository and Module Design

Review module boundaries, environment structure, variable strategy, naming standards, tagging standards, and reuse strategy.

### 3. State and Promotion

Review state backend, locking, secrets, plan/apply permissions, promotion workflow, and drift handling.

### 4. Policy and Security

Review policy-as-code, least privilege, encryption, network controls, audit trail, and change approval.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for Infrastructure as Code design, governance, and delivery readiness.

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

- `devops/infrastructure-as-code/iac-repository-strategy.md`
- `devops/infrastructure-as-code/module-design.md`
- `devops/infrastructure-as-code/state-management.md`
- `devops/infrastructure-as-code/policy-as-code.md`
- `devops/infrastructure-as-code/iac-delivery-checklist.md`

---

## Implementation Readiness Checklist

- [ ] IaC scope defined
- [ ] Repository structure reviewed
- [ ] Module strategy defined
- [ ] State backend reviewed
- [ ] Promotion workflow documented
- [ ] Policy-as-code defined
- [ ] Secrets handling reviewed
- [ ] Drift strategy defined
- [ ] Security scanning included

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

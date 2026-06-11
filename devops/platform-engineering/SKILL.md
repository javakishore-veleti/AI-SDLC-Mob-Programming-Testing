---
name: platform-engineering-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for internal developer platforms, golden paths, self-service infrastructure, platform capabilities, developer experience, paved roads, service catalogs, and platform governance.
---

# Platform Engineering AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for internal developer platform and golden path design.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Internal Developer Platform design
- Golden path definition
- Self-service environment provisioning
- Developer onboarding
- Service catalog design
- Platform capability roadmap
- Platform governance
- Developer experience improvement

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
| Developer Portal / Backstage | Review service catalog and developer workflows |
| GitHub / GitLab / Azure DevOps | Review templates, workflows, and onboarding |
| CI/CD Platform | Review reusable pipeline templates |
| Cloud Platform | Review self-service infrastructure capabilities |
| Kubernetes / Runtime Platform | Review platform runtime capabilities |
| IaC Tooling | Review Terraform, Bicep, Crossplane, or Pulumi modules |
| Observability Platform | Review platform-level dashboards and standards |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Platform repositories access | Review golden path templates and modules |
| Developer portal access | Review service catalog and onboarding |
| CI/CD admin access | Review reusable pipeline capabilities |
| Cloud/cluster access | Review self-service infrastructure model |
| IaC registry access | Review reusable modules |
| Observability access | Review platform health dashboards |

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

### 1. Platform User Journey

Map how developers create, deploy, observe, and operate services.

### 2. Golden Path Design

Define supported stacks, templates, security defaults, observability defaults, and deployment model.

### 3. Self-Service Model

Review what teams can provision, approval requirements, guardrails, cost controls, and lifecycle management.

### 4. Governance

Define platform standards without blocking delivery.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for internal developer platform and golden path design.

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

- `devops/platform-engineering/golden-path.md`
- `devops/platform-engineering/service-catalog-model.md`
- `devops/platform-engineering/self-service-infrastructure.md`
- `devops/platform-engineering/developer-experience-review.md`
- `devops/platform-engineering/platform-roadmap.md`

---

## Implementation Readiness Checklist

- [ ] Developer journeys mapped
- [ ] Golden path defined
- [ ] Service catalog model defined
- [ ] Self-service capabilities identified
- [ ] Guardrails documented
- [ ] Security defaults defined
- [ ] Observability defaults defined
- [ ] Platform roadmap created

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

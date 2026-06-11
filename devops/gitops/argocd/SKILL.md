---
name: argocd-gitops-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for argocd, gitops repository strategy, application deployment, environment promotion, drift detection, multi-cluster rollout, rollback, and kubernetes delivery governance.
---

# ArgoCD GitOps AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for ArgoCD and GitOps deployment model design.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Introducing ArgoCD
- GitOps repository design
- Kubernetes application deployment
- Multi-environment promotion
- Multi-cluster deployment
- Drift detection
- Rollback strategy
- ApplicationSet design
- GitOps governance

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
| Git Repository | Source of truth for Kubernetes manifests and GitOps workflow |
| ArgoCD | Review applications, projects, sync policies, and health status |
| Kubernetes Cluster | Validate deployment targets |
| Helm / Kustomize | Define packaging and overlay strategy |
| Secrets Manager | Review secret delivery approach |
| CI/CD Platform | Connect build pipeline to GitOps promotion |
| Observability Platform | Validate post-sync health and alerts |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Git repo admin access | Review repo structure and branch strategy |
| ArgoCD access | Review projects, apps, sync policies, and RBAC |
| Kubernetes read/admin access | Validate namespaces, workloads, and cluster policies |
| Secrets manager access | Review secret injection model |
| CI/CD access | Review image build and promotion workflow |
| Observability access | Validate deployment health checks |

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

### 1. GitOps Scope

Define which applications, environments, and clusters are managed by ArgoCD.

### 2. Repository Strategy

Decide app repo vs environment repo, mono repo vs multi repo, Helm vs Kustomize, overlay model, and promotion branch strategy.

### 3. ArgoCD Design

Define projects, applications, ApplicationSets, sync policies, RBAC, health checks, and drift handling.

### 4. Promotion and Rollback

Define:

```text
Build image -> update manifest -> sync app -> validate health -> promote
```

### 5. Governance

Review approvals, auditability, environment protection, and ownership.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for ArgoCD and GitOps deployment model design.

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

- `devops/gitops/argocd/gitops-repository-strategy.md`
- `devops/gitops/argocd/argocd-application-design.md`
- `devops/gitops/argocd/environment-promotion-flow.md`
- `devops/gitops/argocd/rollback-strategy.md`
- `devops/gitops/argocd/rbac-and-governance.md`

---

## Implementation Readiness Checklist

- [ ] GitOps scope defined
- [ ] Repository strategy selected
- [ ] ArgoCD project model defined
- [ ] Application model defined
- [ ] Sync policy defined
- [ ] Promotion workflow documented
- [ ] Rollback strategy documented
- [ ] RBAC reviewed
- [ ] Operational alerts defined

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

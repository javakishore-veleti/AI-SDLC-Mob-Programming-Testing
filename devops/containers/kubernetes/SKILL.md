---
name: kubernetes-operations-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for kubernetes deployment standards, cluster operations, workload design, autoscaling, ingress, networking, security, observability, cost optimization, and production readiness.
---

# Kubernetes Operations AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for Kubernetes workload and cluster operational readiness.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- Kubernetes workload onboarding
- Cluster readiness review
- Namespace and tenancy design
- Deployment standards
- Autoscaling strategy
- Ingress and networking review
- Resource management
- Kubernetes security baseline
- Production readiness review

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
| Kubernetes Cluster | Review runtime, workloads, namespaces, policies, and resources |
| kubectl / Lens / Kubernetes Dashboard | Inspect workloads and cluster objects |
| Helm / Kustomize | Review deployment packaging |
| Container Registry | Validate image lifecycle and scanning |
| Ingress Controller / Service Mesh | Review traffic routing |
| Observability Platform | Validate workload health, logs, metrics, and traces |
| Secrets Manager | Review secret delivery and rotation |
| Policy Tool | Validate OPA/Gatekeeper/Kyverno policies if used |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Cluster read/admin access | Review workloads, namespaces, policies, and resources |
| Container registry access | Validate images and tags |
| Deployment repo access | Review manifests, Helm charts, or Kustomize overlays |
| Observability access | Review metrics, logs, traces, and alerts |
| Secrets manager access | Review secret handling |
| Network/ingress access | Review routing and TLS configuration |
| Security policy access | Review admission and runtime policies |

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

### 1. Workload Context

Define application purpose, criticality, traffic profile, runtime dependencies, and environment targets.

### 2. Deployment Design

Review deployment type, replica strategy, resource requests and limits, probes, ConfigMaps, secrets, image tagging, and rollout strategy.

### 3. Networking and Traffic

Review services, ingress, TLS, service mesh, network policies, and external dependencies.

### 4. Reliability and Scaling

Review HPA/VPA, pod disruption budgets, node affinity, availability zones, and failure behavior.

### 5. Security and Operations

Review RBAC, secrets, pod security, image scanning, runtime policies, observability, and runbooks.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for Kubernetes workload and cluster operational readiness.

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

- `devops/containers/kubernetes/workload-readiness.md`
- `devops/containers/kubernetes/deployment-standards.md`
- `devops/containers/kubernetes/security-baseline.md`
- `devops/containers/kubernetes/autoscaling-strategy.md`
- `devops/containers/kubernetes/operational-runbook.md`

---

## Implementation Readiness Checklist

- [ ] Workload criticality defined
- [ ] Manifests reviewed
- [ ] Resource requests/limits defined
- [ ] Probes configured
- [ ] Autoscaling reviewed
- [ ] Ingress/TLS reviewed
- [ ] Secrets strategy reviewed
- [ ] RBAC reviewed
- [ ] Observability defined
- [ ] Runbook created

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

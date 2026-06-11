---
name: azure-cloud-deployment-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for azure cloud deployment architecture, identity, networking, compute, kubernetes, observability, security, cost, disaster recovery, and operational readiness.
---

# Azure Cloud Deployment AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for Azure cloud deployment architecture and operational readiness.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- New Azure application deployment
- Azure landing zone review
- Identity and access design
- Network and security design
- Kubernetes or container deployment
- Serverless deployment
- Observability and logging
- Cost and capacity planning
- Disaster recovery and resilience review

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
| Azure Console / Portal | Review cloud resources, identity, networking, compute, and monitoring |
| Infrastructure-as-Code Repository | Review Terraform, Bicep, CloudFormation, or deployment definitions |
| CI/CD Platform | Review cloud deployment pipeline |
| Secrets Manager | Review secret storage and rotation |
| Observability Platform | Review logs, metrics, alerts, and traces |
| Security Center / Cloud Security Tool | Review posture, policies, vulnerabilities, and compliance |
| Cost Management Tool | Review cost allocation and optimization |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Azure read/admin access | Review cloud architecture and resources |
| IAM/identity access | Review permissions, roles, groups, and service principals |
| Network access | Review VPC/VNet, subnets, routing, DNS, firewall rules |
| IaC repo access | Review deployment definitions |
| CI/CD access | Review deployment workflows |
| Observability access | Review monitoring and alerting |
| Security dashboard access | Review policy and posture findings |

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
| Cloud Architect | Reviews provider-specific architecture, identity, networking, and managed services |

---

## Recommended Session Flow

### 1. Cloud Scope

Define application or platform, environments, regions, criticality, and compliance constraints.

### 2. Architecture Review

Review provider-specific services:

```text
Entra ID, VNets, AKS, App Service, Functions, Monitor, Key Vault, Storage, Azure DevOps
```

### 3. Identity and Security

Review human access, service identity, least privilege, secret management, encryption, policy enforcement, and audit logging.

### 4. Network and Runtime

Review network boundaries, private endpoints, load balancing, Kubernetes or compute runtime, scaling model, and high availability.

### 5. Operations

Review monitoring, logging, alerting, backup, disaster recovery, cost management, and runbooks.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for Azure cloud deployment architecture and operational readiness.

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

- `devops/cloud/azure/architecture-review.md`
- `devops/cloud/azure/identity-access-review.md`
- `devops/cloud/azure/networking-review.md`
- `devops/cloud/azure/deployment-readiness.md`
- `devops/cloud/azure/operational-readiness.md`
- `devops/cloud/azure/cost-and-resilience-review.md`

---

## Implementation Readiness Checklist

- [ ] Cloud scope defined
- [ ] Runtime architecture reviewed
- [ ] Identity model reviewed
- [ ] Network model reviewed
- [ ] Security controls reviewed
- [ ] IaC approach reviewed
- [ ] CI/CD integration reviewed
- [ ] Observability defined
- [ ] DR and backup reviewed
- [ ] Cost ownership identified

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

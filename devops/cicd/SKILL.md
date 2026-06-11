---
name: devops-cicd-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for ci/cd pipeline design, build automation, test gates, security scanning, artifact management, deployment approvals, rollback strategy, and release automation across modern engineering teams.
---

# CI/CD AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for CI/CD pipeline design and delivery automation.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- New CI/CD pipeline design
- Pipeline modernization
- Build and test automation
- Security and compliance gates
- Artifact versioning and promotion
- Deployment approval workflow
- Blue/green, canary, or rolling deployments
- Rollback and recovery planning
- Environment promotion strategy

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
| GitHub Actions / Azure DevOps / Jenkins / GitLab CI | Design and validate pipeline workflow |
| Source Code Repository | Review branching, pull request, and merge strategy |
| Artifact Repository | Validate image, package, and version promotion |
| Security Scanner | Define SAST, SCA, container, IaC, and secret scanning gates |
| Test Automation Framework | Define unit, integration, regression, and contract test stages |
| Deployment Platform | Validate deployment targets such as Kubernetes, cloud apps, or VMs |
| Observability Platform | Define post-deployment health checks and rollback signals |
| Issue Tracker | Convert pipeline design into implementation tasks |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Repository admin access | Review branch protection, environments, and workflow permissions |
| CI/CD platform access | Review pipeline configuration and execution history |
| Artifact repository access | Validate package and container promotion |
| Cloud or cluster access | Validate deployment targets |
| Secrets management access | Review pipeline secrets and rotation model |
| Security scanning dashboard access | Review existing vulnerabilities and policies |
| Test reporting access | Review quality gates and current coverage |

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

### 1. Delivery Flow Mapping

Map the current or proposed delivery flow:

```text
Commit -> Build -> Test -> Scan -> Package -> Deploy -> Validate -> Promote
```

### 2. Branching and Promotion Strategy

Decide:

- Trunk-based vs branch-based development
- Pull request gates
- Environment promotion path
- Manual vs automated approvals
- Release tagging strategy

### 3. Pipeline Stage Design

Define pipeline stages:

- Source validation
- Build
- Unit tests
- Static analysis
- Dependency scanning
- Container scanning
- IaC scanning
- Integration tests
- Package creation
- Deployment
- Smoke tests
- Rollback hooks

### 4. Security and Compliance Gates

Decide which findings block delivery and which create backlog items.

### 5. Deployment and Rollback Strategy

Define deployment model, rollback trigger, rollback execution, health checks, and release ownership.

### 6. Readiness Review

Confirm pipeline design can be implemented safely and repeatedly.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for CI/CD pipeline design and delivery automation.

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

- `devops/cicd/pipeline-architecture.md`
- `devops/cicd/pipeline-stage-design.md`
- `devops/cicd/security-gates.md`
- `devops/cicd/deployment-strategy.md`
- `devops/cicd/rollback-plan.md`
- `devops/cicd/implementation-checklist.md`

---

## Implementation Readiness Checklist

- [ ] Branching strategy defined
- [ ] Pipeline stages documented
- [ ] Quality gates defined
- [ ] Security gates defined
- [ ] Artifact versioning defined
- [ ] Secrets strategy reviewed
- [ ] Deployment model selected
- [ ] Rollback strategy documented
- [ ] Post-deployment validation defined
- [ ] Backlog-ready tasks created

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

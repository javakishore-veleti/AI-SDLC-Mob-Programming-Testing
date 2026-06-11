---
name: sre-observability-mob-programming
description: use this skill to run ai-sdlc mob programming sessions for observability design, metrics, logs, traces, dashboards, alerting, correlation ids, telemetry standards, and production diagnostic readiness.
---

# Observability AI-SDLC Mob Programming Playbook

## Purpose

Use this SKILL.md as an **AI-SDLC Mob Programming playbook** for observability, monitoring, logging, tracing, and diagnostic readiness.

This is not a generic DevOps checklist. It is a facilitation guide for a cross-functional mob session where Product, Engineering, QA, Security, SRE, DevOps, Platform, and AI collaborate to produce implementation-ready DevOps artifacts.

The goal is to leave the session with decisions, designs, checklists, risks, and backlog-ready work items.

---

## When to Use This Skill

Use this playbook when the team needs to collaboratively design, review, modernize, or validate:

- New service observability design
- Dashboard standardization
- Alert strategy design
- Logging standards
- Distributed tracing strategy
- Correlation ID design
- OpenTelemetry adoption
- Production diagnostics improvement
- Alert noise reduction

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
| Observability Platform | Review and design metrics, logs, traces, and dashboards |
| OpenTelemetry / Instrumentation Libraries | Define telemetry implementation approach |
| Log Platform | Validate structured logging and searchability |
| Metrics Platform | Define service health and business metrics |
| Tracing Platform | Design cross-service diagnostics |
| Alerting Tool | Define actionable alerts and escalation |
| Service Repository | Add instrumentation requirements to implementation |

---

## Required Logins / Access

| Access | Why It Is Needed |
|---|---|
| Observability dashboard access | Review existing telemetry |
| Log query access | Validate log structure and usefulness |
| Tracing access | Review distributed trace coverage |
| Alert management access | Review alert rules and noise |
| Service repository access | Define instrumentation changes |
| Cloud/cluster access | Review platform-level metrics |

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

### 1. Observability Objective

Define what the team needs to understand in production.

### 2. Signal Design

Define golden signals, business metrics, technical metrics, dependency metrics, error metrics, and saturation metrics.

### 3. Logging Strategy

Define structured log fields, correlation ID, request identifiers, error codes, and sensitive data masking.

### 4. Tracing Strategy

Define trace boundaries, service spans, external dependency spans, sampling strategy, and trace-to-log correlation.

### 5. Alert Strategy

Define alerts that are actionable, owned, and tied to customer impact.

### 6. Dashboard Strategy

Define dashboards for engineering, SRE, operations, and leadership.

---

## GitHub Copilot / AI Prompt

Use this prompt inside GitHub Copilot Chat or another AI assistant with repository context:

```text
Use this SKILL.md as context.

Act as an AI-SDLC Mob Programming assistant.

Help the team run a mob session for observability, monitoring, logging, tracing, and diagnostic readiness.

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

- `devops/sre/observability/telemetry-standards.md`
- `devops/sre/observability/logging-standards.md`
- `devops/sre/observability/tracing-strategy.md`
- `devops/sre/observability/alerting-strategy.md`
- `devops/sre/observability/dashboard-requirements.md`

---

## Implementation Readiness Checklist

- [ ] Critical user journeys identified
- [ ] Metrics defined
- [ ] Logs standardized
- [ ] Trace strategy defined
- [ ] Correlation ID approach defined
- [ ] Alert ownership assigned
- [ ] Dashboards designed
- [ ] Sensitive data masking reviewed
- [ ] Observability tasks created

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

# AI-SDLC Mob Programming Templates

## Purpose

This folder contains reusable templates for converting AI-SDLC Mob Programming sessions into implementation-ready artifacts.

The framework documents explain **how to run the session**.

The SKILL.md playbooks explain **what domain or capability the session is focused on**.

These templates define **what the team should produce**.

---

## Recommended Flow

```text
Framework
  -> SKILL.md Playbook
  -> Mob Programming Session
  -> Templates
  -> Implementation Artifacts
  -> Backlog / Delivery Work
```

---

## Templates Included

| Template | Purpose |
|---|---|
| `session-output-template.md` | Capture the complete output of a mob session |
| `implementation-readiness-template.md` | Determine whether a capability is ready for implementation |
| `architecture-decision-template.md` | Capture architectural decisions made during the session |
| `api-contract-template.md` | Define API contracts produced by the mob |
| `event-contract-template.md` | Define event contracts for asynchronous workflows |
| `test-scenario-template.md` | Capture test scenarios during the session |
| `risk-register-template.md` | Capture risks, assumptions, mitigations, and owners |
| `backlog-story-template.md` | Convert session output into backlog-ready stories |
| `operational-readiness-template.md` | Capture observability, support, rollback, and SRE readiness |
| `mob-session-agenda-template.md` | Plan and facilitate the session |

---

## How to Use

1. Start with the relevant `SKILL.md` playbook.
2. Run the AI-SDLC Mob Programming session.
3. Copy the relevant templates into the domain/use-case folder.
4. Fill them during or immediately after the session.
5. Commit completed artifacts into the repository.
6. Convert action items into GitHub Issues, Jira stories, or Azure DevOps work items.

---

## Example

For Shopify Discount Segmentation:

```text
skills/shopify-headless-middleware/references/discount-segmentation.md
```

Possible outputs:

```text
domains/shopify-headless/use-cases/discount-segmentation-session-output.md
domains/shopify-headless/architecture/discount-api-contract.md
domains/shopify-headless/testing/discount-test-scenarios.md
domains/shopify-headless/use-cases/discount-risk-register.md
domains/shopify-headless/use-cases/discount-implementation-readiness.md
```

---

## Principle

The purpose of these templates is not documentation for documentation's sake.

The purpose is to convert shared understanding into implementation-ready engineering artifacts.

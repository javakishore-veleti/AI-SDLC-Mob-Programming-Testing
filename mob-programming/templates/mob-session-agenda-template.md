# Mob Session Agenda Template

## Session Title

```text
<Capability / Use Case Name>
```

## Session Objective

Describe what the mob must accomplish.

```text
Example:
Design the guest and logged-in customer discount segmentation flow for Shopify Headless middleware and produce implementation-ready outputs.
```

---

## Session Type

Select one or more:

- [ ] Requirements discovery
- [ ] Architecture design
- [ ] API design
- [ ] Event design
- [ ] DevOps readiness
- [ ] SRE readiness
- [ ] Security review
- [ ] Test strategy
- [ ] Implementation planning
- [ ] Incident readiness
- [ ] Release readiness

---

## Recommended Participants

| Role | Participant | Required? | Notes |
|---|---|---:|---|
| Product Owner |  | Yes | Business outcome and priority |
| Business SME |  | Optional | Domain rules and exceptions |
| Architect |  | Yes | System design and dependencies |
| Developer |  | Yes | Technical feasibility |
| QA Engineer |  | Yes | Test strategy and edge cases |
| DevOps / SRE |  | As needed | Reliability, deployment, observability |
| Security Engineer |  | As needed | Identity, access, data, compliance |
| AI / Copilot Operator |  | Yes | Prompting and artifact generation |
| Facilitator |  | Yes | Session flow and decisions |

---

## Required Inputs

- [ ] Business problem statement
- [ ] Existing requirements or tickets
- [ ] Current architecture diagrams
- [ ] Relevant repository files
- [ ] API documentation
- [ ] Existing test cases
- [ ] Known risks or incidents
- [ ] Required access list
- [ ] Relevant SKILL.md playbook

---

## Timeboxed Agenda

| Time | Activity | Outcome |
|---:|---|---|
| 5 min | Objective and scope | Shared understanding of session goal |
| 10 min | Business framing | Problem statement and success criteria |
| 15 min | Domain discovery | Actors, systems, rules, constraints |
| 20 min | Architecture discussion | System boundaries and decisions |
| 20 min | API/event design | Draft contract |
| 15 min | Test strategy | Test scenario matrix |
| 10 min | Risk review | Risk register |
| 10 min | Readiness review | Implementation checklist |
| 5 min | Closeout | Owners and next steps |

---

## AI / Copilot Prompt

```text
Use the relevant SKILL.md playbook and this session agenda.

Act as an AI-SDLC Mob Programming assistant.

Help the team facilitate this session.

Capture:
- decisions
- assumptions
- open questions
- risks
- API or event contracts
- test scenarios
- implementation checklist
- backlog-ready tasks
```

---

## Session Rules

- Focus on producing artifacts, not meeting notes.
- Validate AI-generated output with human owners.
- Capture open questions separately from decisions.
- Identify owners for unresolved items.
- Do not leave without a concrete next step.

---

## Expected Outputs

- [ ] Session output summary
- [ ] Architecture decisions
- [ ] API/event contract
- [ ] Test scenarios
- [ ] Risk register
- [ ] Implementation readiness checklist
- [ ] Backlog-ready stories

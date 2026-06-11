# Operational Readiness Template

## Capability / Service

```text
<Service, feature, integration, platform, or workflow>
```

## Related SKILL.md

```text
<Path to related SKILL.md>
```

---

## Service Ownership

| Area | Owner |
|---|---|
| Product Owner |  |
| Engineering Owner |  |
| SRE / Operations Owner |  |
| Security Owner |  |
| Support Owner |  |

---

## Runtime Overview

| Area | Details |
|---|---|
| Runtime platform |  |
| Deployment method |  |
| Environment(s) |  |
| Dependencies |  |
| Criticality |  |
| Customer impact |  |

---

## Observability

### Logs

- [ ] Structured logs defined
- [ ] Correlation ID included
- [ ] Error codes included
- [ ] Sensitive data masking reviewed

### Metrics

| Metric | Purpose | Alert? |
|---|---|---|
|  |  | Yes / No |

### Traces

- [ ] Distributed tracing enabled
- [ ] External dependency spans included
- [ ] Trace-to-log correlation available

### Dashboards

| Dashboard | Audience | Purpose |
|---|---|---|
|  | Engineering / SRE / Business |  |

---

## Alerting

| Alert | Trigger | Severity | Owner | Runbook |
|---|---|---|---|---|
|  |  |  |  |  |

---

## SLI / SLO

| SLI | SLO Target | Measurement Source |
|---|---|---|
| Availability |  |  |
| Latency |  |  |
| Error Rate |  |  |

---

## Failure Handling

| Failure Scenario | Expected Behavior | Alert Required? | Recovery |
|---|---|---|---|
| Dependency failure |  | Yes / No |  |
| Timeout |  | Yes / No |  |
| Data issue |  | Yes / No |  |
| Deployment failure |  | Yes / No |  |

---

## Runbook

| Procedure | Link / Notes |
|---|---|
| Restart / recover |  |
| Rollback |  |
| Scale up/down |  |
| Dependency failure |  |
| Incident escalation |  |

---

## Deployment Readiness

- [ ] Deployment strategy defined
- [ ] Rollback strategy defined
- [ ] Feature flag strategy reviewed
- [ ] Smoke tests defined
- [ ] Post-deployment validation defined
- [ ] Support team informed

---

## Support Readiness

- [ ] Known failure scenarios documented
- [ ] Support escalation path defined
- [ ] Customer communication process defined
- [ ] Incident severity guidance defined

---

## Final Operational Readiness Decision

- [ ] Ready for production
- [ ] Ready with risks
- [ ] Not ready
- [ ] Blocked

Decision Notes:

```text

```

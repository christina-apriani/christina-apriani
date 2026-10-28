<div align="center">

# 🔵 AEGIS — Incident Response Command Center

**Run an incident from declaration to post-mortem on the NIST SP 800-61 lifecycle.**

Live, phase-based playbooks. Timeline reconstruction. Communications tracking.
Resolution metrics. Auto-generated post-incident reviews.

![Team](https://img.shields.io/badge/team-BLUE-2e9bff?style=flat-square)
![Framework](https://img.shields.io/badge/NIST-SP%20800--61-5fb4ff?style=flat-square)
![ATT&CK](https://img.shields.io/badge/ATT%26CK-v20-5fb4ff?style=flat-square)
![Stack](https://img.shields.io/badge/stack-zero%20dependency-0f1620?style=flat-square)

*Authored by **Christina Apriani***

</div>

---

## The idea

When an incident hits, the difference between a contained event and a breach is whether responders have a
structured path and a single source of truth. AEGIS gives the incident commander exactly that: declare the
incident, instantiate the right playbook as a live checklist, drive it through the four NIST phases, and keep
the timeline and communications in one place. When it closes, the review writes itself.

Playbooks contain **response actions** (isolate, preserve, eradicate, recover). This is defensive IR tooling.

## Features

| Area | What you get |
|---|---|
| **Declare & classify** | Create an incident, pick a playbook, set severity (SEV-1 → SEV-4). |
| **Lifecycle stepper** | NIST SP 800-61r2 phases: Preparation → Detection & Analysis → Containment, Eradication & Recovery → Post-Incident Activity. |
| **Live playbooks** | Five ready playbooks (ransomware, BEC, data exfiltration, phishing, account compromise), each a phased checklist with progress tracking. |
| **Timeline** | Append-only incident timeline; every phase change, step, and comm is recorded automatically. |
| **Communications** | Log escalations to leadership, legal, comms, and affected teams. |
| **Metrics** | Active count, SEV-1/2 load, median time to resolve, time to containment. |
| **PIR generator** | One-click post-incident review with timeline, metrics, what-worked, and action items. |

## Playbook library

- 🔒 **Ransomware / Destructive Impact** — `T1486`, `T1490`
- 📧 **Business Email Compromise** — `T1566`, `T1078`
- 📤 **Data Exfiltration** — `T1041`, `T1567`
- 🎣 **Phishing Campaign** — `T1566`
- 🔑 **Account Compromise** — `T1078`, `T1110`

Each playbook maps its actions to the NIST phases, so progress is always visible against the lifecycle.

## Run it

```bash
open index.html            # or xdg-open / start
# or:  python3 -m http.server 8080
```

No dependencies. Incidents persist in `localStorage`.

## Responsible use

> This is a coordination tool for authorized incident responders. The playbook actions are defensive.
> Treat real incident data according to your organization's handling and privacy requirements.

## Roadmap

- [ ] SLA clocks and breach warnings per severity
- [ ] Evidence/chain-of-custody register per incident
- [ ] Import detections that fired from the SENTINEL catalog
- [ ] Tabletop mode for scheduled exercises

---

<div align="center">
<sub>Part of the Christina Apriani cyber security portfolio · Blue Team track</sub>
</div>

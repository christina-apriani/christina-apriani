<div align="center">

# 🔴 ATLAS — Adversary Emulation Planner

**Threat-informed engagement design, aligned to MITRE ATT&CK v20**

Turn a threat hypothesis into a defensible, scoped emulation plan. Map adversary behaviors
across all 15 Enterprise tactics and bridge every TTP to the telemetry defenders should see.

![Team](https://img.shields.io/badge/team-RED-ff3b47?style=flat-square)
![ATT&CK](https://img.shields.io/badge/ATT%26CK-v20-ff6b74?style=flat-square)
![Scope](https://img.shields.io/badge/scope-planning%20only-242a36?style=flat-square)
![Stack](https://img.shields.io/badge/stack-zero%20dependency-13161d?style=flat-square)

*Authored by **Christina Apriani***

</div>

---

## Why this exists

Most red team work fails not at execution but at planning. Scope creep, missing de-confliction,
untracked behaviors, and reports that defenders cannot act on. ATLAS fixes the front of the kill chain:
it forces every emulated behavior to be **named, scoped, prioritized, and tied to a detection opportunity
before anyone touches a keyboard.**

It is a planning and coordination surface. It holds **no exploit code, payloads, or execution tooling.**
That is deliberate. A public engagement artifact should prove methodology, not ship weapons.

## What it does

| Capability | Detail |
|---|---|
| **Threat profiling** | Seed a plan from documented adversary profiles (APT29, FIN7, Lazarus, APT28, Scattered Spider) drawn from public ATT&CK Groups data. |
| **ATT&CK v20 matrix** | Interactive 15-tactic board (post Defense-Evasion split into Stealth `TA0005` + Defense Impairment `TA0112`). Click to add or remove techniques. |
| **Blue-team bridge** | Every technique carries its expected telemetry and a detection opportunity, so purple hand-off is built in. |
| **Rules of engagement** | Six mandatory safety gates with explicit de-confliction and simulated-impact controls. |
| **Readiness scoring** | Live kill-chain completeness, tactic breadth, and ROE sign-off metrics. |
| **Portable output** | Export the whole plan to structured JSON, or print it for approval sign-off. |

## The 15 ATT&CK v20 tactics covered

`Reconnaissance` · `Resource Development` · `Initial Access` · `Execution` · `Persistence` ·
`Privilege Escalation` · `Stealth` · `Defense Impairment` · `Credential Access` · `Discovery` ·
`Lateral Movement` · `Collection` · `Command & Control` · `Exfiltration` · `Impact`

## Run it

No build step. No dependencies. No server required.

```bash
# Option 1 — open directly
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Option 2 — serve locally
python3 -m http.server 8080
# then visit http://localhost:8080
```

State persists in your browser via `localStorage`. Nothing leaves the machine.

## Design notes

- Single self-contained HTML file. Vanilla JS, no framework, no external calls.
- Dark operations-console aesthetic with a red-team signature palette.
- Right-click any technique in the matrix for its detection detail.
- Fully responsive; the TTP matrix scrolls horizontally on narrow screens.

## Responsible use

> This tool is for **authorized** adversary emulation only. Run emulation activities exclusively
> against systems you own or have explicit written permission to test, under signed rules of
> engagement. Destructive-impact techniques (`T1486`, `T1490`) stay **simulated** unless separately
> approved in writing.

## Roadmap

- [ ] Import/merge an ATT&CK Navigator layer
- [ ] Per-technique success-criteria templates
- [ ] Multi-operator plan collaboration
- [ ] Coverage diff against the detection catalog from the Purple Team suite

---

<div align="center">
<sub>Part of the Christina Apriani cyber security portfolio · Red Team track</sub>
</div>

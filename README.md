<div align="center">

# Christina Apriani

### Head of Cyber Security · Red / Blue / Purple Team

**Offensive proof. Defensive depth. Measured in the middle.**

A portfolio of six operational tooling projects across the full security spectrum.
Every project is hands-on, interactive, aligned to **MITRE ATT&CK v20**, and built to run with zero dependencies.

![Red Team](https://img.shields.io/badge/RED-adversary%20emulation-ff3b47?style=for-the-badge)
![Blue Team](https://img.shields.io/badge/BLUE-detection%20%26%20response-2e9bff?style=for-the-badge)
![Purple Team](https://img.shields.io/badge/PURPLE-validation-a855f7?style=for-the-badge)

![ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-v20-0b0e14?style=flat-square)
![CVSS](https://img.shields.io/badge/CVSS-v3.1-0b0e14?style=flat-square)
![NIST](https://img.shields.io/badge/NIST-SP%20800--61-0b0e14?style=flat-square)
![Sigma](https://img.shields.io/badge/Detections-Sigma-0b0e14?style=flat-square)

</div>

---

## How I think about security

Red teams prove a path exists. Blue teams see and stop it. Purple teams prove the two are actually connected.
A security leader has to operate across all three and turn the work into something a board can act on. These six
projects are that practice, made tangible.

A note on scope: this is a **public** portfolio, so every project is methodology, detection, and response tooling.
There are no exploits, payloads, or malware here, by design. Live weaponry does not belong on a public profile;
rigor, measurement, and defensible process do.

---

## 🔴 Red Team

> Offensive methodology, scoping, and reporting. Planning surfaces, not weapons.

| Project | What it is |
|---|---|
| **[ATLAS — Adversary Emulation Planner](./red-team/adversary-emulation-planner)** | Build a threat-informed emulation plan across all 15 ATT&CK v20 tactics. Seed from documented actor profiles, attach a detection opportunity and a safety gate to every behavior, export for sign-off. |
| **[SPECTRE — Engagement Ops](./red-team/redteam-engagement-ops)** | The console a red team lead runs an engagement from: findings register, a real **CVSS v3.1** calculator, risk heatmap, remediation tracker, and an auto-generated executive report. |

## 🔵 Blue Team

> Detection engineering and incident response. The defender's craft, operationalized.

| Project | What it is |
|---|---|
| **[SENTINEL — Detection Engineering Lab](./blue-team/detection-engineering-lab)** | A **Sigma** rule library mapped to ATT&CK, a live rule builder, a coverage view, and a 0–100 detection maturity score. Biased toward the top of the Pyramid of Pain. |
| **[AEGIS — Incident Response Command Center](./blue-team/incident-response-center)** | Run an incident on the **NIST SP 800-61** lifecycle: live phased playbooks, timeline reconstruction, communications tracking, resolution metrics, and a one-click post-incident review. |

## 🟣 Purple Team

> Where offense and defense are reconciled and measured.

| Project | What it is |
|---|---|
| **[PRISM — ATT&CK Coverage Navigator](./purple-team/attack-coverage-navigator)** | Map every technique as tested, detected, validated, or a gap. Quantify coverage, surface blind spots, and build a prioritized hardening backlog. Exports a Navigator layer. |
| **[CRUCIBLE — Detection Validation Platform](./purple-team/detection-validation-platform)** | Run detection validation cycles, record detected / partial / missed outcomes, track **MTTD**, and trend detection effectiveness cycle over cycle. |

---

## The projects work as one system

```
   ATLAS plans the emulation  ──►  SPECTRE runs the engagement
            │                               │
            ▼                               ▼
     exercised techniques  ─────►  PRISM coverage navigator  ◄─── SENTINEL authors detections
                                           │                               ▲
                                           ▼                               │
                                  CRUCIBLE validates & measures  ──────────┘
                                           │
                                           ▼
                                  AEGIS responds when it is real
```

Red proves the path. Blue builds the detection. Purple confirms the loop closed. The leader reports the result.

---

## Running any project

Every project is a single self-contained page with no build step and no dependencies.

```bash
cd <project-folder>
python3 -m http.server 8080      # then open http://localhost:8080
# or simply open index.html in a browser
```

State is stored locally in the browser. Nothing is transmitted anywhere.

## Technical standards used

- **MITRE ATT&CK v20** (Oct 2026) — 15 Enterprise tactics, including the Stealth / Defense Impairment split
- **CVSS v3.1** — base-score math per the FIRST.org specification
- **NIST SP 800-61r2** — incident response lifecycle
- **Sigma** — vendor-agnostic detection format
- **Pyramid of Pain** — detection prioritization

---

<div align="center">

**Christina Apriani** · Head of Cyber Security
*Red Team · Blue Team · Purple Team · Incident Response*

<sub>All projects are defensive and methodology-focused. For authorized use only.</sub>

</div>

<div align="center">

# 🔴 SPECTRE — Red Team Engagement Ops

**The console a red team lead runs an engagement from.**

Track findings, score them with a real CVSS v3.1 calculator, plot risk,
drive remediation, and generate an executive summary in one place.

![Team](https://img.shields.io/badge/team-RED-ff3b47?style=flat-square)
![CVSS](https://img.shields.io/badge/CVSS-v3.1-ff6b74?style=flat-square)
![ATT&CK](https://img.shields.io/badge/ATT%26CK-v20-ff6b74?style=flat-square)
![Stack](https://img.shields.io/badge/stack-zero%20dependency-13161d?style=flat-square)

*Authored by **Christina Apriani***

</div>

---

## The problem it solves

Findings scattered across spreadsheets, scores argued by vibe, and a report written from scratch at 2am
the night before the debrief. SPECTRE replaces that with one operating surface that keeps the whole
engagement consistent from first finding to board-ready summary.

Findings are recorded at a **decision-grade** abstraction: what was validated, the business impact, and the
fix. No exploitation walkthroughs. Technical detail belongs in a separate NDA-bound package, not a public tool.

## Features

| Area | What you get |
|---|---|
| **CVSS v3.1 calculator** | All eight base metrics, scope-aware Privileges Required, official FIRST round-up, live vector string, and qualitative rating. |
| **Findings register** | Severity, status, affected asset, ATT&CK technique, observation, and remediation per finding. Filter by severity and status. |
| **Risk heatmap** | Likelihood × impact grid auto-populated from each finding's CVSS vector. |
| **Remediation tracker** | Open items sorted by score, one-click status transitions, live remediation percentage. |
| **ATT&CK coverage** | Which tactics the engagement actually exercised, mapped to ATT&CK v20. |
| **Executive report** | Auto-generated summary with risk posture, top findings, coverage, and strategic recommendations. Copy or export. |

## About the CVSS math

The base-score engine implements the [FIRST.org CVSS v3.1](https://www.first.org/cvss/v3-1/specification-document)
specification exactly: impact sub-score, scope-dependent exploitability, the `1.08` scope-changed multiplier, and
the integer-based round-up function. Scores you get here match the official calculator.

Severity bands: `None 0.0` · `Low 0.1–3.9` · `Medium 4.0–6.9` · `High 7.0–8.9` · `Critical 9.0–10.0`.

## Run it

```bash
open index.html            # or xdg-open / start
# or:  python3 -m http.server 8080
```

Zero dependencies. All state lives in your browser `localStorage`; nothing is transmitted.

## Responsible use

> Record findings only from engagements you are authorized to perform. Keep the public register at a
> decision-grade abstraction. Deliver reproduction detail to the remediation team through a controlled channel.

## Roadmap

- [ ] CVSS v4.0 scoring toggle
- [ ] Retest / delta view against a previous report
- [ ] SLA clocks per severity tier
- [ ] One-click push of exercised techniques into the Purple Team coverage navigator

---

<div align="center">
<sub>Part of the Christina Apriani cyber security portfolio · Red Team track</sub>
</div>

<div align="center">

# 🔵 SENTINEL — Detection Engineering Lab

**A Sigma-first workbench for building, scoring, and measuring detections.**

A curated rule library mapped to MITRE ATT&CK v20, a live Sigma rule builder,
a coverage view that tells the honest truth, and a detection maturity score.

![Team](https://img.shields.io/badge/team-BLUE-2e9bff?style=flat-square)
![Format](https://img.shields.io/badge/format-Sigma-5fb4ff?style=flat-square)
![ATT&CK](https://img.shields.io/badge/ATT%26CK-v20-5fb4ff?style=flat-square)
![Stack](https://img.shields.io/badge/stack-zero%20dependency-0f1620?style=flat-square)

*Authored by **Christina Apriani***

</div>

---

## The idea

Detection engineering only works when it is treated as code: version-controlled, mapped to a threat model,
tuned against false positives, and measured. SENTINEL is that practice in a single page. Every rule is written
in **Sigma**, the vendor-agnostic detection format, so it converts to Splunk, Elastic, Microsoft Sentinel, or
any backend.

This is **defensive** content. Rules describe the log patterns a SIEM should alert on. There is no attack tooling.

## Features

| Area | What you get |
|---|---|
| **Rule library** | 12 production-style detections across the kill chain, each with ATT&CK mapping, confidence level, data source, status, and false-positive notes. |
| **Live Sigma builder** | Author a rule from a form and watch valid Sigma YAML render in real time. Edit any library rule the same way. |
| **Coverage view** | Rule count per ATT&CK tactic and per data source, so gaps are visible, not assumed. |
| **Maturity score** | A weighted 0–100 score from tactic breadth, data-source diversity, stable-rule count, and FP tuning. |
| **Pyramid of Pain** | Visualizes how much the catalog leans on behavior-level detection versus brittle indicators. |
| **Export** | Download the whole catalog as a single multi-document Sigma bundle. |

## Detection philosophy

SENTINEL biases toward the top of the [Pyramid of Pain](https://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html):
behavior and TTP-level rules that are expensive for an adversary to evade, rather than IPs and hashes that change
in minutes. Every rule declares its false positives up front, because an untuned rule is a future ignored alert.

## Sample rule

```yaml
title: Suspicious LSASS Memory Access
status: stable
author: Christina Apriani
logsource:
  product: windows
  category: process_access
detection:
  selection:
    TargetImage|endswith: '\lsass.exe'
    GrantedAccess|contains: ['0x1010','0x1410']
    SourceImage|contains: '\temp\'
  condition: selection
falsepositives:
  - Endpoint protection and backup agents reading LSASS
level: critical
tags:
  - attack.credential_access
  - attack.t1003.001
```

## Run it

```bash
open index.html            # or xdg-open / start
# or:  python3 -m http.server 8080
```

No dependencies. The catalog persists in `localStorage`.

## Roadmap

- [ ] One-click Sigma → Splunk / KQL translation preview
- [ ] Detection test-coverage status from the Purple Team validation platform
- [ ] Rule deprecation lifecycle and change log
- [ ] ATT&CK Navigator layer export of covered techniques

---

<div align="center">
<sub>Part of the Christina Apriani cyber security portfolio · Blue Team track</sub>
</div>

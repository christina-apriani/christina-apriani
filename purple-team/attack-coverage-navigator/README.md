<div align="center">

# 🟣 PRISM — ATT&CK Purple Coverage Navigator

**The single picture a purple team lives by: what was tested, what was detected, and the gap between.**

Map every ATT&CK v20 technique to a coverage state, quantify detection and validation,
and turn blind spots into a ranked hardening backlog.

![Team](https://img.shields.io/badge/team-PURPLE-a855f7?style=flat-square)
![ATT&CK](https://img.shields.io/badge/ATT%26CK-v20-c77dff?style=flat-square)
![Export](https://img.shields.io/badge/export-Navigator%20layer-c77dff?style=flat-square)
![Stack](https://img.shields.io/badge/stack-zero%20dependency-141022?style=flat-square)

*Authored by **Christina Apriani***

</div>

---

## Why it matters

A red team proves an attack works. A blue team believes it has detection. The only honest way to know is to
line them up technique by technique. PRISM is that alignment surface. It makes the uncomfortable truth visible:
the techniques that were tested and produced **no alert**. Those are the paths an adversary already has and the
defender cannot see.

The whole purpose of a purple-team cycle is to turn **red cells green.**

## The four states

| State | Meaning | Action |
|---|---|---|
| ⬛ **Untested** | Never emulated, no detection assumed | Blind spot — schedule it |
| 🟥 **Tested, not detected** | Emulated and produced no alert | Confirmed gap — top priority |
| 🟦 **Detected, not tested** | Detection exists but unproven | Validate it in the next cycle |
| 🟩 **Validated** | Tested and reliably detected | The target state |

Click any technique in the matrix to cycle its state.

## Features

- **Full ATT&CK v20 matrix** across all 15 tactics with per-tactic mini coverage bars.
- **Live metrics**: detection coverage, validation rate, confirmed gaps, blind spots, techniques tested.
- **Analytics view**: coverage donut, state breakdown, and per-tactic stacked coverage bars.
- **Prioritized backlog**: auto-ranked (P1 confirmed gaps → P2/P3 blind spots) with a recommended action per item.
- **ATT&CK Navigator layer export**: download a JSON layer compatible with the MITRE ATT&CK Navigator.

## Run it

```bash
open index.html            # or xdg-open / start
# or:  python3 -m http.server 8080
```

No dependencies. Coverage state persists in `localStorage`.

## How it fits the suite

PRISM is the hinge of the purple program. Feed it the techniques exercised by the Red Team engagement, and the
detections authored in the Blue Team SENTINEL lab. What stays red becomes the backlog that the Detection
Validation platform then closes and re-tests.

## Roadmap

- [ ] Import an ATT&CK Navigator layer to pre-seed state
- [ ] Trend coverage across successive purple cycles
- [ ] Per-technique notes and evidence links
- [ ] Sync directly with the Detection Validation platform

---

<div align="center">
<sub>Part of the Christina Apriani cyber security portfolio · Purple Team track</sub>
</div>

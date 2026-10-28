<div align="center">

# 🟣 CRUCIBLE — Detection Validation Platform

**Purple team as a measurable loop: emulate, measure, tune, re-test.**

Run detection validation cycles, record detected / partial / missed outcomes,
track time-to-detect, and trend detection effectiveness over time.

![Team](https://img.shields.io/badge/team-PURPLE-a855f7?style=flat-square)
![ATT&CK](https://img.shields.io/badge/ATT%26CK-v20-c77dff?style=flat-square)
![Metric](https://img.shields.io/badge/metric-MTTD-c77dff?style=flat-square)
![Stack](https://img.shields.io/badge/stack-zero%20dependency-141022?style=flat-square)

*Authored by **Christina Apriani***

</div>

---

## The idea

Coverage maps tell you where you stand once. CRUCIBLE tells you whether you are getting better. Each purple
cycle emulates a set of ATT&CK behaviors in an authorized lab, records whether the expected detection fired and
how fast, and plots the trend. A detection that passed last cycle but regressed this cycle is caught here.

It records **test outcomes and metrics**. There is no offensive content.

## The three outcomes

| Outcome | Meaning |
|---|---|
| 🟩 **Detected** | The expected alert fired. Record the time to detect. |
| 🟨 **Partial** | Telemetry was logged but no alert fired, or detection was manual/late. |
| 🟥 **Missed** | No telemetry at all. A true blind spot. |

## Features

- **Validation runs** — technique, expected detection, data source, outcome, MTTD, and notes per test.
- **Cycle dashboard** — detection rate ring, outcome mix, average MTTD, and missed count for the current cycle.
- **Trend chart** — detection rate and average MTTD plotted across every cycle, so regression and improvement are visible.
- **Cycle report** — auto-generated summary with headline metrics, delta versus the previous cycle, open items, and recommendations.
- **Metrics that matter** — MTTD treated as a service-level metric, not an afterthought.
- **Export** — full validation dataset to JSON.

> The platform ships with three cycles of example data so the trend view is populated on first open.
> Use **Reset** behavior by clearing runs, or start fresh with your own tests. Everything persists in `localStorage`.

## The purple loop, operationalized

```
  Red emulates a technique
            │
            ▼
  CRUCIBLE records: did detection fire?  →  MTTD captured
            │
     detected?  ── no ──►  Blue authors / tunes a detection (SENTINEL)
            │ yes                     │
            ▼                         ▼
  Coverage navigator (PRISM) marks it validated  ◄── re-test next cycle
```

## Run it

```bash
open index.html            # or xdg-open / start
# or:  python3 -m http.server 8080
```

No dependencies.

## Roadmap

- [ ] Per-technique regression alerts across cycles
- [ ] SLA target lines on the MTTD trend
- [ ] Import the exercised-technique set from the Red Team engagement
- [ ] Push validated detections straight into the PRISM coverage layer

---

<div align="center">
<sub>Part of the Christina Apriani cyber security portfolio · Purple Team track</sub>
</div>

# OA3D Framework
### Modernize Always-On Platforms Without Drama

> *Modernizing an always-on platform isn't a technology problem; it's a risk governance problem. Modernization efforts fail not because teams lack skill, but because risk stays implied and decisions are made without clear gates, proof points, and blast-radius control.*

**OA3D** (Orient → Assess → Decide → De-Risk → Deliver) is a decision-and-delivery framework for replacing or stabilizing fragile, revenue-critical platforms — with explicit risk control, proof-backed gates, and weekly executive visibility.

Developed and maintained by [Tower Workshop](https://github.com/TheTowerworkshop).

---

## The Core Problem

Always-on modernization fails in a consistent pattern:

1. **Competing narratives.** Teams disagree on root causes, critical dependencies, and how fragile the system actually is.
2. **Implied risk.** Risks are discussed but never expressed as explicit conditions with owners and acceptance criteria.
3. **Heroic cutovers.** Major changes rely on confidence rather than rehearsed rollback and blast-radius containment.
4. **Leadership opacity.** Executives receive status updates, not concrete evidence.

The result: rising incidents, delayed timelines, vendor leverage loss, and a growing fear of touching the system at all.

**OA3D interrupts that pattern.**

---

## When OA3D Is Most Necessary

Use this framework when one or more of the following is true:

- Incident frequency or severity is increasing
- An EOL, renewal, audit, launch, or contract milestone is forcing action
- The vendor relationship is losing leverage
- Teams are technically capable but organizationally fragmented
- Leadership is saying: *"If we touch it, it might go down."*

**OA3D is not for:** greenfield builds, nice-to-have upgrades, or situations where downtime is acceptable.

---

## The Framework: Five Verbs, One Governable Path

Each phase produces a small set of artifacts and has explicit exit criteria — so the organization does not advance on hope.

---

### Phase 1 — Orient

**Purpose:** Define the decision the effort must enable, the mission threads that cannot break, and the constraints that define safe change.

**Orient answers three questions:**
1. What is the single decision this work must enable?
2. What mission threads cannot fail — and what does "down" actually mean for each?
3. What are the constraints that define our safe-change envelope?

**Key artifacts:**
- **Decision Anchor** — the one decision the entire effort is built to enable (invest / replace / extend / sequence)
- **Mission Thread Map (Tier-0 / Tier-1)** — the user journeys or operational flows that cannot fail, with failure definitions
- **Safe Change Envelope** — explicit constraints: what cannot break, what cannot be exposed, what must be validated before production

> ⚠️ **A note on the Decision Anchor:** If there is no named decision owner, there is no modernization. The single most common reason these efforts stall is the absence of one person accountable for the next decision.

📄 *[Starter worksheet → `worksheets/01-orient.md`](worksheets/01-orient.md)*

---

### Phase 2 — Assess

**Purpose:** Replace competing opinions with evidence — current reliability posture, maturity baseline, and material risks.

**Assess answers three questions:**
1. What is the current reliability and fragility posture?
2. What are the material risks, and how do they propagate?
3. What forcing functions (EOL, renewal, audit, compliance) constrain the timeline?

**Key artifacts:**
- **Reliability Posture Summary** — incident trends, fragility indicators, MTTR/MTBF if available
- **Risk Register** — risks expressed in plain language with blast radius, failure propagation, and owner
- **Blast Radius Map** — what breaks if each Tier-0/Tier-1 thread fails, and what is the downstream impact
- **Maturity Baseline** — current-state scoring across key dimensions (see [tech-maturity-framework](https://github.com/TheTowerworkshop/tech-maturity-framework))

**Evidence standards:**
Strong evidence includes: source code repositories, CI/CD pipelines, monitoring dashboards, runbooks, architecture diagrams (current state), logs, metrics, access controls, and technical debt registers.

Weak evidence includes: verbal assurances without artifacts, future plans presented as current state, single-person claims not corroborated by any artifact.

> *Absence of evidence is evidence. Document it explicitly.*

📄 *[Starter worksheet → `worksheets/02-assess.md`](worksheets/02-assess.md)*

---

### Phase 3 — Decide

**Purpose:** Convert evidence into a credible, time-bound path forward that leadership can approve and govern.

**Decide answers three questions:**
1. What are the viable options?
2. What are the tradeoffs?
3. What sequence best manages risk within the safe-change envelope?

**Key artifacts:**
- **Option Set (2–3 paths)** — each option with explicit tradeoffs, not just descriptions
- **Tradeoff Table** — risk movement, effort, timeline, and sequencing per option
- **Decision Statement** — the selected path, the rationale, and who owns it

> ⚠️ **Exit criteria:** If teams are still debating architecture patterns, you are not in Decide. If you can articulate risk movement and sequencing clearly, you are ready. An option must be explicitly selected with documented tradeoffs before moving forward. Preference is not a decision framework.

📄 *[Starter worksheet → `worksheets/03-decide.md`](worksheets/03-decide.md)*

---

### Phase 4 — De-Risk

**Purpose:** Make change safe through proof points, blast-radius controls, and explicit go/no-go gates — before production bets.

Most modernization failures happen not because the strategy was wrong, but because proof was assumed instead of demonstrated. De-Risk converts confidence into verification.

**De-Risk answers three questions:**
1. What must be true before we proceed?
2. How will we prove it?
3. What happens if we are wrong?

**Key artifacts:**
- **Go/No-Go Gate Definitions** — explicit conditions with acceptance criteria (not "we think it's ready")
- **Evidence Plan** — how each gate condition will be demonstrated before production exposure
- **Rollback Plan** — documented, rehearsed, not theoretical

📄 *[Starter worksheet → `worksheets/04-derisk.md`](worksheets/04-derisk.md)*

---

### Phase 5 — Deliver

**Purpose:** Execute with control through a 30–90 day runnable plan and weekly executive visibility.

Delivery is not a sprint. It is a disciplined sequence of gated moves that keeps risk visible and steerable at the executive level.

**Key artifacts:**
- **Runnable Plan** — 30–90 day (or longer) sequence tied to gates and decision checkpoints
- **Weekly Exec Visibility Cadence** — a standing format that shows progress and risk movement, not just status
- **Cutover Plan** — sequenced, gate-controlled, with rehearsed rollback at each meaningful exposure

📄 *[Starter worksheet → `worksheets/05-deliver.md`](worksheets/05-deliver.md)*

---

## Starter Worksheets

The `worksheets/` folder contains Markdown-based starter templates for each phase. They are intentionally minimal — designed to produce a useful draft artifact in a working session, not to become documentation theater.

| File | Phase | What It Produces |
|---|---|---|
| `worksheets/01-orient.md` | Orient | Decision Anchor, Mission Thread Map, Safe Change Envelope |
| `worksheets/02-assess.md` | Assess | Risk Register, Blast Radius Map, Evidence Log |
| `worksheets/03-decide.md` | Decide | Option Set, Tradeoff Table, Decision Statement |
| `worksheets/04-derisk.md` | De-Risk | Gate Definitions, Evidence Plan, Rollback Plan |
| `worksheets/05-deliver.md` | Deliver | Runnable Plan outline, Weekly Visibility cadence |

---

## Quick Start (15 Minutes)

If you want to pressure-test your current situation right now, answer these five questions in writing:

1. **What is the single decision your modernization effort must enable?** (Name the decision and the decision owner.)
2. **What is your one most critical mission thread — and what does "down" mean for it?**
3. **What are your three most material risks?** Express each as: *If [condition], then [failure mode] affects [what], owned by [who].*
4. **What are your two viable paths forward?** (Not just one — if you only have one, you have a preference, not a decision.)
5. **What must be true before you expose production to each path?** Name three gate conditions.

If you can answer all five clearly, you are ready to work the full OA3D flow. If you cannot, those gaps are where the risk lives.

---

## What This Repository Is (And Is Not)

This repository publishes the **framework layer** of OA3D: the vocabulary, decision structures, phase logic, and starter templates.

The full delivery methodology — including the internal operator guide, scoring confidence models, executive readout templates, and engagement governance — is maintained separately and applied in Tower Workshop engagements.

If you are working through a high-stakes platform modernization and want structured support, reach out at **towerworkshop.com**.

---

## License

Framework documentation and worksheets in this repository are published under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may use, adapt, and share with attribution.

---

## About Tower Workshop

Tower Workshop is a fractional CTO practice specializing in always-on platform modernization for mid-market companies. Founded by **Ramberto Torruella Jr.**

[LinkedIn](https://www.linkedin.com/in/rambertotorruella/) · [towerworkshop.com](https://towerworkshop.com) · [@TheTowerworkshop](https://github.com/TheTowerworkshop)


# OA3D Worksheet 01 — Orient
*Part of the [OA3D Framework](../README.md) by Tower Workshop*

> **Purpose:** Define the decision the effort must enable, the mission threads that cannot break, and the constraints that define safe change.
>
> **Time to complete:** 30–60 minutes with the right people in the room.
>
> **Who should be in the room:** The decision owner, the CTO or technical lead, and one operator who knows where the system actually breaks.

---

## Section 1 — Decision Anchor

The Decision Anchor is the single decision your modernization work must enable. Everything else is subordinate to it.

> ⚠️ If you cannot name a decision owner, stop here. No decision owner = no modernization.

| Field | Your Answer |
|---|---|
| **The decision to be made** | *e.g., Replace vs. extend the current platform by Q3* |
| **Decision owner (name and role)** | |
| **Decision deadline or forcing function** | *e.g., License renewal Oct 1, EOL announcement, compliance audit* |
| **Secondary decision (optional)** | *e.g., Sequencing / vendor selection / risk holdback structure* |

---

## Section 2 — Mission Thread Map

List the user journeys or operational flows that cannot fail. These are your Tier-0 and Tier-1 threads.

**Tier-0:** Failure causes immediate, material business impact. Revenue stops, safety degrades, or compliance is breached.

**Tier-1:** Failure causes significant degradation or reputational damage. Not instant revenue loss, but unacceptable within hours.

| Tier | Thread Name | What "Down" Means | Blast Radius (who/what is affected) | Current Fragility Signal |
|---|---|---|---|---|
| 0 | | | | |
| 0 | | | | |
| 1 | | | | |
| 1 | | | | |

> *Tip: "Down" should be specific. Not "the system is unavailable" but "customers cannot complete checkout" or "on-air broadcast drops."*

---

## Section 3 — Safe Change Envelope

Define the constraints that bound what safe change looks like. These become your go/no-go guardrails throughout the engagement.

| Constraint Type | Description |
|---|---|
| **What cannot break under any circumstance** | |
| **What cannot be exposed (security, compliance, contractual)** | |
| **What must be validated before any production exposure** | |
| **Blackout windows (dates / events when no change is allowed)** | |
| **Stakeholder visibility requirements** | *e.g., CEO must be briefed before any Tier-0 cutover* |

---

## Orient Exit Criteria

Before moving to **Assess**, confirm:

- [ ] A single decision is named and has an owner
- [ ] At least two Tier-0 mission threads are documented with failure definitions
- [ ] The safe-change envelope is explicit enough to use as a gate later
- [ ] Key stakeholders agree on what "down" means

If any box is unchecked, those gaps are where misalignment lives. Surface them now.

---

*Next: [Assess →](02-assess.md)*

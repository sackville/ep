---
title: "Command — Visual Design Brief (MVP)"
project: Innovative Safe Solutions
status: Ready for artist hand-off
audience: Visual / UI artists
date: 2026-06-19
---

# Command — Visual Design Brief (MVP)

*The board, its vocabulary, and the journey.*

---

## What this is — and what's yours

Command is the first ISS application: a decision-facilitation tool that helps a founding team build and preserve shared understanding by giving them one legible, living picture of where every decision stands, what each settled decision unblocks, and what to do next.

This brief **locks the structure and the visual vocabulary** — the regions of the board, the states a node can hold, and how each is encoded. It deliberately **does not lock the aesthetic**. Warmth, glow, typography, exact hue refinement, motion, and atmosphere are *yours*.

The one directional constraint: **this is a warm tech tree, not a cold planning grid.** It should feel like a game board you *want* to look at, while staying legible enough to orient on in seconds. Where we had to choose, we chose engagement and honesty over spreadsheet rigor — please carry that the rest of the way.

The node *content* below (Mission, Name the company, File in Delaware…) is the real formation board and is illustrative; the *vocabulary* is the fixed part.

---

## The hero: a tech tree

Founding decisions form a dependency graph — a layered, directed structure where settling one thing unlocks others. A Civ-style **tech tree** is the most faithful rendering of that structure that is also a beloved game board: left-to-right progress, a visible future, and a bright "available now" frontier. We borrow exactly **one move** from the Metroidvania genre — *fog for the unknown* (see **Interior fog**, below).

---

## Reading the board: the regions

| Region | Where | Holds |
|---|---|---|
| **The wake** | Left of the seam | Everything already decided. Settled nodes carrying real timestamps. This is *measured time* — the past. |
| **The Today seam** | A hard vertical line | Left = done and dated. Right = undated dependency structure. |
| **The frontier** | Right of the seam | Everything not yet done — available, queued, or locked-but-visible. Position encodes *dependency*, never calendar. |
| **The exogenous track** | A thin lane along the bottom | Forces outside the team's control — counsel latency, hard external dates. The only things allowed to gate a frontier node without being a node themselves. |
| **The headcount band** | Top of the wake | Team size over time; rides the wake and stops at Today. Three countable marks at MVP scale; a stacked band at larger scale. |

---

## The one rule that governs color

**Hue means exactly one thing: who owns the unblocking. Nothing else ever uses hue.**

Every other distinction — a node's *state* — is carried by **fill, border, and badge**. If you find yourself reaching for a color to show status, stop: status is shape, not hue.

### Ownership palette

| Owner | Hue (our draft — you may re-pick) |
|---|---|
| Russ | coral |
| Scott | blue |
| Cynthia | teal |
| External (counsel, partners) | amber |
| No owner | red |

You're free to re-choose the exact hues, with two non-negotiables: the owner→hue mapping stays strictly 1:1, and **external** and **no-owner** must read as distinct and (for no-owner) faintly alarming.

---

## Node states — the catalog

Every node is exactly one of these, tinted by its owner.

| State | Looks like | Means |
|---|---|---|
| **Researched** | Filled card + ✓ | Settled. Lives in the wake. |
| **Available** | Owner-tinted solid card | Actionable now. The live frontier. |
| **Locked (future)** | Greyed outline | Visible, not yet reachable. |
| **Process-undefined** | Dashed card + "?", interior fogged | The step exists, but its process hasn't been chosen — and you can't see what it unlocks. |
| **Orphan** | Red card + "!" | No one owns the unblocking. An alarm — the loudest thing on the board. |
| **Recursive node** | Card + "▸ N inside" | Collapses a sub-graph; expands on demand. |

---

## Two mechanics to get exactly right

**Interior fog** *(the one Metroidvania steal).* A process-undefined node is visible, but you **cannot see what it unlocks** — its outgoing edges and the nodes beyond it are fogged and unlit until the team authors its process. When they do, the fog lifts and the unlock appears. This is the emotional core of Beat 5; the lift should feel like a small reveal, not a state-toggle.

**The cascade.** Settling a node should visibly *fire*: it crosses the seam into the wake, and its downstream edges light, flipping locked nodes to available. **The reward is the propagation itself** — no points, no score, no confetti. Progress made visible is the whole payoff.

---

## Altitude (a note for scale — not MVP-critical)

The board is built to zoom by *level of detail*. Zoom out and recursive nodes collapse into super-nodes while the headcount marks merge into a band; zoom in to a single node (Beat 5 is a close-up). The MVP mostly lives zoomed all the way in, but please don't design anything that would forbid this later.

---

## The journey — six beats

Schematic reference frames for each beat accompany this brief. Treat them as blocking, not art.

**Beat 0 — The world at rest.** The establishing shot. Every state in repose: the wake of settled nodes with the headcount band; the Today seam; one live node on the frontier with the rest queued and locked behind it; an undefined node fogged; the exogenous track quiet.

**Beat 1 — Orient.** The user returns after days away with little time. Everything recedes except the single available node, which carries the eye. The point: the next move is obvious in seconds, with no digging.

**Beat 2 — The cascade.** The team settles "Name the company." The node crosses the seam into the wake (gaining a timestamp), and the frontier lights — three nodes flip to available, one of them landing with **no owner** (orphan-red). Propagation reveals new work *and* unowned work.

**Beat 3 — Walk in aligned.** Before an attorney call, the board is shared so everyone opens on one picture — settled, asked, parked, and waiting, with the questions for counsel in the external color. (v1 sharing is **screen-share only**; the board stays single-user.)

**Beat 4 — Absorb a change.** Counsel reopens the purpose wording (it pulls back across the seam onto the frontier, flagged *reopened*) and a new disclosure node inserts, gating **two non-adjacent steps** and arriving **unowned**. The turnaround is logged on the exogenous track. The map stays true with no document rewrite.

**Beat 5 — Map the fog.** The user hits a process-undefined node. The app refuses to fake a next step; it routes to the meta-process (research → trade-off → recommend → discuss → align → document). The chosen process is authored in as data, the node flips to available, and **the interior fog lifts** — revealing what it unlocks.

---

## Out of scope — do not design for these yet

Deferred by demand-pull; we'll pull each only when real use makes it hurt:

- **Recurring / cadence nodes** (things that repeat and never "settle").
- **Bet nodes** (open exploratory threads, reviewed and killed rather than completed).
- **Soft edges** (enable / inform relationships, distinct from hard gates).
- **Decision vs. achievement nodes** (willed-when-unblocked vs. occurs-on-convergence).
- **Multi-user / real-time sharing** — v1 is single-user, screen-share only.

---

## Tone, in one line

**Warm tech tree.** Legible enough to orient in seconds, alive enough to want to look at. The structure here is fixed; the soul is yours.

---

## Command Design Principles

The following principles guide every design decision in Command. They are derived from the Enterprise Playability philosophy, the founding persona, and the company's purpose of building the shared understanding that equips people to make well-informed decisions.

These principles are intended to constrain design rather than merely inspire it. Any proposed feature, interaction, visualization, or workflow should strengthen these principles rather than weaken them.

### 1. Maintain a shared model of reality

The board is the team's collective working memory.

It must accurately represent the team's current understanding of the situation while remaining easy to update as reality changes.

The dependency graph exists to support this purpose; it is a means, not the end.

### 2. Preserve shared understanding

The primary purpose of Command is to preserve and strengthen shared understanding over time.

Every significant feature should contribute to creating, maintaining, restoring, or communicating shared understanding among participants.

### 3. Answer "What's next?"

At any meaningful pause in the work, the application should help participants identify the most valuable next step.

Doing so requires making visible the factors that influence that decision, including dependencies, urgency, blockers, effort, and impact.

### 4. Make consequences visible

The value of completing a decision lies not merely in marking work complete, but in revealing what has changed.

Whenever possible, Command should expose downstream consequences, newly available work, newly blocked work, and changes to the decision landscape.

### 5. Preserve organizational memory

Important decisions should not disappear into meeting notes, email threads, or fading memories.

Command should preserve significant decisions together with the context required to understand them later, including rationale, alternatives considered, assumptions, and conditions that would justify revisiting the decision.

When decisions change, the history of those changes should remain visible.

### 6. Reveal uncertainty honestly

The application must never invent certainty.

Undefined processes, unresolved decisions, missing information, and unknown consequences should be represented explicitly rather than concealed.

Uncertainty is part of the shared understanding.

### 7. Treat process as data

Command facilitates decision-making processes rather than hard-coding them.

Processes should be discoverable, inspectable, selectable, and improvable as organizational knowledge evolves.

### 8. Treat objectives as first-class artifacts

Shared objectives exist independently of the processes used to create them.

Processes may define, refine, or retire objectives, but objectives themselves should remain visible and traceable throughout the decision graph.

### 9. Reduce the cost of reorientation

Every return to the application should require as little cognitive effort as possible.

Command should minimize the effort required to re-establish shared understanding between work sessions by preserving the context, decisions, rationale, and current state needed to continue meaningful work immediately.

The board exists so the team can spend its time making decisions rather than reconstructing context.

### 10. Reward understanding

The primary reward for using Command is increased clarity.

Progress should leave participants with a better understanding of the work, the current situation, the available opportunities, and the consequences of future decisions.

The application should avoid artificial reward systems that distract from meaningful progress.

### 11. Keep the board truthful

The board should always represent the team's best current understanding.

When new information proves that understanding incomplete or incorrect, updating the board should be simple, immediate, and welcomed rather than resisted.

Truthfulness is more important than permanence.
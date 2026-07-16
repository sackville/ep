# Viper Command Through the Game-Design Lens

*Preserved source analysis for EP process reconciliation. This is a situated assessment, not reconciled EP guidance.*

## Governing concern and chosen framework

Scott Rogers's practical approach remains useful and current; the third edition of *Level Up!* was published in December 2024 and retains the one-sheet, ten-page design, beat chart, GDD, systems thinking, and playtest material.[^rogers]

There is no single modern industry-standard process that has replaced it. The assessment therefore used a **player-experience-led, iterative systems-design framework** assembled from durable industry practices:

```text
Player and desired experience
        ↓
Vision and design pillars
        ↓
Player verbs and gameplay loops
        ↓
Mechanics → dynamics → experienced qualities
        ↓
Playable prototype
        ↓
Observe, evaluate, tune, and repeat
```

This draws on MDA's connection among implemented rules, emergent system behavior, and player experience,[^mda] contemporary core-loop/prototype/playtest guidance,[^unity-design] and the game industry's use of concise living artifacts for vision, pillars, loops, and resource flow.[^gdc-docs]

## Work completed or substantially underway

### High concept and player

Command is a warm tech tree that helps a founding team maintain shared understanding, see the path to objectives, and determine what to do next. Scott is a specific player with documented work, motivations, constraints, and desired emotional outcome.

### Desired player experience

Command should feel warm, legible, alive, engaging, and honest. Scott should leave relieved, confident, curious, inspired, and ready to help. These are experiential goals rather than features.

### Central metaphor

The tech tree fits Dependencies, locked possibilities, Available actions, progress, unlocking, history, uncertainty, and Objectives. Fog is similarly tied to genuinely unknown process rather than decorative theme.

### Design pillars in raw form

Existing principles include maintaining shared understanding, answering what's next, making consequences visible, revealing uncertainty, keeping truth, rewarding understanding, reducing reorientation cost, consistent ownership hue, and meaningful propagation over artificial rewards.

### Mechanics and progression

Mechanics include Decisions, Tasks, hard Dependencies, Availability, ownership, Orphans, Wake, reopening, correction, process fog, External Forces, and Recursive groups.

The natural progression is:

```text
Unknown or Locked
  → reachable
  → Available
  → acted upon
  → settled or completed
  → consequences propagate
  → new possibilities become reachable
```

### Reward philosophy and signature moments

The reward is increased clarity, visible consequence, new action, reduced uncertainty, and movement toward Objectives—not points or confetti. Cascade and fog lift are intended emotional moments of propagation and reveal.

### Beat structure, visual frames, and scope

The six beats provide pacing from establishment through payoff, social use, complication, and deeper system revelation. SVG frames communicate composition and emphasis. Recurrence, bets, soft edges, achievements, real-time multiplayer, altitude, and reorientation are deferred.

## Work not yet completed

- Explicit player role or fantasy.
- Three to five concise design pillars.
- Player-verb vocabulary.
- Explicit core and supporting loops.
- Feedback map.
- Mechanics-to-dynamics analysis.
- Onboarding.
- Playable prototype and observed playtests.
- Tuning.
- Game feel, sound, motion, responsiveness, and accessibility treatment.

The board is designed more completely than the play.

## Recommended next work

### 1. Write a one-page game vision

State the player, role, goal, repeated activity, desired feeling, reason for interactivity, and anti-goals. A provisional role is facilitator and navigator of shared understanding, but “commander,” “navigator,” “facilitator,” “cartographer,” and “steward” carry different implications and should be chosen deliberately.

### 2. Distill design pillars

Possible pillars:

- **The next move is legible.**
- **Progress reveals consequence.**
- **Uncertainty is playable.**
- **The board remains truthful.**

Pillars should reject mechanics as well as approve them.

### 3. Define player verbs

Candidate verbs include orient, inspect, trace, compare, choose, assign, ask, settle, complete, attach evidence, reopen, correct, define, reveal, explain, and share. Distinguish core verbs, supporting administration, in-app action, and real-world work performed outside Command.

### 4. Define nested loops

Moment to moment:

```text
Scan → notice → inspect → understand
```

Core action:

```text
Orient → choose meaningful work → act or facilitate action
       → record the result → observe consequences → reorient
```

Long term:

```text
Maintain the shared model → advance Objectives → absorb changed reality
→ preserve memory → improve how the team works
```

Avoid “compulsion loop”; Command seeks willing engagement through clarity, not behavioral capture. A core loop is the repeating cycle of action and feedback through which progress occurs.[^core-loop]

### 5. Analyze mechanics, dynamics, and experience

Examples:

| Intended experience | Desired dynamic | Supporting mechanics |
| --- | --- | --- |
| Clarity | Attention converges on actionable work | Availability, hierarchy, Frontier |
| Agency | Intervention points are understood | Dependencies, ownership, inspection |
| Satisfaction | Progress changes the landscape | Records, cascade, Wake |
| Curiosity | Meaningful unknowns invite investigation | Fog, Locked future, Relationships |
| Trust | State and change are explainable | History, reopening, correction |
| Constructive concern | Unowned or external gates draw attention | Orphan treatment, exogenous track |
| Relief | Context survives time away | Stable state, records, reorientation |

Test for unwanted dynamics such as orphan-red producing blame or anxiety instead of constructive urgency.

### 6. Build a playable core-loop prototype

Let the player open a small real board, identify Available work, inspect why it matters, complete a Task or settle a Decision, record a minimal result, observe downstream Availability, and identify the next action.

Use enough warmth and responsiveness to test the intended experience; completely sterile placeholder presentation can distort perceived responsiveness and game feel.[^prototype-fidelity]

### 7. Playtest behavior and experience

Observe attention, interpretation, prediction, cascade comprehension, trust, willingness to continue, and transition back to real work. Ask what the player expected and understood rather than whether they merely liked it. Early playtesting is essential while changes remain inexpensive.[^playtest]

### 8. Tune feedback and game feel

Tune input response, hover and selection, edge emphasis, node movement, cascade timing, fog, sound if appropriate, persistent aftermath, reduced-motion alternatives, and screen-share legibility.

### 9. Teach through play

Introduce the core loop by having the player notice, inspect, complete, observe, and inspect preserved history. Reveal reopening, correction, External Forces, and undefined process when first encountered.

### 10. Repeat short design–build–playtest cycles

For each cycle, ask which experience was intended, which mechanic should produce it, what behavior emerged, what the player actually understood or felt, and what should be removed or tuned.

## Lens summary

Command has completed much of game preproduction: player, concept, emotional target, metaphor, mechanics, progression, reward philosophy, signature moments, beats, visual vocabulary, and scope. The next transition is to define role, verbs, pillars, and loops; connect mechanics to intended experience; build the smallest playable core; and tune it through observation until progress feels like increased understanding.

## References

[^rogers]: [*Level Up! The Guide to Great Video Game Design*, third-edition overview](https://www.oreilly.com/library/view/level-up-the/9781394298761/cover.xhtml)
[^mda]: [Robin Hunicke, Marc LeBlanc, and Robert Zubek, “MDA: A Formal Approach to Game Design and Game Research”](https://users.cs.northwestern.edu/~rob/publications/MDA.pdf)
[^unity-design]: [Unity, “Game Design”](https://learn.unity.com/pathway/game-development/unit/planning-a-game/tutorial/game-design)
[^gdc-docs]: [GDC 2025, “The Four One-Page Design Docs You Need (And How to Use Them)”](https://gdcvault.com/play/1035120/The-Four-One-Page-Design)
[^core-loop]: [Unity, “Close the core game loop”](https://learn.unity.com/course/2D-adventure-robot-repair/unit/game-ui-and-game-loop/tutorial/close-the-core-game-loop?version=6.3)
[^prototype-fidelity]: [Unity, “The placeholder asset problem: How programmer art kills playtests”](https://unity.com/blog/placeholder-asset-problem)
[^playtest]: [Unity, “How To Playtest”](https://learn.unity.com/course/playtesting/tutorial/how-to-playtest)

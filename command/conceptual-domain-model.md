# Command Conceptual Domain Model

*First draft. A living document.*

This model describes the conceptual truths Command must preserve. It is not a database schema, object model, service boundary, or UI specification. Its purpose is to establish the ubiquitous language used by founders, designers, engineers, and AI collaborators while designing and building Command.

## Foundational Concepts

### Shared Understanding

**Definition**  
The evolving understanding held by the team about its situation, decisions, objectives, processes, and next actions.

**Purpose**  
Shared Understanding is the reason Command exists. The application helps create, preserve, restore, and communicate it.

**Relationships**  
Shared Understanding is shaped by Decisions, Objectives, Processes, Relationships, External Forces, and Change Events.

**Representation**  
The Board is the primary representation of Shared Understanding.

**Notes**  
Shared Understanding is not mere agreement in a meeting. It must be durable enough to survive time, memory drift, and later review.

### Reality

**Definition**  
The actual situation the team is trying to understand: what has happened, what is true now, what is possible, what is blocked, and what may change.

**Purpose**  
Reality is what the Board must remain truthful to.

**Relationships**  
Reality is reflected imperfectly by the Board. New information may reveal that the Board is incomplete or wrong.

**Representation**  
Reality is represented by the Board but is not identical to it.

**Notes**  
Truthfulness implies a distinction between reality and the team's current model of reality.

### Representation

**Definition**  
A designed rendering of the team's current understanding of reality.

**Purpose**  
Representation reduces the cognitive cost of reorientation by making the current situation legible.

**Relationships**  
The Board is Command's primary representation.

**Representation**  
Representation appears as the visual board, regions, nodes, edges, states, badges, fog, and motion.

**Notes**  
The UI should reveal domain truths rather than inventing concepts for visual convenience.

### Organizational Memory

**Definition**  
The durable record of what was decided, why, under what assumptions, and under what conditions it should be revisited.

**Purpose**  
Organizational Memory prevents repeated conversations, decision churn, and loss of rationale.

**Relationships**  
Organizational Memory is primarily built from Decision Records and Change Events.

**Representation**  
The Wake is the primary visual region for settled, dated organizational memory.

**Notes**  
Organizational Memory is Command's application-level counterpart to the YTHO idea: preserving the why behind important decisions.

## Modeling Philosophy

The Conceptual Domain Model describes the truths that exist within Command.

It intentionally avoids implementation concerns, persistence, service boundaries, APIs, and user interface design.

Nodes do not define the domain.
Relationships do not define the visualization.

Instead, the domain model defines reality, while the board reveals the team's current shared understanding of that reality.

Visualization concepts such as the Wake, Frontier, and Seam are projections over domain concepts rather than the concepts themselves.

## Rule 0: Model reality, not implementation

The conceptual model answers:

> What truths exist in the world of Command?

It does not answer:

- how those truths are stored;
- which aggregate owns them;
- which table contains them;
- which service publishes them;
- how the UI renders them.

Those decisions come later.

## Core thesis

Command maintains a shared model of reality so a team can understand what has been decided, what is true now, what is possible next, and why.

The dependency graph is the current visual mechanism for that purpose. It is not the purpose itself.

## Top-level ontology

```text
Shared Understanding
│
├── Reality
│   ├── Objectives
│   ├── Decisions
│   ├── Processes
│   ├── External Forces
│   └── Relationships
│
├── Representation
│   └── Board
│       ├── Nodes
│       ├── Edges
│       ├── Wake
│       ├── Frontier
│       └── Seam
│
└── Evolution
    ├── Decision Records
    ├── Change Events
    ├── Reopening Conditions
    └── Organizational Memory
```

## Operational concepts

### Objective

**Definition**  
A desired outcome the team is trying to achieve.

**Purpose**  
Objectives give decisions and processes direction. They answer what a process or decision is trying to accomplish.

**Relationships**  
Objectives may be produced, refined, or retired by Processes. Decisions may serve, advance, or constrain Objectives. Downstream work may trace to Objectives.

**Representation**  
Objectives may appear as node content, node metadata, or contextual labels associated with active decisions and processes.

**Notes**  
Objectives are process-independent and process-agnostic. The method for creating an objective may be process-specific, but the Objective itself remains a first-class artifact.

### Decision

**Definition**  
A commitment made by the team that changes the state of the Board.

**Purpose**  
Decisions settle uncertainty, unlock downstream work, preserve rationale, and evolve Shared Understanding.

**Relationships**  
A Decision may satisfy Dependencies, create Change Events, produce Decision Records, advance Objectives, and trigger Reopening Conditions later.

**Representation**  
A Decision may be represented by a Node. When settled, it moves into the Wake with a timestamp and associated record.

**Notes**  
A Node is not necessarily a Decision. A Node may represent multiple kinds of domain concepts.

### Decision Record

**Definition**  
The durable explanation of a Decision.

**Purpose**  
Decision Records preserve the context needed to understand a Decision later.

**Relationships**  
A Decision Record belongs to a Decision. It may reference Objectives, alternatives, assumptions, rationale, consequences, evidence, source materials, and Reopening Conditions.

**Representation**  
A Decision Record may be surfaced from a settled node in the Wake.

**Notes**  
Suggested contents include: decision, date, participants, options considered, rationale, assumptions, accepted drawbacks, consequences, source references, and conditions for reconsideration.

### Process

**Definition**  
A repeatable way of reaching a decision, producing an artifact, or advancing work.

**Purpose**  
Processes guide how the team moves from uncertainty to a usable result.

**Relationships**  
Processes may produce Decisions, Objectives, artifacts, or additional Nodes. A Node may be process-defined or process-undefined.

**Representation**  
A Process may be represented by node metadata, process detail, or a recursive sub-graph.

**Notes**  
Processes are data. Command facilitates processes rather than hard-coding them.

### Process Definition

**Definition**  
The authored data that makes a Process usable by Command.

**Purpose**  
A Process Definition turns an undefined process into one that can guide work and reveal downstream structure.

**Relationships**  
A Process Definition belongs to a Process and may be authored through a meta-process.

**Representation**  
When a Process Definition is authored, a process-undefined Node may become process-defined and its fog may lift.

**Notes**  
The constitutional meta-process is the t=0 exception to demand-pull because it is required to define all other processes.

### External Force

**Definition**  
A force outside the team's direct control that can affect progress.

**Purpose**  
External Forces preserve truthfulness when progress is gated by something other than the team's own decisions.

**Relationships**  
External Forces may gate Nodes, trigger Change Events, or create Reopening Conditions.

**Representation**  
External Forces appear on the exogenous track rather than as ordinary nodes, unless later design work proves a need to model them differently.

**Notes**  
Examples include counsel latency, legal requirements, hard external dates, or partner responses.

## Structural concepts

### Node

**Definition**  
A visual representation of something in the domain model.

**Purpose**  
Nodes make domain concepts visible and actionable on the Board.

**Relationships**  
Nodes may represent Decisions, Objectives, Processes, External Forces, or future domain concepts. Nodes are connected by Relationships.

**Representation**  
Nodes appear as cards with owner hue, state treatment, badges, and possible fog.

**Notes**  
Nodes do not hold domain truth; they represent it. This keeps visualization separate from reality.

### Relationship

**Definition**  
A meaningful connection between two domain concepts.

**Purpose**  
Relationships carry much of the meaning in Command. They explain why something matters, what it affects, and what affects it.

**Relationships**  
Dependency is the primary relationship type for the MVP. Future relationship types may include enables, informs, supersedes, conflicts with, duplicates, or soft edge.

**Representation**  
Relationships are visualized as edges between Nodes.

**Notes**  
The Board is not merely a graph of nodes. It is a graph of relationships.

### Dependency

**Definition**  
A gating Relationship in which one concept must be satisfied before another becomes available.

**Purpose**  
Dependencies determine availability, locked state, and cascade behavior.

**Relationships**  
Dependencies connect upstream and downstream Nodes. When satisfied, they may unblock downstream work.

**Representation**  
Dependencies appear as directed edges. Satisfied dependencies may light during cascade.

**Notes**  
For the MVP, most visible edges are dependencies. This should not imply that every future edge is a dependency.

### Edge

**Definition**  
The visual connector used to represent a Relationship on the Board.

**Purpose**  
Edges make relationships visible.

**Relationships**  
An Edge represents a Relationship. It is not itself the relationship.

**Representation**  
Edges connect Nodes and may light, fade, disappear into fog, or otherwise change treatment based on relationship state.

**Notes**  
This distinction allows future visual treatments for non-dependency relationships without changing the conceptual model.

### Owner

**Definition**  
The person, party, or external actor responsible for unblocking something.

**Purpose**  
Ownership answers who owns the next movement of work.

**Relationships**  
Owners may be assigned to Nodes or to specific unblocking responsibilities.

**Representation**  
Owner is encoded by hue and nothing else.

**Notes**  
No-owner is a meaningful and alarming condition.

### State

**Definition**  
The current condition of a Node relative to the team's understanding and ability to act.

**Purpose**  
State tells the team what kind of attention a Node requires.

**Relationships**  
State may be derived from Decisions, Process Definitions, Dependencies, Ownership, and external gates.

**Representation**  
State is encoded through fill, border, badge, fog, and other non-hue treatments.

**Notes**  
Hue must not be used for state.

## Historical concepts

### Change Event

**Definition**  
A recorded event that changes the Board's representation of reality.

**Purpose**  
Change Events preserve why the Board changed.

**Relationships**  
Change Events may affect Decisions, Relationships, Objectives, Processes, or External Forces.

**Representation**  
Some Change Events may appear in the Wake, exogenous track, or node history.

**Notes**  
Examples include counsel reopening a purpose decision, a new legal requirement, or a process being defined.

### Reopening Condition

**Definition**  
A condition under which a settled Decision should be reconsidered.

**Purpose**  
Reopening Conditions make future reconsideration principled rather than arbitrary.

**Relationships**  
Reopening Conditions belong to Decision Records and may be triggered by Change Events.

**Representation**  
A reopened node may pull back from the Wake to the Frontier and carry a reopened flag.

**Notes**  
When a Decision is reopened, the conditions that drove reopening should be preserved.

### Reopening

**Definition**  
The act of moving a settled Decision back into active consideration because reality changed or a Reopening Condition was met.

**Purpose**  
Reopening keeps the Board truthful without erasing history.

**Relationships**  
A Reopening creates a Change Event, modifies State, and extends Organizational Memory.

**Representation**  
A reopened node may move back across the Today seam with a visual flag.

**Notes**  
Reopening does not imply the original decision was bad. It means the conditions around it changed.

## Visualization concepts

### Board

**Definition**  
The primary visual representation of the team's shared model of reality.

**Purpose**  
The Board reduces the cognitive cost of reorientation and helps the team decide what to do next.

**Relationships**  
The Board represents Nodes and Relationships. It projects historical, current, and future-facing understanding into a legible scene.

**Representation**  
The Board includes the Wake, Today seam, Frontier, Exogenous Track, and Headcount Band.

**Notes**  
The Board is not the domain. It is the domain made visible.

### Wake

**Definition**  
The visual region containing settled, dated Nodes.

**Purpose**  
The Wake preserves organizational memory and shows measured time.

**Relationships**  
The Wake contains representations of settled Decisions and other completed domain concepts.

**Representation**  
The Wake sits left of the Today seam.

**Notes**  
The Wake should expose access to Decision Records and history, not merely completion status.

### Today Seam

**Definition**  
The visual boundary between dated history and undated dependency structure.

**Purpose**  
The Today seam helps distinguish measured time from dependency-positioned possibility.

**Relationships**  
The seam separates Wake from Frontier.

**Representation**  
The seam appears as a hard vertical line.

**Notes**  
The seam is a visual concept, not a domain entity.

### Frontier

**Definition**  
The visual region containing available, locked, undefined, and queued work.

**Purpose**  
The Frontier shows what is not yet settled and what may become actionable.

**Relationships**  
The Frontier is computed from Node State, Dependencies, Process Definitions, and External Forces.

**Representation**  
The Frontier sits right of the Today seam.

**Notes**  
Position in the Frontier encodes dependency, not calendar time.

### Exogenous Track

**Definition**  
The visual lane for external forces that affect progress.

**Purpose**  
The Exogenous Track distinguishes team-owned work from externally controlled gates.

**Relationships**  
It represents External Forces and their effects.

**Representation**  
The track runs along the bottom of the Board.

**Notes**  
The Exogenous Track prevents external conditions from being misrepresented as ordinary team-owned work.

### Headcount Band

**Definition**  
The visual representation of team size over measured time.

**Purpose**  
The Headcount Band provides organizational context for the Wake.

**Relationships**  
It relates to time, team composition, and historical context.

**Representation**  
The band rides the top of the Wake and stops at Today.

**Notes**  
Not MVP-critical beyond the current visual vocabulary.

## Open modeling questions

1. Which domain concepts may be represented by Nodes in the MVP?
2. Are Owners assigned to Nodes, Relationships, or unblocking responsibilities?
3. What is the minimum viable Decision Record?
4. How much of Objective traceability belongs in the MVP?
5. What exactly makes a Dependency satisfied?
6. What data must be captured when a Process Definition is authored?
7. How should External Forces differ from externally owned Nodes?
8. Which derived concepts should be computed rather than stored?
9. What is the minimum model needed to support the six story beats?
10. Which concepts are Command-specific, and which may become reusable EP/Viper concepts?

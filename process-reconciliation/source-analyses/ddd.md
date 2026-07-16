# Viper Command Through the Domain-Driven Design Lens

*Preserved source analysis for EP process reconciliation. This is a situated assessment of Viper Command, not reconciled EP guidance.*

## Governing concern

From a DDD perspective, Command has completed a meaningful portion of strategic domain discovery but has not yet crossed into a tactical implementation model.

## Work completed or substantially underway

### Domain vision

Command exists to maintain sufficient shared understanding for a team to see the path toward its objectives and confidently decide what to do next. This identifies shared understanding—not task tracking or graph visualization—as the central problem.

### Likely core domain

The differentiating capability appears to be maintaining a truthful, durable, evolving model of the team's reality and making the consequences of change legible. Graph rendering, authentication, persistence, and ordinary task management are not the core domain.

### First ubiquitous language

The conceptual model defines Shared Understanding, Reality, Representation, Organizational Memory, Objective, Decision, Task, Decision Record, Task Completion Record, Process, Process Definition, Dependency, External Force, Owner, Change Event, Reopening, and Task Correction.

It preserves important distinctions:

- Reality versus its representation.
- Domain concepts versus Nodes.
- Relationships versus Edges.
- Decisions settle uncertainty; Tasks change reality.
- Decision Reopening versus Task Correction.
- External Forces versus team-owned work.

### Separation of domain and presentation

Nodes and Edges represent domain concepts and Relationships. Wake, Frontier, and Today Seam are projections. This guards against building a graph editor whose business meaning exists only in UI attributes.

### Scenarios and observable behavior

The six story beats provide early domain scenarios: reorientation, cascade, shared meeting context, changed information, reopening, correction, and definition of unknown process.

### Modeling discipline

The project explicitly records open questions instead of inventing certainty, including ownership, dependency satisfaction, task completion, process-definition data, objective traceability, and the minimum model required for the beats.

## Work not yet completed

- Domain-event model.
- Commands, policies, and invariants.
- Explicit subdomains.
- Bounded Contexts and Context Map.
- Aggregate and consistency boundaries.
- Entity identity and Value Objects.
- Executable domain examples.
- A selected implementation slice.

## Recommended next work

### 1. Model real formation work as domain events

Use actual ISS formation history and the story beats in a focused event-storming exercise. Candidate events include:

```text
ObjectiveEstablished
DecisionRequested
DecisionSettled
TaskAssigned
TaskCompleted
DependencySatisfied
WorkBecameAvailable
DecisionReopened
CorrectiveTaskCreated
ExternalRequirementIntroduced
ProcessFoundUndefined
ProcessDefined
```

Place commands, actors, policies, external actors, questions, and conflicts around the events. Beat 2—the cascade—is a strong first slice because it exercises decisions, tasks, dependencies, records, availability, ownership, and consequences.

### 2. Turn scenarios into concrete examples

Write specific Given/When/Then examples that force precise meanings for *satisfied*, *available*, *complete*, and *owned*. For example, a filing Task gated by a naming Decision and domain-check Task should become Available only after both prerequisites are satisfied.

### 3. Identify invariants and policies

Likely candidates include:

- A settled Decision has a Decision Record.
- A completed Task has a Task Completion Record.
- Work is not Available while a hard Dependency remains unsatisfied.
- Reopening preserves prior Decision history.
- Corrective work does not erase a valid prior completion.
- Process-undefined work does not expose invented downstream structure.
- Visible board changes are explainable from domain state or history.

### 4. Discover subdomains and propose Bounded Contexts

Possible areas include Work Navigation, Organizational Memory, Process Knowledge, Organization and Ownership, and Board Projection. These are hypotheses, not recommended services. The MVP may reasonably begin as one principal Command context with clear internal modules.

### 5. Resolve only questions required by the first slice

For the cascade, determine identity, Dependency satisfaction, multiple hard dependencies, whether Availability is derived, required completion evidence, MVP owner types, and whether Orphan and Recursive are truly states or orthogonal representation conditions.

### 6. Produce a minimal tactical model

Use concrete rules to identify Entities, Value Objects, Aggregates, Domain Events, repositories, and policies. Do not declare the entire Board one Aggregate by convenience; let consistency requirements determine boundaries.

### 7. Build one vertical walking slice

Load a small formation model, display historical and frontier work, settle a Decision or complete a Task, preserve the record, recalculate satisfied Dependencies, reveal newly Available work, and render the consequence visibly.

## Lens summary

Command has completed domain vision, early discovery, conceptual language, representation separation, and scenario framing. The next DDD transition is from concepts to behavior: domain events, concrete examples, policies, and invariants, followed by the smallest tactical model required for one working vertical slice.

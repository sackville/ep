# Viper Command Through the Behavior-Driven Development Lens

*Preserved source analysis for EP process reconciliation. This is a situated assessment, not reconciled EP guidance.*

## Governing concern

BDD is collaborative discovery through concrete examples, not merely writing Gherkin tests. The examples create shared understanding of behavior and may then be preserved in executable form where valuable.

Command has much of the discovery material required for good behavior specifications but not yet examples precise enough to drive implementation.

## Work completed or substantially underway

### Desired outcome and actor

Command exists to help Scott and the founders maintain shared understanding and decide what to do next. The persona supplies context, constraints, vocabulary, representative situations, and observable success.

### Ubiquitous language

The project defines Objective, Decision, Decision Record, Task, Task Completion Record, Dependency, Available, Locked, Owner, External Force, Process Definition, Reopening, Task Correction, Change Event, Wake, and Frontier. Domain/representation separation supports behavior specifications that are not coupled to UI details.

### High-level scenarios

The six beats describe orientation, cascade, meeting alignment, changed information, reopening, correction, and undefined process.

### Important rules

- Hard Dependencies gate downstream Availability.
- Settled Decisions preserve Decision Records.
- Completed Tasks preserve Task Completion Records.
- Progress can make downstream work Available.
- Reopening preserves earlier history.
- Corrective work normally preserves valid prior completion.
- Undefined process must not expose invented structure.
- Ownership and state are distinct.
- Frontier position means dependency, not calendar time.
- The board remains truthful as reality changes.

### Concrete formation language and explicit scope

Examples such as naming the company, checking the domain, filing in Delaware, purpose wording, disclosure work, and counsel questions are stronger than abstract Task A/Node B examples. Deferred capabilities prevent first examples from expanding without bound.

## Work not yet completed

- Example-mapping conversations.
- Rules paired with concrete examples.
- Given/When/Then scenarios.
- Explicit triggering commands.
- Agreed observable outcomes.
- Boundary and exception examples.
- Resolved contradictions exposed by examples.
- Executable specifications and outside-in automation.
- A process for keeping specifications living.

## Recommended next work

### 1. Select one capability

The cascade is a strong first candidate: when a Task is completed or Decision settled, preserve the result and reveal resulting Available work.

### 2. Conduct example mapping

Organize discussion around outcome, rules, examples, and questions. For example, the rule “all hard Dependencies must be satisfied” can be illustrated by filing work gated by naming and domain checking, while leaving questions about External Forces visible.

### 3. Write declarative scenarios

An example:

```gherkin
Scenario: Completing the last required task makes downstream work available
  Given "File in Delaware" depends on:
    | prerequisite              | condition |
    | Name the company          | settled   |
    | Check domain availability | completed |
  And "Name the company" has been settled
  And "Check domain availability" is incomplete
  When Scott completes "Check domain availability"
  Then a completion record is preserved for "Check domain availability"
  And "File in Delaware" becomes available
```

Keep database, HTTP, CSS, and animation implementation out of the business example.

### 4. Probe boundaries

Explore remaining Dependencies, opposite completion order, repeated completion, missing evidence, mixed Task/Decision gates, simultaneous unlocks, unowned newly Available work, remaining external gates, reopened prerequisites, and corrective work.

### 5. Resolve contradictions through examples

Examples should clarify whether Orphan can coexist with Available, whether orphanhood is derived, whether Recursive is a state/kind/representation behavior, whether moving to the Wake is domain or projection, what completes a Task, whether reopening relocks downstream work, and what structure is known around undefined process.

### 6. Separate domain and visual behavior

Domain examples cover completion, records, Dependency satisfaction, and Availability. Representation examples cover Wake placement, highlighted Relationships, state treatment, and ownership alarms. Both matter but may require different verification.

### 7. Automate outside-in

Drive at least one stable boundary through a known board, real user action, preserved result, changed Availability, and changed projection. Use lower-level tests for detail while retaining an end-to-end example.

Do not choose Cucumber, SpecFlow, Behave, Playwright, or another framework until the application stack warrants it. Discovery can begin in Markdown.

### 8. Implement only enough to satisfy agreed examples

Let examples pull implementation forward rather than building speculative workflow or graph engines. Passing automation proves conformance to the examples, not that the examples describe the right product, so review the result with participants.

### 9. Grow by capability

A possible sequence is hard-dependency Availability, Task completion, Decision settlement, cascade, unowned work, reopening, correction, external gating, undefined process, and process revelation.

### 10. Keep specifications living

Retain only significant scenarios in Command language. Run them continuously and revise them with shared understanding. Do not convert every technical test into Gherkin.

## Representative first example set

- One remaining Dependency keeps work Locked.
- The final Dependency makes work Available.
- Completing a Task preserves its record.
- Settling a Decision preserves its record.
- Completing one item makes several downstream items Available.
- Unrelated work remains unchanged.
- Newly Available unowned work is identified as requiring ownership.

## Lens summary

Command has the purpose, persona, language, rules, and scenarios from which BDD can grow. The next transition is to choose one valuable capability, map its rules and examples, expose questions, agree on observable behavior, automate the stable examples, and let those examples pull implementation forward.

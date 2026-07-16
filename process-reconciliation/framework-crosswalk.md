# Framework Crosswalk

*Step 2 output for the EP process reconciliation. This document maps the six situated lenses without reconciling them. Overlaps, seams, tensions, and unique contributions are interpreted in step 3.*

## Purpose

The crosswalk makes each framework's contribution visible while preserving the different questions it asks. It is descriptive rather than prescriptive: appearing first in a row does not grant a lens ownership of that activity, and an empty cell does not mean the lens can never contribute.

## Source analyses

- [Domain-Driven Design](source-analyses/ddd.md)
- [Agile development](source-analyses/agile-development.md)
- [Lean Startup and Business Model Canvas](source-analyses/lean-startup-and-bmc.md)
- [User-Centered Design](source-analyses/user-centered-design.md)
- [Behavior-Driven Development](source-analyses/behavior-driven-development.md)
- [Game design](source-analyses/game-design.md)

## The six lenses at a glance

| Lens | Governing question | Primary subject of evaluation |
| --- | --- | --- |
| User-Centered Design | Who are we helping, in what situation, to accomplish what job? | Human progress in context |
| Lean Startup and BMC | Which beliefs about value, demand, growth, and viability survive contact with reality? | Product and business hypotheses |
| Game design | What does the player repeatedly do, and what experience emerges from the system? | Player behavior, dynamics, and experience |
| Domain-Driven Design | What truths, language, relationships, rules, and boundaries exist in the domain? | Explanatory and behavioral fidelity of the domain model |
| Behavior-Driven Development | Can participants agree on significant behavior through concrete examples? | Shared behavioral understanding and observable outcomes |
| Agile development | How can we deliver small usable increments and adapt from feedback? | Usable increments, learning flow, and responsiveness |

## Lens profiles

### User-Centered Design

**Contribution**

Keeps design attached to a specific person carrying real jobs in a real situation. It discovers context, current behavior, breakdowns, needs, desired outcomes, and whether an intervention helps the person make progress.

**Typical artifacts**

- Research and observation notes.
- Real-person-anchored persona.
- Canonical and situated job lists.
- People-by-jobs matrix when a broader population is being considered.
- Current- and future-state journeys.
- Persona–job–scenario framing.
- Task flows and prototypes.
- Usability and accessibility findings.
- Roadmap to mind uncovered jobs.

**Evidence sought**

- Observed current behavior and source artifacts.
- Successful completion of representative tasks.
- Reduced effort, error, confusion, or workaround use.
- Improved confidence, comprehension, and progress.
- Voluntary use in the real situation.
- Accessibility across relevant perceptual and interaction needs.

**Depends on**

- Access to real people and their work.
- A sufficiently specific situation and job.
- Representative content and tasks.
- Willingness to observe behavior rather than accept stated preference alone.

**Failure modes it helps prevent**

- Building for an averaged or fictional person.
- Solving a proxy stakeholder's problem instead of the user's.
- Treating requirements as evidence of need.
- Feature sprawl caused by serving multiple personas at once.
- Locally correct software that does not help a human make progress.
- Inaccessible or context-insensitive design.

### Lean Startup and Business Model Canvas

**Contribution**

Makes product and business beliefs explicit, ranks uncertainty, and organizes experiments that generate evidence about desirability, demand, adoption, channels, revenue, delivery economics, partnerships, and growth.

**Typical artifacts**

- Product- and company-hypothesis map.
- Product-specific Business Model Canvas.
- Hypothesis register with confidence and importance.
- Assumption map.
- Baseline observations.
- Experiment design and thresholds.
- Evidence and experiment log.
- Innovation-accounting measures.
- Persevere, adapt, or pivot record.

**Evidence sought**

- Demonstrated problem frequency and consequence.
- Behavioral commitment of time, access, data, reputation, or money.
- Repeat use and adoption.
- Identifiable buyer, budget, and procurement movement.
- Channel progression rather than attention alone.
- Delivery effort and unit economics.
- Repeatability across customers or situations.
- Evidence that contradicts as well as supports the hypothesis.

**Depends on**

- Explicit falsifiable hypotheses.
- Honest confidence and evidence assessment.
- Access to users, buyers, partners, and market behavior.
- Success and failure thresholds chosen before results are known.
- Separation of evidence from interpretation.

**Failure modes it helps prevent**

- Treating a compelling idea as a validated business.
- Confusing technical feasibility, interest, or praise with demand.
- Blending evidence across distinct products or hypotheses.
- Overbuilding before testing a fatal assumption.
- Optimizing vanity metrics.
- Discovering too late that delivery is uneconomic or the buyer unreachable.

### Game design

**Contribution**

Designs the repeated actions, feedback, system dynamics, progression, and experiential qualities that make an interactive system understandable, engaging, and worth returning to.

**Typical artifacts**

- One-page game or experience vision.
- Design pillars and anti-goals.
- Player role and verb vocabulary.
- Core, supporting, session, and long-term loops.
- Mechanics–Dynamics–Aesthetics map.
- Feedback and resource-flow map.
- Beat chart.
- Playable prototype.
- Playtest observations and tuning notes.
- Onboarding and game-feel guidance.

**Evidence sought**

- What the player notices and does without coaching.
- Whether mechanics produce the intended dynamics.
- Whether those dynamics produce the intended understanding and feeling.
- Player prediction, agency, trust, curiosity, and willingness to continue.
- Comprehension after motion or feedback ends.
- Unwanted dynamics such as anxiety, blame, confusion, or compulsion.
- Robustness across accessibility and presentation conditions.

**Depends on**

- A specific player and desired experience.
- Explicit mechanics, actions, and feedback.
- A prototype real enough for the relevant dynamics to emerge.
- Observational playtesting rather than design critique alone.
- Freedom to tune or remove mechanics after play.

**Failure modes it helps prevent**

- Functionally correct but inert or unpleasant interaction.
- Decorative gamification disconnected from real work.
- Designing a board more completely than the play.
- Mechanics that create unintended behavior or emotion.
- Feedback that is attractive but incomprehensible.
- Onboarding by explanation rather than experience.

### Domain-Driven Design

**Contribution**

Discovers and preserves domain truth through shared language, meaningful boundaries, explicit relationships, behavior, policies, and models that can evolve without collapsing into storage or interface structures.

**Typical artifacts**

- Domain vision and core-domain statement.
- Ubiquitous Language glossary.
- Event-storming model.
- Domain scenarios and examples.
- Subdomain analysis.
- Bounded Contexts and Context Map.
- Invariants and policies.
- Domain Events, Entities, Value Objects, and Aggregates.
- Minimal tactical model for the selected capability.

**Evidence sought**

- Domain-expert agreement on language and distinctions.
- Ability of the model to explain real cases and changed reality.
- Rules that remain coherent across boundary and exception cases.
- Correct preservation of invariants and history.
- Clear ownership of meaning and consistency.
- Reduced translation between conversation, design, and code.

**Depends on**

- Access to domain experts and real work.
- Concrete episodes and examples.
- Discipline to separate domain truth from UI, persistence, and service structure.
- Willingness to leave questions open until evidence requires resolution.
- A selected slice to constrain tactical modeling.

**Failure modes it helps prevent**

- Modeling the database or UI instead of the domain.
- Ambiguous or inconsistent language.
- Loss of important distinctions and history.
- A single oversized model that hides context boundaries.
- Premature service or Aggregate boundaries.
- Software that becomes untruthful when reality changes.

### Behavior-Driven Development

**Contribution**

Uses collaborative conversations and concrete examples to discover significant behavior, expose ambiguity, align participants, and preserve agreed outcomes as living executable specifications where useful.

**Typical artifacts**

- Example map containing outcome, rules, examples, and questions.
- Declarative Given/When/Then scenarios.
- Boundary and exception examples.
- Observable acceptance criteria.
- Executable specifications at stable boundaries.
- Supporting lower-level automated tests.
- Living behavioral documentation.

**Evidence sought**

- Participants interpret the examples the same way.
- Concrete cases expose and resolve ambiguous rules.
- The implemented system produces the agreed observable outcomes.
- Important boundary and exception cases remain coherent.
- Specifications continue to match deployed behavior.
- Domain and representation behavior are verified at appropriate boundaries.

**Depends on**

- A valuable capability and actor outcome.
- Shared domain language.
- Product, domain, and delivery perspectives in the discovery conversation.
- Concrete representative examples.
- An implementation boundary stable enough to automate when appropriate.

**Failure modes it helps prevent**

- Requirements that different participants read differently.
- Examples arriving only after implementation.
- Automation of misunderstood behavior.
- Technical conformance without business meaning.
- UI details contaminating domain rules.
- Feature files becoming a second unreadable test language.

### Agile development

**Contribution**

Organizes work into small usable increments, establishes a feedback-producing delivery rhythm, and continually reorders work based on evidence and changing priorities.

**Typical artifacts**

- Product and release goals.
- Story map.
- Ordered backlog.
- Thin user stories and acceptance criteria.
- Definition of Done.
- Tracer bullet or walking skeleton.
- Working increment.
- Review findings and reordered backlog.
- Lightweight delivery and quality measures.

**Evidence sought**

- A real person can use the increment end to end.
- The increment advances the product goal.
- Feedback arrives early enough to change direction cheaply.
- Work completes in small batches rather than accumulating by component.
- Quality and operability survive incremental change.
- The backlog changes in response to learning.

**Depends on**

- A product goal and ordered priorities.
- Work sliced by usable outcome rather than component.
- A team capable of completing the slice end to end.
- A usable environment and lightweight Definition of Done.
- Regular access to review and feedback.

**Failure modes it helps prevent**

- Long delivery batches and late integration.
- Component completion without user value.
- Fixed plans that ignore learning.
- Feedback arriving after expensive commitment.
- “Done” meaning coded but not usable or operable.
- Discovery and delivery becoming disconnected queues.

## Activity crosswalk

The following map shows how each lens contributes to recurring activities. It intentionally allows several lenses to address the same activity from different perspectives.

### 1. Establish purpose and strategic intent

| Lens | Contribution |
| --- | --- |
| UCD | Gives organizational purpose a human referent: who must benefit and what progress means for that person. |
| Lean/BMC | Keeps durable vision separate from product, strategy, and business-model hypotheses that may change. |
| Game design | Translates intent into a high concept and desired player experience. |
| DDD | States the domain vision and identifies the likely core domain. |
| BDD | Uses the desired outcome to keep behavior examples valuable rather than merely testable. |
| Agile | Expresses near-term direction as a product or release goal that can guide ordering. |

### 2. Identify the people involved

| Lens | Contribution |
| --- | --- |
| UCD | Selects a real-person-anchored persona from real candidates and keeps jobs situated. |
| Lean/BMC | Distinguishes users, beneficiaries, champions, buyers, approvers, blockers, partners, and segments. |
| Game design | Identifies the player and the role or identity through which they experience the system. |
| DDD | Identifies domain experts, actors, organizational responsibilities, and context ownership. |
| BDD | Brings the relevant product, domain, and delivery perspectives into example conversations. |
| Agile | Makes the user or stakeholder visible in goals, stories, reviews, and prioritization. |

### 3. Observe the current situation and establish a baseline

| Lens | Contribution |
| --- | --- |
| UCD | Observes actual work, tools, artifacts, workarounds, constraints, emotions, and breakdowns. |
| Lean/BMC | Measures current behavior, problem consequence, alternatives, commitment, and economic conditions before intervention. |
| Game design | Studies existing interaction patterns, mental models, feedback expectations, and analogous playable systems. |
| DDD | Reconstructs real episodes to discover events, relationships, policies, and language. |
| BDD | Mines concrete examples and counterexamples from actual cases. |
| Agile | Uses current performance and feedback delay to inform goals and the smallest valuable change. |

### 4. Define jobs, outcomes, and value

| Lens | Contribution |
| --- | --- |
| UCD | Defines the root and supporting jobs carried by a person in a situation; progress on the job is the governing test. |
| Lean/BMC | Frames the value proposition and the customer or business outcome believed important enough to drive action. |
| Game design | Defines experiential outcomes—what the player should understand, feel, and be motivated to do. |
| DDD | Connects Objectives and domain outcomes to the work and Decisions that serve them. |
| BDD | States the actor outcome that gives a capability and its examples meaning. |
| Agile | Converts desired outcomes into product/release goals and user-visible increments. |

### 5. State hypotheses and uncertainty

| Lens | Contribution |
| --- | --- |
| UCD | Treats the persona, jobs, needs, and proposed design as understandings to validate through observation. |
| Lean/BMC | Explicitly records, ranks, and tests product, market, channel, revenue, cost, partnership, and growth assumptions. |
| Game design | Treats the link from mechanics through dynamics to experience as a design hypothesis. |
| DDD | Records open modeling questions and allows the model to change with newly understood reality. |
| BDD | Makes unresolved questions a first-class output of example mapping. |
| Agile | Orders work by value, risk, and learning while keeping plans revisable. |

### 6. Establish shared language and models

| Lens | Contribution |
| --- | --- |
| UCD | Provides language grounded in the persona's work, motives, and situation. |
| Lean/BMC | Defines business-model terms, hypothesis boundaries, and distinctions among separate products and actors. |
| Game design | Names the player role, verbs, mechanics, loops, resources, feedback, and desired experience. |
| DDD | Establishes the Ubiquitous Language, domain distinctions, Relationships, boundaries, and conceptual model. |
| BDD | Tests whether language carries the same meaning in concrete behavioral examples. |
| Agile | Keeps goals, stories, reviews, and work items understandable across disciplines. |

### 7. Define the intended experience and design constraints

| Lens | Contribution |
| --- | --- |
| UCD | Derives requirements and constraints from the persona, job, context, accessibility, and desired progress. |
| Lean/BMC | Constrains experience experiments to the value and adoption hypotheses being tested. |
| Game design | Defines vision, pillars, anti-goals, aesthetics, feedback, progression, onboarding, and game feel. |
| DDD | Requires the interface to reveal domain truth rather than invent convenient falsehoods. |
| BDD | Makes significant experiential outcomes observable without reducing every quality to UI implementation detail. |
| Agile | Keeps constraints visible in acceptance criteria, Definition of Done, and review. |

### 8. Map journeys, workflows, beats, and loops

| Lens | Contribution |
| --- | --- |
| UCD | Maps the person's current and intended journey through a situated job. |
| Lean/BMC | Maps acquisition, adoption, delivery, payment, and learning journeys where relevant. |
| Game design | Defines moment-to-moment, core, session, and long-term loops plus pacing and beats. |
| DDD | Maps event flows, commands, policies, actors, and process boundaries. |
| BDD | Selects capabilities and scenarios within those flows for concrete discovery. |
| Agile | Uses story mapping to organize activities and draw usable release slices across them. |

### 9. Discover rules through examples

| Lens | Contribution |
| --- | --- |
| UCD | Supplies representative tasks, contexts, exceptions, and human consequences. |
| Lean/BMC | Turns beliefs into falsifiable statements with expected results and failure thresholds. |
| Game design | Defines mechanics and tests how rules combine into dynamics, balance, and feedback. |
| DDD | Discovers invariants, policies, Domain Events, and model boundaries through real cases. |
| BDD | Facilitates example mapping and expresses agreed behavior as concrete scenarios. |
| Agile | Uses examples as acceptance criteria for thin increments and review. |

### 10. Choose what to learn or deliver next

| Lens | Contribution |
| --- | --- |
| UCD | Prioritizes a persona–job–scenario and keeps uncovered jobs visible without blending them. |
| Lean/BMC | Selects the assumption that is most damaging if false and least supported by evidence. |
| Game design | Selects the core mechanic, loop, or experiential uncertainty that must become playable. |
| DDD | Selects a domain capability rich enough to clarify important behavior while constraining modeling. |
| BDD | Selects a valuable capability with rules and questions worth resolving. |
| Agile | Orders the backlog and chooses the smallest valuable end-to-end slice. |

### 11. Bound the intervention

| Lens | Contribution |
| --- | --- |
| UCD | Defines minimum viable relative to one persona and job, not merely less functionality. |
| Lean/BMC | Chooses the cheapest credible experiment capable of changing confidence in a hypothesis. |
| Game design | Prototypes the smallest loop or mechanic capable of producing the relevant dynamic. |
| DDD | Models only the concepts and consistency required by the selected domain slice. |
| BDD | Specifies only enough examples to establish significant behavior and boundaries. |
| Agile | Slices work vertically and defines a usable release boundary and Definition of Done. |

### 12. Create a prototype or experiment

| Lens | Contribution |
| --- | --- |
| UCD | Makes the proposed interaction attemptable with representative tasks and content. |
| Lean/BMC | Designs the experiment, commitment requested, measurement, and thresholds. |
| Game design | Makes mechanics and feedback playable at sufficient fidelity for dynamics to emerge. |
| DDD | Uses models and simulations to test language, behavior, and boundaries before hardening implementation. |
| BDD | Uses examples to drive the prototype's significant observable behavior. |
| Agile | Time-bounds exploratory work and turns sufficient learning into the next deliverable slice. |

### 13. Build a thin working slice

| Lens | Contribution |
| --- | --- |
| UCD | Keeps the slice usable by the selected persona for the selected job. |
| Lean/BMC | Includes only the capability needed for the next Build–Measure–Learn cycle. |
| Game design | Preserves the core loop and enough feedback quality to test the intended experience. |
| DDD | Implements the smallest coherent domain behavior and history needed by the slice. |
| BDD | Drives implementation outside-in from agreed examples and stable observable boundaries. |
| Agile | Coordinates an end-to-end tracer bullet or walking skeleton that is operable and reviewable. |

### 14. Evaluate correctness and agreed behavior

| Lens | Contribution |
| --- | --- |
| UCD | Notices when technically correct behavior still fails the person's actual job. |
| Lean/BMC | Checks experiment integrity so implementation defects are not mistaken for hypothesis evidence. |
| Game design | Checks rules, state, feedback, and deterministic outcomes needed for fair and comprehensible play. |
| DDD | Verifies invariants, history, domain distinctions, and truthfulness under changed cases. |
| BDD | Verifies the system produces agreed outcomes for significant examples and boundaries. |
| Agile | Includes appropriate testing, integration, operability, and review in Done. |

### 15. Evaluate human use and experience

| Lens | Contribution |
| --- | --- |
| UCD | Observes task performance, comprehension, effort, confidence, accessibility, and progress in context. |
| Lean/BMC | Observes use as evidence for value, adoption, retention, and maintenance-cost hypotheses. |
| Game design | Playtests attention, agency, prediction, dynamics, emotion, game feel, and willingness to continue. |
| DDD | Observes whether the representation and language match how domain participants understand reality. |
| BDD | Checks whether examples omitted important human or representational outcomes and feeds questions back into discovery. |
| Agile | Brings the working increment to review and incorporates feedback into ordering. |

### 16. Evaluate business viability and growth

| Lens | Contribution |
| --- | --- |
| UCD | Shows whether the offering produces meaningful human value for a strategically relevant person. |
| Lean/BMC | Tests segments, value propositions, buyers, channels, relationships, revenue, resources, activities, partners, costs, and repeatability. |
| Game design | Contributes evidence about engagement, return, onboarding, and experience-driven adoption without equating them to commercial viability. |
| DDD | Identifies costly domain complexity, integration boundaries, and capabilities that may affect delivery economics. |
| BDD | Makes promised or contracted business behavior explicit and verifiable where appropriate. |
| Agile | Supplies small releases, delivery data, and responsiveness needed to test commercial assumptions incrementally. |

### 17. Learn, update, and preserve memory

| Lens | Contribution |
| --- | --- |
| UCD | Updates understanding of the person, job, situation, and design separately; preserves uncovered jobs. |
| Lean/BMC | Updates confidence, canvas, hypothesis register, evidence log, and persevere/adapt/pivot decision. |
| Game design | Tunes or removes mechanics and updates pillars, loops, playtest findings, and experience targets. |
| DDD | Evolves language, model, boundaries, policies, and history to remain truthful. |
| BDD | Revises examples and executable specifications so they remain shared living documentation. |
| Agile | Reviews outcomes, updates goals and backlog, and changes the plan based on evidence. |

### 18. Expand or scale behind evidence

| Lens | Contribution |
| --- | --- |
| UCD | Adds personas or jobs deliberately and sequences them through the roadmap to mind gaps. |
| Lean/BMC | Expands after evidence of demand, viable acquisition, delivery economics, and repeatability. |
| Game design | Adds mechanics, content, progression, or complexity only after the core experience works. |
| DDD | Adds contexts, integrations, or platform capabilities when real domain boundaries and demand require them. |
| BDD | Grows significant examples with behavior while avoiding exhaustive specification noise. |
| Agile | Delivers additional capability incrementally and preserves adaptability as scope grows. |

## Crosswalk boundaries

This document does not yet decide:

- Which activities are genuinely shared versus merely similar.
- Which lens should lead or follow at a particular moment.
- Whether any artifacts can be combined safely.
- Which tensions should become explicit decision rules.
- What order or cadence the reconciled process should use.
- Which activities are always required versus pulled by context.

Those are step 3 questions. The purpose of this step is to make the raw contributions visible before interpreting their relationships.

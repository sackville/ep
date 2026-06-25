# Persona-Driven UCD and Jobs to Be Done — Synthesis for ISS

*A working synthesis of how we build applications: how User-Centered Design, Jobs to Be Done, and personas fit together, and how that frame interlocks with our EP, ToMo, and Viper concepts. This is a living document and sits at the leading edge of EP and Viper thinking; as the ideas sharpen, refinements flow back into the standalone EP and Viper projects.*

---

## Who this is for

**Primary persona: Claude.** Its job is to help Scott design the first ISS application using the Viper method. This document exists so that an AI collaborator loads the right frame *before* touching any design, architecture, or prioritization question — who we are building for, and why, before deciding what to build. When that frame is missing, an AI fills the gap with generic assumptions, the same way any collaborator working without context does.

**Secondary persona: Russ.** His job is to understand our approach — Viper, EP, UCD, ToMo — well enough to participate in it.

Two personas here is not a violation of our own discipline. The "one persona" rule guards against multiple personas *competing over the same feature*. These two hold genuinely different jobs, which is exactly the legitimate case for a second persona.

---

## The core commitment

The most important thing we do is help a specific person get something done. Every design choice, architectural decision, and priority call is ultimately in service of that. When organizations lose sight of it, they ship software that satisfies procurement checklists and internal politics while failing the human at the desk — the default condition of enterprise software, and the thing we exist to refuse.

---

## Jobs and personas are not rivals

This is the reconciliation the rest of the method hangs on.

**A job is the atomic unit of analysis. A persona is the unit of design focus.** You don't choose between them, and you don't subordinate one to the other.

Jobs are how we *discover and define* personas: we identify real people, learn the jobs they are trying to make progress on, and group people by the similarity of their job lists to see where the strategically dense, high-value jobs cluster. The persona, in turn, is the carrier that keeps a coherent bundle of jobs attached to a real situation — its constraints, its environment, and the motivation behind it.

We therefore reject Jobs-to-be-Done *purism* — the "fire the persona, the job is the only unit" position. Not because jobs aren't central; they are at the core of every design and the foundation of every test. But a job stripped of its person loses the situation and the motivational texture, and that texture is the actual design target (see the ToMo primer: the direct motives are what produce adaptive performance, and they live in a person, not in a disembodied task). A bare job is a record. A persona is a character. This is the same discipline the GameStorming work surfaced as a runtime mechanic: *one persona, always a person in a situation.*

So: jobs in. Persona-as-carrier-of-jobs in. Disembodied-job-as-sole-unit out. The persona is what keeps the job *situated*; the job is what keeps the persona *honest*.

---

## How a persona comes to be (the method in brief)

The full step-by-step procedure for creating personas is being revised (see Open Threads). What follows is the *logic* of the current method, which is what an AI collaborator needs to reason correctly even before the procedure is rewritten.

We start from real people — segmentation and target identification get us to actual candidates, and we interview them rather than guessing from a conference room. (Get out of the building.) From those conversations we extract jobs, then reconcile them — dedupe, summarize, generalize, decompose — into a canonical set. We map which people hold which jobs, then group people by the similarity of their job lists.

Two principles govern this:

- **Jobs re-segment people.** Whatever a-priori categories we walked in with, we throw them away and let the jobs define the groupings. This is the move that keeps personas grounded in what people are trying to accomplish rather than in demographics or org-chart roles.
- **The clustering is diagnostic, not generative.** Grouping people by job-similarity tells us where overlap and strategic value concentrate, so we can prioritize people and pick our favorites. It does **not** produce the persona by blending the group together.

When it's time to create the persona, we select a single real favorite — chosen for the strategic value of *their* personal job list — and we carry *that person's actual jobs* onto the profile. The persona artifact still abstracts away from the individual, but it is anchored to a real list, not a composite.

**The guardrail.** The one place a composite can sneak back in is the job list itself. Once you've seen the people-by-jobs matrix, the temptation is to pad the favorite's list with high-value jobs their neighbors hold, so the persona "covers" more people. The moment you do that, you've rebuilt a fictional person no real human matches. The discipline: the persona's jobs stay a real person's real jobs (or a principled subset). Jobs you choose not to carry go onto the *roadmap to mind the gaps* — never onto the persona.

The persona then becomes the shared benefactor across the organization — the figure on the poster or the trading card that marketing, sales, product, and engineering all build toward. Because the persona is derived from the same pipeline that begins at the target customer / acquisition contact, the marketing-persona and the product-persona can't drift apart: they're built from one source. The method is itself the alignment mechanism.

---

## Aggregation is the enemy of delight

A persona built from averages describes nobody in particular, and software built to delight nobody in particular delights nobody. The operative word is *averages*. Our method never averages — it *selects* a real exemplar and retains them at full fidelity. Selection discards the people you didn't pick; aggregation blends everyone into someone who doesn't exist. Only the second erases the individual, and that erasure is the enemy.

---

## "One persona per feature"

This is two claims:

1. A restatement of the UCD principle that *the ideal number of personas for a product is one* — with **ideal** doing the heavy lifting. At the product level, multiple personas are often unavoidable.
2. A far more attainable version of the same discipline at the feature level, where designing for more than one persona rarely makes sense.

It does **not** mean only one persona will ever care about a feature. It means a feature built to delight one well-chosen persona will tend to delight others with similar needs, while a feature built to satisfy several at once fully satisfies none. The rule is also a focusing device: naming one persona and one job defines everything the feature does *not* need to do right now, which is what makes "minimum viable" a meaningful claim rather than just "we built less."

---

## Sequencing — which persona, when

Sequencing isn't a separate prioritization exercise; it falls out of the work already done.

The **primary** persona is the one whose job list is densest with strategic jobs. The remaining personas are sequenced by two things: the strategic value of *their* remaining jobs, and the **dependencies** among jobs and features — some personas can't be served until the infrastructure built for the primary exists. The *roadmap to mind the gaps* is not a separate document; it **is** the sequencing artifact, and it's also where the honestly-uncovered jobs live.

---

## The test that governs everything

For any feature, any spec, any line of code, the foundational test is: **does it get the job done — for the persona?**

That question is the acceptance criterion above all the others. It connects directly to the ToMo distinction: a feature can pass every explicit, encodable check (tactical conformance) and still fail to help the person make progress (the adaptive target). The persona-and-job test is how we keep the adaptive target in the room, because it's the one thing a checklist structurally can't hold — it's a judgment about whether a human made progress, not a box to tick. EP already embraces UCD on exactly this basis: the whole point of a playable interface is to make the consequences for that person *visible*, so the test can actually be answered.

---

## On specs (a held position)

UCD sits **upstream** of spec-driven development. A spec describes what to build to satisfy stated acceptance criteria, but it presupposes a *who* and a *why* it neither generates nor validates. Personas, their goals, their jobs, and the scenarios that follow are the headwaters; the spec is a downstream tributary. The risk in the current spec-driven tooling is that it makes skipping the upstream work *easier*, because an executable spec looks authoritative — it can launder the absence of UCD into a confident artifact built on an unexamined premise. Locally correct, globally wrong, and faster than before.

We are not positioning against SDD publicly right now; that's potential blog/LinkedIn outreach for later, if and when others raise it. EP remains open to whatever real value SDD offers at the tactical layer. The position above is the frame we hold internally, not a manifesto we're shipping.

---

## Terminology

We say **persona**. We've retired "ad hoc," following Tamara Adlin, who dropped both "ad hoc" and "data-driven" as qualifiers and simply uses the term. When we're explicitly contrasting with data-driven personas or with specs, we may reach for a precision phrase — *singular, real-person-anchored persona* — but the default term is just *persona*.

---

## Open threads

- **The v3 persona-creation procedure needs updating.** The detailed how-to in the older Ad Hoc Persona Guide predates the current method (real-candidate interviews, the people-by-jobs matrix, diagnostic clustering, single-exemplar instantiation). Deferred, not forgotten.
- **Outward UCD/SDD positioning** (blog or LinkedIn) — to be developed only if/when it would help others, and only once someone else brings SDD to the table.
- **Personanator** is expected to be pulled into the ISS application fold, possibly under a different name, with the project itself likely retired after it's stripped for parts. Nothing here edits or depends on it.

# The Viper Method: Principles and Mechanics

*Status: living working document. Last revised 8 June 2026.*
*Companion to [Viper: A Short Tour](Viper-A-Short-Tour.md). Proceeds from the principles in [FOUNDING.md](FOUNDING.md) and [persona-universality.md](persona-universality.md).*

---

## What this document is

*A Short Tour* tells the story of Viper — where it came from, what the diagram shows, how a diagram became a method and a method produced a platform. This document records the mechanics underneath that story: the axiom the whole thing rests on, the disciplines that follow from it, and the three hard governance questions any platform built this way must answer — when an application-local capability becomes a platform capability, how the platform handles needs that only become reachable once it exists, and who pays for any of it.

Two framing notes before the substance.

First, this is the *Method*, abstracted from any one instance of it. The reference instance carries codenames — Foundry, Sentinel, Vanguard, Arsenal, Intel — drawn from a defense-sector vocabulary that happened to suit the team that coined them. A real-world instance, including the one we will build for ISS, may not be called Viper at all, and the military naming will not travel. So everything here describes *roles and disciplines*, never brand. If a concept in this document depends on the word "Viper" or "Squadron" to make sense, that is a defect in the writing, not a feature of the Method.

Second, a word on epistemic status, because precision here is worth the effort. The claims in this document are not all the same kind of thing. Some are **axioms** — accepted as foundational and not argued from anything prior. Some are **disciplines** — practices derived from the axioms. Some are **models** — representations that simplify a decision. And some are **bets** — hypotheses of value still awaiting their proof. Where it matters, the status is named.

---

## The founding axiom: all requirements are user requirements

Everything in Viper rests on a single axiom, and it is the same one that grounds Personanator: **the most important thing we can do is help people get things done.** Stated as a constraint on what gets built, it becomes sharper still — *all system requirements are, or are derived from, user requirements. We build nothing that does not help some specific person accomplish something.*

The usual objection arrives immediately and it is worth meeting head-on, because how it is answered determines whether the axiom holds. The objection: security is not a user need. It is a compliance need, a business need, a cross-cutting concern that exists whether or not any user ever asks for it.

The answer is that security is a compliance, business, and cross-cutting concern, and the *only reason any of those matter* is that the system and its outputs must be as secure as its users need them to be. A clinician using a system in a regulated hospital network needs a very particular and very high standard of security; a visitor sharing an email address with a static marketing site needs the modest assurance that the address will not be harvested by an interloper. The standard differs because *the users differ*, and the differing standards are user needs. A user's requirements include the conditions under which they must work: the tools they already use, the networks they sit on, the regulatory environment that constrains them. Those are not separate from the user — they are part of the situation the user is in. There is no such thing as a system requirement that does not bottom out in a person trying to accomplish something within some set of constraints. The constraints are the user's; therefore the requirements are too.

This axiom has real teeth, but only if two conditions are met, and both deserve to be written down because each guards against a way the axiom can quietly fail.

**The definition of "user" must be generous.** A platform component that no end user ever touches still serves *someone* — the application team that consumes it, the operator who keeps it running, the developer who builds against it, even the AI collaborator working alongside the team. The chain from a deep infrastructure capability to a person getting something done may be long, but it exists, and every link in it is a user of the link above. Narrow the definition of "user" to "end user with a mouse" and the axiom collapses: half the platform becomes unjustifiable and the people who weaponize the narrow reading use it to kill necessary work. Broaden it to *anyone trying to make progress with or through the system* and the axiom holds across the entire stack. This is the same move Personanator makes when it insists that a persona is owed to the developer building for themselves and to the AI in the loop, not only to the customer.

**The axiom must be chained to persona discipline, or it becomes a rationalization.** "It's a user need" is infinitely flexible. Anyone can invent a plausible beneficiary *after* they have already decided to build the thing they wanted to build. The axiom only protects against waste when it is forced to name a *specific* person in a *specific* situation getting a *specific* thing done — which is precisely the persona discipline: one persona per feature, a portrait of a person in a situation rather than a demographic average, the job stated as the progress the person is trying to make. These are not two separate commitments. The axiom says *why* you build; the persona discipline is the test that keeps the "why" from going vacuous. Together they form a closed loop. Neither survives alone: the axiom without the persona is unfalsifiable, and the persona without the axiom is decoration.

It is worth being honest about epistemic status here. The axiom — help people get things done; all requirements are user requirements — is exactly that, an axiom, accepted as foundational. The *claim that rigorous, singular, ad hoc personas applied across the full stack produce better outcomes than the alternatives* is a **hypothesis**, and proving it is the work of Personanator. Viper consumes that hypothesis as if it were true and will benefit from its proof; the Method does not itself constitute the proof.

One consequence of the axiom matters so much to the rest of this document that it deserves its own sentence. **"Minimum viable" is only a meaningful concept relative to a specific user and a specific job.** Without a persona, minimum viable degrades into "we built less." With a persona it means "we built exactly what this person needs to accomplish this thing, and nothing else yet." That distinction is what makes the next section possible.

---

## The build discipline: demand-pull

From the axiom follows the discipline that defines the Method in practice: **build only behind a clarified, validated need — never ahead of one.** Domains lead; the platform follows; and the platform extends only after a real minimum viable product has de-risked the need that justifies the extension. This is YAGNI promoted from the level of a function to the level of an architecture, and it is the shape the Viper Diagram draws — applications arriving one at a time along the top, the platform growing as a staircase beneath, each step earned by a proven application need.

The discipline borrows its unit of measure from the axiom. A "clarified need" is a persona's job made concrete enough to build against. "MVP-proven" means de-risked *for that persona* — not in the abstract, not for an imagined committee, but for the specific person whose job the application exists to serve. This is why the persona work is not a soft front-end to the engineering; it is what gives the engineering discipline something to measure against. Lean Startup's build-measure-learn loop is the same instinct at the product scale; EDGE's insistence on funding business outcomes incrementally rather than committing big money up front is the same instinct at the portfolio scale. Viper's contribution is to run that instinct all the way down into the platform architecture, where it is least common and most valuable.

The discipline earns its keep by preventing two failure modes that platforms fall into constantly.

The first is the *speculative platform*: a team builds the grand, general, future-proof substrate before any application has proven it is needed, and the result is an expensive abstraction that fits no real workload well — what Sandi Metz captured in the observation that the wrong abstraction costs more than the duplication it was meant to eliminate. The second is *organizational paralysis*: the ambitious cross-silo platform that never starts because it cannot survive the sentence "great idea, but we'd have to change everything." Demand-pull defeats both at once. It makes the speculative platform impossible by construction — you cannot build what no application has pulled — and it defeats the paralysis by shrinking the first commitment to something a single team can say yes to.

A caution that belongs with the discipline rather than against it: demand-pull is a default, not an absolute. There is a class of need that is clarified before any application appears, and the next sections deal with it. The discipline is not "never build until an application asks"; it is "never build until a need is clarified and validated against a real person." Sometimes the clarifying happens at t=0, supplied by the enterprise's regulatory and operating context rather than by an application team. That is not an exception to the rule. It is the same rule on a different clock.

---

## The Method as an adoption strategy

The most under-appreciated property of the Method is that the technical build order and the organizational adoption path are *the same shape*, and that this is deliberate.

Most platform efforts ask an organization to believe first and benefit later: commit to the vision, fund the build, migrate the teams, and trust that value will arrive once the substrate is complete. Viper inverts the sequence. It delivers value to one small, low-stakes application team as early as possible, and lets organizational belief accumulate one proven step at a time. The platform team gets to demonstrate worth — to a real team, with a real workload — before anyone is asked to bet the enterprise on it. No team is ever pushed onto a platform that has not yet earned its place in their work.

This is the difference that distinguishes Viper from a generic enterprise platform program, and it is worth stating plainly in any pitch: *a generic platform asks for belief up front and promises payback later; Viper pays back first and earns the belief incrementally.* The staircase is not only an architecture diagram. It is also the adoption curve, and the fact that one picture serves both is the whole trick.

---

## What the Method produces: the Platform

The Platform is not designed and then constructed. It is *grown* by running the Method, and what accretes over time is a demand-pulled, federally-governed collection of shared services and enablements — each one earned by a real application need, each one funded as a standing investment rather than billed to whichever team happened to need it first. Any platform grown this way ends up with the same silhouette, which is why "the Viper Platform" names both a specific artifact and a *kind* of platform: one that was grown, not poured.

Viper inherits its structural bones from Data Mesh: domain ownership, data treated as a product, a self-serve platform, and federated computational governance. What Viper adds is the part Dehghani leaves open. Data Mesh tells you *what* a healthy data architecture is made of; it is comparatively quiet on *sequencing*. Viper supplies the sequencing discipline (domains lead, platform follows, only after MVP), grounds the whole thing in the user-requirement axiom so that "data as a product" never drifts into "data for its own sake," and adds the adoption strategy so the architecture can actually be introduced into a real organization without dying in the first meeting.

In the reference instance, the Method's structural roles are embodied by named components — platform capability development (Foundry), governance and discovery (Sentinel), the self-serve service catalog (Arsenal), customer and persona development (Intel), and the continuous-improvement loop (Vanguard). These are conveniences of the instance, not parts of the Method. What follows describes the roles; the names are local color.

---

## Governance question 1: when does an application capability become a platform capability?

The diagram draws needs dropping from applications into the platform, but it does not say *which* needs drop, *when*, or *in what order*. Those omissions are the first governance question, and answering it well is where federated computational governance earns its salary.

Start from the discipline. Because the platform does not build ahead of need, a novel capability appears first *inside an application* — built by the trailblazing team, in their own domain, on their own clock. The governance question is not about the first appearance. It is about the *second*: App A built something; App B now needs the same thing; do you refactor that capability out of App A and into the platform as a shared, supported, versioned service?

The wrong way to answer is with a single number. "Rule of three" or "second customer" treats every capability as the same kind of thing, and they are not. The right answer is a **model**, and the axis of the model is *cost of divergence* — what does it cost the enterprise if every application builds its own version?

At one end sit capabilities where divergence is dangerous: security policy, identity, audit and observability, the cross-cutting concerns whose whole value is uniformity. A security policy that varies per application is not a duplication problem; it is a vulnerability surface. Audit logging that varies per application is a compliance gap. These should globalize *eagerly* — and here is the resolution of an apparent contradiction with the build discipline. Eager globalization of these capabilities does not violate "don't build ahead of need," because for a governance concern the need is clarified at t=0, defined by the enterprise's regulatory and operating context before the first application ever appears. The need was always there; it simply did not originate with an application team. Same rule, different clock.

At the other end sit domain-specific capabilities — a particular simulation solver, a bespoke transform — where divergence is cheap and the real danger is the opposite: globalize too early, bake App A's idiosyncrasies into a shared service, and condemn App B to contorting itself to fit. These should globalize *lazily*, on genuine repeated demand, with "never — keep it local" as a fully legitimate outcome.

The eager set and the lazy set are not two kinds of requirement. Under the axiom, both are user requirements: the user needs to operate safely, and the user needs the bespoke capability. What differs is the *shape* the user need takes. One is a need for consistency and protection, where divergence harms the user. The other is a need for a specific capability, where premature sharing harms the user. The old instinct to file "security" and "discoverability" under different headings than "features" is a habit worth dropping; they are all features, owed to someone, and the cost-of-divergence model tells you only how eagerly to share them.

Two operational notes complete the answer.

The first is *who senses the decision*. A team building a novel capability should be cross-functional enough to design, build, and run it, and should have access to an enabling team or an embedded platform engineer in the Team Topologies sense. That embedded person is not only there to help the application team build well — they are the **sensing mechanism** for the promotion decision. They are positioned to call the capability's class at build time: "this is the cross-cutting kind, build it clean because we will extract it" versus "this is bespoke, your team owns it for good." The enabling relationship and the governance trigger are the same machinery viewed from two angles.

The second is *sequencing*. Once several capabilities are candidates for promotion, rank them by something like the number of teams currently duplicating or blocked on the capability, multiplied by the cost of divergence, net of the cost to extract. This is weighted-shortest-job-first applied to platform capability, and it gives the governance body a concrete basis to sort against rather than relitigating each case on intuition.

Where do these decisions actually get made? In the continuous-improvement loop. The propose → design → approve workflow already documented in the vault — proposals that move from backlog to active to accepted, designs that move from drafting to review to accepted, processes that move from MVP to alive — is the live home for promotion decisions. Promotion is continuous improvement of the platform, and it should run through the same structured, reviewable, killable pipeline as any other improvement rather than happening by decree or by whoever shouts loudest.

The failure modes this model guards against are symmetric and both expensive. Promote too eagerly and you get the wrong abstraction — a shared liability that fits no one. Promote too reluctantly and you get N divergent implementations of a capability that needed to be uniform, which for the security-and-compliance class is not inefficiency but exposure. The model's only job is to tell you which error you are about to make.

---

## Governance question 2: needs that only become reachable once the platform exists

A successful platform generates a class of requirement that no application originally pulled. The canonical example is data discoverability. The first cross-silo data consumer just wants one API to one producer; nobody asks for "make all data in the organization discoverable." But once data is available across silos, the value of finding it appears — and at real scale (think of an organization left with dozens of ERP systems after an acquisition spree, or a data lake with more tables than anyone can enumerate) finding the data becomes the hard problem, the one that gates data science, cross-silo decision support, and every form of learning across the business.

It is tempting to describe this as the platform *creating demand*, and an earlier draft of our thinking did. The axiom corrects it. The platform does not create the need. The procurement team that cannot see its purchase orders across thirty-two systems *always* needed to see them whole; what it lacked was any way to act on the need, and so the need went unspoken because asking for it was science fiction. The platform's foundational capabilities make a *pre-existing, latent user need reachable* — and reachability is what lets users finally articulate things they had given up on. There is no second engine here and no special budget for speculation. There is one engine — user-need-pull — and "generative" is simply a *property* that some capabilities have: they make whole classes of latent user need reachable at once.

This reframing dictates how a generative seed is grown and who owns it.

The *vision* originates in the domain, not in the platform team. The platform team builds catalogs and policy frameworks; it is the worst-positioned group in the organization to imagine that procurement could finally reconcile its purchase orders, because that imagination requires closeness to the domain. So the seed of possibility is recognized by someone near the work, and the way it gets grown is the way any user-facing capability gets grown under the axiom: **an application team forms around the seed, finds the real users whose need just became reachable, and builds for them.** This is the correction to an earlier, wrong instinct of mine to hand generative exploration to an enabling team in the abstract. Abstract exploration with no user attached is exactly the speculative work the Method distrusts. The enabling relationship stays — embedded support, the promotion sensing mechanism — but as support, not ownership. The owner of a growing seed is always a team with users.

The guardrail is the one Viper already owns, expressed in EDGE's vocabulary: a generative seed is a **bet** — a hypothesis of value — and the application team that forms around it is the way the hypothesis is tested. Bets get periodic value review. They get funded incrementally as they prove out, and they get killed or pivoted when they do not. The minimum seed the platform builds to make a possibility reachable is itself an MVP, killed if the demand it was meant to surface fails to appear. This is how the Method builds toward the future without resurrecting the speculative-platform disaster: it never builds the speculative thing on faith; it builds the *minimum that makes a real user need reachable*, then lets a team and its users decide whether the possibility was real.

The seed lifecycle, then, moves ownership across stages. Vision lives in the domain. Growth lives with an application team and its users. Cross-cutting residue thrown off by that growth — the discoverability mechanism, the catalog, the lineage tracking — is promoted to the platform by governance question 1's machinery, once demand for it has genuinely converged. Ownership is not a fixed assignment; it follows the lifecycle stage.

---

## Governance question 3: who pays?

The funding question resolves to a single principle that sorts the whole mess: **fund a capability at the level where the decision to build it is made.**

The decision to build an application-local capability belongs to the application team, so the application's budget funds it. The decision to *promote* a capability to the platform is a governance decision made for the organization's benefit, so the platform's investment budget funds the extraction — the party that decides to globalize is the party that pays to generalize, version, and support. Runtime is the consuming application's decision, since they chose to use the capability and chose how heavily, so operating cost stays metered to the consumer. Cloud billing makes this last part clean: workloads carry clear boundaries for cost attribution, and an application team can see — and if necessary pay — exactly the compute it drives. That is rental, not tax. You pay for what you run.

The one move the principle forbids absolutely is charging *build* cost back to the trailblazer. App A's customer funding capability that App G's customer later inherits is not a billing error to be corrected; it is the cost of seeding the commons, and recovering it from the first mover destroys the willingness to be first — which is the exact behavior the entire Method depends on. Build cost and extraction cost belong in a standing platform investment budget, never on the trailblazer's invoice.

This is where the funding model and EDGE meet. EDGE's central financial move is to replace big up-front program funding with incremental funding of the outcomes to be achieved — bets funded as they prove value, killed or pivoted at periodic review. The Viper platform budget is exactly that: not a slush fund, but an investment account that funds proven and converging needs incrementally, governed by the same demand discipline that governs everything else.

And that discipline is what makes a model that otherwise smells like trouble actually safe. Treating a platform team as a cost center is the conventional enterprise answer, and conventionally it rots — cost-center platforms drift into building elegant things nobody asked for, because they have no market signal to keep them honest. Viper imports the missing signal. The platform cannot build what no application has pulled. So "platform as a funded investment center, governed by demand-pull" is not the lazy answer; it is the answer that closes the problem, because the demand discipline supplies the market accountability a cost center normally lacks. The build decision is made on behalf of the application teams that are the platform's customers, and funded at the level where that decision lives. It is less a tax than the correct place to fund platform development.

One piece of honest residue remains, and a living document should name it rather than paper over it. Cloud metering attributes *runtime* cost beautifully. It does not amortize *build* cost — the engineering effort to create a capability the first time, or to extract it the second. In a pure cost-center treatment this evaporates, because no one keeps that ledger. In an organization doing careful internal accounting, it is still open: runtime attribution solves the easy half, and build-cost amortization across present and future consumers is the unsolved half. The cost-of-divergence model at least routes the question — for the cross-cutting, compliance-driven promotions the funding argument is trivial, and for the domain-specific ones it is exactly where the argument is real and might end in "the second team funds the extraction, or rebuilds it locally." But the general mechanism for amortizing build cost fairly is left for a future revision.

---

## The three operating principles, and where they sit

Three principles are often stated as the surface identity of Viper. They are not separate from the spine described above; they are that spine expressed in day-to-day operating terms.

**Work where you are.** The platform meets teams in the tools, networks, and environments they already use rather than demanding migration. This is sometimes presented as a courtesy or an adoption tactic, and it is both, but at root it is a direct consequence of the founding axiom: a user's requirements include the conditions under which they must work, and "abandon your tools and come to ours" is a requirement imposed on the user for the platform's convenience, which the axiom does not permit. Working where you are is what the axiom looks like when applied to the user's environment rather than the user's task.

**Support decisions.** The tools Viper builds exist to help teams decide better. This is the principle that collects the payoff of generativity: cross-silo data made reachable is worth the effort precisely because it lets people decide things they could not previously decide — which is also the natural meeting point with Enterprise Playability, since a decision-support tool that is not actually used supports no decisions, and being used is a design problem about the person at the desk.

**Continuous improvement.** The platform and its processes evolve through a structured propose → design → approve loop rather than by decree. This is not only a cultural value; it is the operational home of governance question 1. Promotion decisions, generative bets, and process changes all run through the same reviewable, killable pipeline, which is what keeps the Method's discipline enforceable rather than aspirational.

---

## Foundations

For readers tracing the lineage, the Method is a synthesis rather than an invention, and it is worth being explicit about what comes from where.

Data Mesh (Dehghani) supplies the structural model — domain ownership, data as a product, self-serve platform, federated computational governance. Domain-Driven Design supplies the domain decomposition that makes ownership coherent. Team Topologies (Pais and Skelton) supplies the team shapes, and in particular the enabling-team relationship that does double duty as the promotion sensing mechanism. Lean Startup supplies the MVP and the build-measure-learn loop at product scale. EDGE (Highsmith, Luu, Robinson) supplies the funding philosophy — incremental funding of outcomes, bets as hypotheses, periodic value review, products owned by teams across their lifecycle. Jobs-to-be-done (in the Christensen lineage) supplies the operational expression of the axiom: build for the progress a person is trying to make. And the persona discipline — singular, ad hoc, a person in a situation — supplies the test that keeps the axiom honest, which is the work Personanator exists to prove.

What is distinctively Viper is the synthesis itself: demand-pull sequencing run all the way down into the architecture, grounded in the user-requirement axiom, and delivered through an adoption strategy in which the build order and the path to organizational belief are the same shape.

---

## Open questions and next revisions

This document is meant to grow. The threads currently open:

- **Build-cost amortization.** The unsolved half of the funding model, for organizations doing careful internal accounting rather than treating the platform as a pure cost center. Needs a fair mechanism for spreading first-build and extraction cost across present and future consumers.
- **The promotion threshold.** The cost-of-divergence model tells you how eagerly to share, but the precise trigger for the lazy/domain class — repeated demand of what magnitude, validated how — is still a judgment call. Worth deciding whether to formalize it or to keep it deliberately a governed judgment.
- **Generative kill criteria.** Seeds are bets and bets get killed, but the Method does not yet specify how a seed's kill-or-continue criteria are set at the moment it is funded. EDGE's periodic value review is the right frame; the specifics are unwritten.
- **The naming origin.** A minor historical note worth recording for completeness: whether "Viper Platform" was named deliberately, in recognition that the Method produces a nameable *kind* of thing, or whether it simply slid into the vocabulary from the diagram. Either is a good story; they are different stories.

Each of these is a candidate for its own section once resolved. Until then, they are named here so the gaps are visible rather than hidden — which is the only honest way to run a living document, and not coincidentally the same discipline the Method asks of everything else.

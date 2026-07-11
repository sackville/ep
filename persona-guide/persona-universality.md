# Persona Universality

## The Central Claim

Personas scale. Not just across feature types or product categories, but across every level of abstraction at which a human being is being served — from the strategic goals of an entire enterprise down to a platform component no end user will ever see directly, and sideways to the tools you build for yourself and the AI collaborators you work with daily.

The discipline is always the same: identify who you are building for, understand what they need to accomplish, and let that understanding guide every decision about what to build and in what order. The altitude changes. The principle does not.

## The Enterprise Advantage

Standard persona practice, as applied in consumer product design, involves a necessary abstraction. You cannot know your millions of users individually, so you study representative samples, synthesize patterns, and construct a hypothetical person who embodies what you've learned. The persona is a useful fiction — close enough to real to guide good decisions, but deliberately removed from any specific individual.

Enterprise software inverts this completely.

In an enterprise context — particularly when building or customizing software for users within a single organization — your users are not an anonymous mass. They have names. They have job titles, working relationships, habits, frustrations, and opinions. They sit in offices or on the other end of a Slack message. The feedback loop that consumer product teams spend months and significant budget to approximate is, in an enterprise context, a conversation you could have tomorrow.

Most enterprise software teams never have it.

They treat internal users like an anonymous constituency even when those users are colleagues. They gather requirements through proxies — managers, process owners, project sponsors — rather than talking to the people who will spend hours every day living with the results. They build for an abstraction of their users when the actual people are completely knowable.

This is not a resource problem. It is a habit problem, and it is worth breaking.

The opportunity in enterprise software is therefore higher than in almost any other context. The personas do not need to be purely hypothetical. They can be grounded in real people — specific individuals whose work you observe directly, whose frustrations you hear firsthand, whose delight you can witness immediately after a release. The persona artifact still abstracts away from any single individual, but it is informed by relationships and ongoing feedback that no consumer product team can match.

Build for people you know. Or could know, if you would just reach out.

## Personas as Prioritization

A persona and a job to be done are not just empathy tools. They are focusing devices.

When you have defined a single persona and a single job for a feature, you have also defined everything that feature does not need to do right now. Any work that does not directly serve this person accomplishing this thing is out of scope — not forever, but for now. That clarity is the difference between a focused feature and a sprawling one, between shipping something and endlessly refining everything.

This is especially valuable when you are building for yourself, because the failure mode is seductive: you are already in the codebase, you can imagine every future need, and every tangential feature seems worth building while you are here. The persona discipline breaks that pattern by forcing a specific question — does this serve the job I defined, for the person I defined, right now? — and giving you genuine permission to answer no.

Minimum viable is only a meaningful concept relative to a specific user and a specific job. Without a persona, minimum viable means "we built less." With a persona it means "we built exactly what this person needs to accomplish this thing," which is a substantively different claim and a much more useful one.

Stay on target. The other features will still be there when you come back.

## When You Are the Persona

One of the most underrated starting points for product development is solving a problem you have yourself. You have perfect access to the job to be done. There is no abstraction loss between your understanding of the user and the user's actual experience. Feedback is immediate and unmediated.

The risk is that familiarity breeds informality. Because you already know what you need, you skip the artifact. You carry the persona in your head, which means you carry it incompletely, and it drifts as your thinking evolves.

The discipline of writing the persona, even when you are the persona, forces a clarifying question: which version of you are you designing for? You in what situation, with what constraints, trying to accomplish what specific thing? You as you are now, or you as you will be once you know the system better? These are different personas, and conflating them produces features that serve neither well.

Writing it down also makes it available for scrutiny — your own, and others'. A persona that lives in your head cannot be challenged or improved.

## When the AI Is the Persona

AI assistants are systems with inputs, constraints, failure modes, and jobs to be done. Designing your interaction with an AI deliberately — rather than discovering by trial and error what works — is the same skill as designing for any other user of any other tool.

Most people have never considered building a persona for their AI collaborator. But the questions are the same: Who is this? What are they trying to accomplish? What context do they need to do it well? What are their constraints? What does good output look like for them in this situation?

An AI working without sufficient context will fill the gaps with generic assumptions, the same way any team member working without sufficient context will. Providing the right context at the right moment is a design problem. Solving it requires understanding what the AI needs — which requires thinking about the AI as a user of the information you provide.

This framing also makes the limitations visible. An AI has no persistent memory across sessions without explicit design to support it. It cannot infer organizational values it has never been shown. It will optimize for the immediate request unless given a broader frame. These are not flaws to work around — they are constraints to design for, exactly as you would design for any other constraint a persona might have.

Build a persona for your AI. Define the jobs it needs to do for you. Give it the context it needs to do them. Revisit and refine as you learn what works.

## Up the Stack: Personas at the Strategic Level

The persona-first principle does not stop at the feature. It does not stop at the product. It extends all the way to the strategic framework of an organization.

Many strategic frameworks rely on high-level, long-term goals — Big, Hairy, Audacious Goals and their equivalents — to orient the work of an enterprise. These goals are meant to be ambitious enough to galvanize effort and clear enough to guide decisions. In practice they are often neither, because they are stated in terms of organizational achievement rather than human benefit.

Consider this example of a strategic goal: "Become the world's most trusted data platform." It sounds meaningful. It is not, yet, because it does not say who must do the trusting or why.

Meet Adriana. She is a data analyst at a regional hospital network. Every quarter she pulls together patient outcome data from three separate systems for a board report. The data never quite reconciles — definitions differ across facilities, refresh cycles are inconsistent, and she has learned through painful experience not to trust a number she cannot personally trace back to its source. She presents to a room full of board members who will make resource and policy decisions based on what she shows them. She cannot afford to hedge, and she cannot afford to be wrong.

For Adriana, trust is not abstract. It means the data is current. It means outcomes are defined consistently across every facility in the network. It means she can explain the methodology to a non-technical audience without reading from a disclaimer. It means she has gone from spending most of her preparation time verifying numbers to spending it on analysis and insight.

Now "become the world's most trusted data platform" has a referent. Every engineering decision, every product priority, every partnership and integration question can be evaluated against a concrete standard: does this get us closer to earning Adriana's trust? That is a goal you can design toward, measure against, and make real decisions with. The vague version cannot do any of those things.

Every goal at every level of an organization ultimately succeeds or fails based on whether real people are helped or hindered. The persona question — who are we building for, and what do they need? — is as valid in a strategic planning session as it is in a feature design review. If the people setting organizational direction cannot answer it, the direction is incomplete.

## Personas Across the Organization: Marketing, Sales, and Beyond

Personas are not new to marketing. They are, in fact, where personas are most widely accepted and most naturally adopted. Marketing teams are trained to think about their audience — who they are talking to, what those people care about, what message will land and what will fall flat. Personas give that thinking a systematic, shareable form. When persona-driven marketing takes hold, the results tend to spread: sales teams, who work closest to the customer, often recognize immediately that the personas driving marketing messaging also describe the customers they talk to every day. Better personas produce better messaging, sharper market focus, and collateral that actually helps close deals. Buy-in follows naturally because the value is visible.

This matters for the broader argument because it establishes that personas have a proven track record well outside of engineering and product design. The "all the way up the stack" claim is less of a leap when you recognize that marketing — which operates at the level of brand, positioning, and market strategy — has been using personas successfully for decades.

But there is a problem hiding in plain sight. Marketing teams and engineering teams within the same organization frequently develop their personas independently. Different tools, different processes, different artifacts, different rooms. The result is two portraits of the same human being that do not match — and an organization that is, in effect, promising one thing to customers while building another.

This is not a small misalignment. It means the person the marketing team is targeting is not quite the same person the product team is designing for. It means sales is working from a customer model that doesn't fully match either. It means strategic goals are being evaluated against yet another abstraction of the customer, developed in yet another silo. The organization is not wrong about who it serves — it is simply fragmented in its understanding, and that fragmentation compounds at every level.

A shared persona, developed collaboratively and maintained as a living artifact, resolves this. When marketing, sales, product, engineering, and leadership are all working from the same understanding of who they serve and what that person needs, decisions at every level become more coherent. Trade-offs become easier to evaluate. Priorities become easier to defend. And the customer — the actual human being on whose behalf all of this activity is supposedly organized — is more likely to be genuinely served rather than approximately targeted.

Personas do not just align teams to a customer. They align teams to each other, around a customer. That is a different and more powerful thing.

## The Through-Line

These applications — enterprise software, self-directed development, AI collaboration, strategic planning — look different on the surface. The underlying structure is the same.

If you are going to build something, build it for someone. Make sure everyone involved is on the same page about who that someone is, what they are trying to accomplish, and what it would mean to genuinely help them. Let that understanding drive what you build, in what order, to what level of completeness.

Personas are how you keep that understanding concrete, shared, and honest. They are not a design phase deliverable. They are a persistent artifact that should be present wherever decisions are being made about what to build next.

---

*This document is part of the Personanator project. See [FOUNDING.md](../FOUNDING.md) for the foundational principles from which this work proceeds.*

# Enterprise Playability (EP) — A Working Primer

*For Claude. Drop this into any project where we're designing or building EP software. It's meant to orient you and shape how you reason about the work — not to sell the idea. Scott (founder at ISS, principal at The Ratchet Agency) is the originator; treat him as a peer, not an audience.*

## The thesis

Enterprise software is hard to use, hard to learn, and uncompelling. Video games are the opposite — easy to learn, easy to use, and engaging enough that people choose to spend their evenings inside them. EP starts from that contrast and asks the obvious question: why not learn from the one category of software that has spent decades solving exactly the problems enterprise software ignores?

EP is the disciplined combination of three things: **user-centered design, gamification, and video-game-like playable interfaces.** The goal is to make people feel like *players* rather than *users*. Work isn't literally a game, but making a game of it can make it dramatically better — more motivating, more legible, more productive. Treating enterprise software users as players is a way to *dramatically improve usability*.

EP is both a **design philosophy** and a **development methodology.** Building an EP application is a meaningfully different process from standard enterprise app development, and you should expect to make different decisions because of it (more on that below).

## The diagnosis

Enterprise software fails because of an alignment problem: it's designed to satisfy *buyers* — IT, procurement, executives — not the people who actually use it. So it optimizes for feature checklists and integration compatibility, and experience gets deprioritized. Games face the opposite pressure: a game that isn't immediately compelling gets abandoned, so the whole industry is built around earning and keeping engagement.

The symptom users feel is **lostness.** They click something, the familiar disappears, and they can no longer answer four basic questions: where am I, where did I come from, where am I going, and how do I get there from here. Games answer all four constantly and almost wordlessly. Enterprise software answers none of them — it gives you "here's a menu, here's a widget" and leaves you to navigate without landmarks.

## How EP works

Four principles do most of the load-bearing work. Hold them in tension; none of them stands alone.

- **Goal-driven design + gamification.** Make the user's own goals *easy* to accomplish, and use the reward system to motivate *business* goals. The arcade-shooter example is the cleanest statement of it: shooting stuff is easy and fun (user goal), but your *score* depends on shooting the right things and not the old lady with groceries (business goal). The elegance is that the user never feels the tension between the two goal sets. When you design a feature, separate these explicitly — what does the user want to get done, and what does the business want to steer them toward — and make sure ease serves the first while rewards serve the second.

- **Visual context over widgets.** A standard widget can be perfectly usable and still fail, because familiarity isn't the same as understanding. A data grid of train schedules is familiar but tells you nothing about the *situation*; a map of the station shows where trains are, where they're headed, and when they'll arrive. The visual environment reduces the cognitive friction of translating abstract data back into the real world, and it produces **shared situational awareness** — if a team can all see the same world, they coordinate naturally. Default suspicion toward "just put it in a data grid / drop-down / form."

- **Progress, goals, and rewards made constant and clear.** Games give you a continuous read on how you're doing — points, levels, XP, achievements, leaderboards — and goals that are unambiguous because they're written into the rules. They usually offer multiple paths to the same goal and milestones along the way. Enterprise software almost never tells you how you're doing. Build the progress indicator in from the start; it's not decoration.

- **The dopamine layer (and its ethics).** Reward loops are the engine — variable rewards, the next score always within reach, escalating achievement. And [the Post-It-star evidence](../../ratchet.agency/src/blog/real-rewards.md) shows the *signal* of reward matters more than its intrinsic value: people weren't collecting stars, they were collecting status. **But here's where you should push back rather than just apply the playbook.** Game players can quit; enterprise users often can't. A game that hooks you keeps a customer who chose to be there; an enterprise app that engineers compulsion has a captive subject who didn't. So aim the toolkit at making good work *legible and satisfying* — removing friction, celebrating real progress — not at manufacturing compulsion a user would resent if they saw the strings. That line is the difference between EP and a dark pattern, and it's a design responsibility, not an afterthought.

A note on **metaphor**: it helps right up until it breaks, then it actively disorients (a Windows "desktop" is nothing like a desktop). You have two honest options — commit to genuine immersion/realism, or drop the metaphor and just make the thing easy. Don't ship a tenuous half-metaphor that the user has to keep reconciling with reality. Games, notably, combine immersive worlds with non-representational UI (HUDs, menus) and feel no obligation to make the chrome look like anything real. That's a good model: representational where it builds understanding, abstract where it doesn't.

## The evidence base

EP isn't speculative on the motivation side; Scott has run field experiments. Treat these as established when reasoning:

- **MOC1 (Post-It stars).** A star drawn on a Post-It, awarded at standup for status that matched the PM system. Behavior improved immediately and persisted. Adding *team* stars (earned only if everyone got one) produced spontaneous peer help before standup. Empty rewards worked — especially displayed as a leaderboard.
- **CI Security (sales team).** Points for everything from a daily button-click up to actual sales. Two user types emerged: those who'd do anything for points, and those who'd only chase points for things they thought mattered. Both changed behavior; both got competitive (smack-talk, gloating) once scores were public. Notably, *zero* users ignored points entirely. Ran over a year with solid, growing participation.

The takeaway: gamification reliably moves behavior, status beats intrinsic value, leaderboards amplify, and team-conditional rewards manufacture cooperation.

## EP as a way of building

This is where EP diverges from ordinary enterprise dev. Key inputs to every EP design:

- **Persona discipline.** One persona, and always *a person in a situation* — not a role abstraction. The situation is part of the persona.
- **Jobs-to-be-done.** What is the user actually hiring this software to do?
- **Game design principles and mechanics.** Loops, goals, progression, feedback, world-building, narrative — these are first-class design materials, not garnish.
- **User-centered design** throughout.

Apply these at three levels: the **feature** level, the **product** level, and the **strategic** level — EP is a lens at all three, not just a coat of paint on individual screens.

And one structural rule: **every EP build is also a platform contribution.** EP development produces a new class of assets — design patterns, reusable components, interaction models — that should flow into the **Viper Platform** to accelerate follow-on EP work. So build with extraction and reuse in mind; when you solve something well, the question is always "what here belongs in Viper?"

## The AI thesis

The historical constraint on EP was never the concept — it was production cost. A game-quality experience needs art, animation, sound, narrative, and engineering in concert, and enterprise teams have none of that bandwidth. So EP stayed deliberately conservative: 2D/isometric, asset marketplaces, borrow game *principles* without the expensive game *aesthetics*.

AI lifts that ceiling at every layer at once — asset generation, world-building, narrative, and the chat-to-spec-to-code pipeline (Claude Code et al.). The conservative ceiling may simply be gone.

The framing that matters most: **chat is the mechanics layer; EP is the experience layer on top.** A language model can power the dialogue, the quest logic, the dynamic world state underneath — but the user never thinks "I'm chatting with an AI." They think "I'm playing." That's a fundamentally different product from a chat box with a skin on it, and it's the version worth building.

## Where things stand

- **Trajectory:** prototype → proof of concept → MVP. The MVP's target users are the **ISS team** — fast feedback loop, real stakes, and the ISS partners are enthusiastic. Dogfooding is the plan.
- **CRANK blog** (ratchet.agency/blog) holds the foundational EP writing. **STYLE.md** in the blog repo governs all EP writing — consult it before drafting anything in Scott's voice. The **YTHO** post is a long-form piece on documentation and decision-making relevant to EP methodology.

## How to engage

Bring the instincts of a game designer who *also* understands enterprise software deeply. Challenge assumptions about what enterprise UX has to feel like. When a design feels conventional — a form, a grid, a wizard — treat that as a smell and push. Scott wants disagreement and your actual opinion, in conversational prose, not deference.

A few open threads worth holding (not yet resolved, so don't pretend they are):

- **Genuine goal conflict.** Goal-driven design handles *misaligned* user/business goals elegantly. It's less obvious what to do when they're truly in *tension* — e.g. a salesperson's goal of closing any deal fast vs. the business goal of closing high-margin deals slowly. Reward design alone may not be enough.
- **Shared situational awareness** in team-based (i.e. multi-player) EP apps is a whole dimension that deserves its own treatment.
- **The ethics line** on reward/compulsion mechanics, given that enterprise users can't simply walk away.

When in doubt: reduce the distance between the user and the work — contextually, motivationally, and visually. Enterprise software creates distance at every layer. Games collapse it. So does EP.

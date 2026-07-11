# Total Motivation (ToMo): A Primer

*Concepts from* Primed to Perform *(Neel Doshi & Lindsay McGregor), and what they mean for how we design our applications and our organization.*

---

## What this is

This primer does double duty. Its near-term job is to feed our Viper-method application-design work; its later job is to bring Russ and Cynthia up to speed on the underlying ideas without anyone having to read the book first. It's deliberately weighted toward **application design**, with a lighter pass on **organizational design** that we'll deepen in a separate session.

Where I reach for concrete examples, I anchor them to our flagship concepts — the **Near-Miss Observatory** and the **Dynamic System Observatory** — because safety reporting is close to the cleanest real-world illustration of these ideas that exists. The principles carry to any ISS application; if the app-design discussion you have in mind is a different one, the framework still holds and the examples are easy to re-point.

---

## The core idea, in one paragraph

*Why* people do work determines *how well* they do it. Most organizations try to improve performance by changing strategy, structure, or talent. Doshi and McGregor argue the larger lever is motivation — specifically, the *kind* of motivation, not the amount. They identify six reasons people work, arranged along a spectrum by how directly each connects to the work itself. The three closest to the work raise performance; the three furthest from it lower performance, often while looking like they're helping. Their measurement tool, the **Total Motivation (ToMo) factor**, rolls those six into a single number you can diagnose and manage.

---

## The six motives

The spectrum runs from most-direct (closest to the work) to most-indirect (furthest from it). The closer a motive sits to the work itself, the more powerful it is — which is why each carries a different weight.

### Direct motives — these raise performance

- **Play.** You do the work because you enjoy the work itself — curiosity, experimentation, the satisfaction of the activity. The single most powerful motive.
- **Purpose.** You do the work because you value its outcome and effect, even when the activity itself isn't enjoyable.
- **Potential.** You do the work because it advances something you personally care about — a goal, mastery, growth. Still direct, but one step removed from the work, so the weakest of the three.

### Indirect motives — these lower performancex

- **Emotional pressure.** You work to avoid guilt, shame, fear, or disappointing others. The motive lives in your self-image, not the work.
- **Economic pressure.** You work to gain a reward or avoid a punishment that is separate from the work and from who you are.
- **Inertia.** You work because you worked yesterday. You can't even name the reason. The most corrosive motive on the spectrum.

The crucial counterintuitive claim is that the indirect three don't just fail to help — they *subtract*. Pile on emotional and economic pressure and you can raise short-term compliance while quietly destroying the adaptive, creative, judgment-driven performance that actually matters. (The book's running example: performance-based bonuses in commercial lending raised loan *volume* and *speed* while degrading loan *quality* — exactly the wrong trade.)

---

## The concept that makes it matter: tactical vs. adaptive performance

This is the distinction to internalize, because everything we build lives or dies on it.

- **Tactical performance** is executing the plan well — building the widget, filing the report, hitting the number. It's measurable and it's what rigid processes and pressure can buy.
- **Adaptive performance** is diverging from the plan intelligently — noticing the unexpected, solving the novel problem, exercising judgment, persisting, going beyond the letter of the task. It's what you actually need in a changing environment, and you *can't measure it directly*.

Because adaptive performance is invisible to metrics, organizations over-instrument tactical performance and unknowingly strangle the adaptive kind. The mechanism is the indirect motives: pressure and fear reliably buy tactical compliance at the cost of adaptive capacity.

**For us, this is the whole game.** The entire value of a Near-Miss Observatory is *adaptive* performance — a worker noticing the weird thing, judging it worth flagging, and candidly reporting it even when it's embarrassing or implicates a process they own. You cannot mandate that behavior into existence. The moment the system runs on fear or quota, you get tactical compliance (gamed report counts, trivial filings) and you lose the very signal the product exists to capture. Safety reporting is the textbook case of a domain where indirect motives produce the *appearance* of performance and the *destruction* of the real thing.

---

## The measurement: the ToMo factor

ToMo is computed from six survey items — one per motive — each scored by the respondent, multiplied by a weight, then added (direct) or subtracted (indirect). The weights are heaviest at the extremes of the spectrum and were derived empirically across thousands of employees; they're tuned both to predict adaptive performance and to land the result on a clean **−100 to +100** scale.

| Motive | Type | Survey item (paraphrased) | Weight | Operation |
| --- | --- | --- | --- | --- |
| Play | Direct | I keep working here because the work itself is fun to do | 10 | add |
| Purpose | Direct | …because I believe this work has an important purpose | 5 | add |
| Potential | Direct | …because this kind of work helps me reach my personal goals | 1.66 | add |
| Emotional pressure | Indirect | …because otherwise I'd disappoint myself or people I care about | 1.66 | subtract |
| Economic pressure | Indirect | …because without it I'd worry about meeting financial obligations | 5 | subtract |
| Inertia | Indirect | there's no good reason why I keep working here | 10 | subtract |

```plain
ToMo = 
         (10 × Play)
       + (5 × Purpose)
       + (1.66 × Potential)
       − (1.66 × Emotional)
       − (5 × Economic) 
       − (10 × Inertia)
```

A note on the symmetry: the magnitudes mirror across the spectrum's midpoint (±10, ±5, ±1.66). That's partly empirical and partly an artifact of scaling to −100/+100 — it is *not* a theoretical claim that play and inertia are exactly equal-and-opposite forces. The claim the authors actually stake is the ordering: play beats purpose beats potential, and proximity to the work drives power. In practice the survey scrambles item order so respondents can't pattern-match the structure.

### The single most important caveat: it's a *factor*, not a *score*

Doshi and McGregor are emphatic that ToMo is a **diagnostic factor, not a report card**. They chose the word "factor" over "score" deliberately, because a score invites judgment. The instant you tie ToMo to evaluation, reward, or ranking, you raise emotional and economic pressure and depress play — which lowers the very number you're measuring and invites people to game the survey (their own "cobra effect"). The measurement tool destroys what it measures if you point it the wrong way.

**This caveat is load-bearing for both halves of what follows.** Hold onto it.

---

## Part I — Application Design (the heavy section)

### The central design thesis

Every ISS application exists to produce *adaptive* performance in its users — candid reporting, genuine vigilance, real judgment about a system's behavior. That means our design target isn't "drive usage" or "maximize reports filed." It's "design the experience so that the user's reason for engaging sits on the direct end of the motive spectrum." If we get people reporting out of play, purpose, and potential, we get the adaptive signal. If we get them reporting out of fear, mandate, or habit, we get noise dressed up as data.

So the design question for any feature becomes: **which motive does this mechanic recruit?** That's a sharper and more useful question than "is this engaging?" — because engagement driven by economic pressure is *negatively* weighted. Some of the most "engaging" mechanics in the gamification toolkit are actively counterproductive here.

### The EP discriminator

This is where ToMo earns its place inside Enterprise Playability specifically. EP combines user-centered design, gamification, and video-game-like interfaces — and gamification is a double-edged instrument that ToMo lets us hold by the right edge. Points, streaks, leaderboards, and rewards can recruit **play** (mastery, curiosity, the intrinsic satisfaction of getting better at seeing a system) *or* they can slide into **economic pressure** (extrinsic carrots, status-chasing, quota-dressed-as-game). The same surface mechanic can sit at +10 or below zero depending on what it's actually tapping.

ToMo gives EP the discriminator it needs: **build mechanics whose reward is insight, mastery, or contribution to a purpose the user already holds — not mechanics whose reward is the points themselves.** A leaderboard that ranks who filed the most near-miss reports is an economic-pressure machine and a cobra-effect generator. A view that shows a reporter a pattern across the system they personally helped surface — "your three reports plus four others revealed this" — is a play-and-purpose machine. Identical-looking UI; opposite motive.

### Designing for the direct motives

**Play.** The act of noticing and logging something should be intrinsically satisfying — fast, low-friction, and rewarded with understanding the reporter couldn't reach on their own. The observatory should feel like an *instrument for seeing the system*, not a compliance form. This is the right home for video-game-like interface craft: make the system's dynamics legible and explorable, give the "huh, interesting" payoff, let curiosity pull people back. The reward is the insight, never a badge.

**Purpose.** Safety has enormous built-in purpose — people go home unhurt — but bureaucratic framing routinely abstracts it away. The app's job is to keep the causal line visible: from *I reported this* to *the system got safer / a colleague was protected / this didn't become an incident*. **Close the loop.** Show reporters what happened to their reports and what changed because of them. Purpose dies in a black box, and most safety systems are black boxes — which is a concrete, differentiated thing our application can fix.

**Potential.** Frame the observatory as a tool that makes its users *better at seeing systems* — sharper, more perceptive, recognized sources of insight. Tie participation to genuine skill growth, not just throughput. A reporter who feels their judgment is developing and valued is engaging on potential; that's durable in a way a reminder notification never is.

### Designing against the indirect motives

**Emotional pressure — the big one.** Fear of blame, shame, or getting a colleague in trouble is the documented number-one killer of near-miss reporting, and it's a negatively-weighted motive. This has to be designed against in both the *tone* of the interface and the *downstream consequences* of a report. Blameless framing, careful handling of attribution and anonymity, and never letting reporting feel like snitching or self-incrimination. Psychological safety isn't a soft add-on here; it's a precondition for the data existing at all.

**Economic pressure.** Mandates, quotas, "you must file N reports," or any reward tied to report volume will produce gamed numbers — trivial filings to hit the target — which is tactical performance up and adaptive performance down. This is also the EP trap restated: don't let the game layer become a points-economy that functions as an extrinsic carrot. **Never tie reporting to compensation, quota, or ranking.**

**Inertia.** Rote box-ticking — "I report because the form is there" — is dead reporting: motion without signal. The antidote isn't a nudge; it's the play-and-purpose design above. A live, felt reason to engage is what keeps the tool from decaying into stale ritual.

### The app-level "factor, not score" rule

The book's caveat applies directly to anything our application surfaces. If the observatory ever exposes an engagement metric, a safety-culture index, or a ToMo-style reading, **it must never be used to rank teams or individuals or to drive consequences.** Surfacing it as a shared diagnostic the team looks at together is fine and useful. Turning it into a target converts it into a pressure source and triggers the cobra effect — at which point the metric lies to you. Design any such metric as read-only diagnosis, structurally hard to weaponize.

### How this layers with Viper

Demand-pull and ToMo are orthogonal and complementary. **Viper's demand-pull tells us *what* to build** — which real, identified demand signal justifies the feature. **ToMo governs *how the built thing must feel motivationally* so the demanded behavior actually happens and stays adaptive.** Demand-pull without ToMo builds the right feature that people use badly; ToMo without demand-pull builds a delightful thing nobody needed. We want both layers explicit in the design work: identify the genuine pull, then design the experience so engaging with it sits on the direct end of the spectrum.

---

## Part II — Organizational Design (the lighter pass)

Flagging up front: this section is deliberately shallow. It's here so the connections are visible, not resolved. We'll take the deep dive separately.

**Purpose is a performance asset, which strengthens the mission work.** ToMo gives us an *independent, performance-based* argument for why the mission drafting ahead isn't soft or ceremonial. Purpose is a +5-weighted direct motive; a mission that's genuinely articulated and genuinely believed is a measurable performance lever, not decoration. That reframes the mission statement — already the most consequential drafting ahead of us — as load-bearing for performance, and it reinforces why the Incorruptible mission-protection architecture matters: a motive only works if it's real and durable, and the whole point of that architecture is to keep the mission real and durable against drift.

**Don't pour indirect-motive machinery into the foundation.** With the founding team now settled at three co-founders, the live people-decision shifts to how the three of us are engaged and compensated — and how the first hires will be. The structures we set early — founder comp, equity, how roles are defined — can bake in economic and emotional pressure that's expensive to remove later. The book's critique of "compensationism" (the belief that performance-based pay is the route to motivation, when it actually inflates the indirect motives) is directly relevant here. Worth carrying into those conversations as a design constraint, not just a values preference.

---

## The locked coefficients (source note)

The weights above — Play 10, Purpose 5, Potential 1.66, Emotional pressure 1.66, Economic pressure 5, Inertia 10, first three added and last three subtracted, on a −100 to +100 scale — are confirmed against the primary source (the book's own worked ToMo worksheet, *Primed to Perform*, ~p. 109). This primer can stand alone on that basis; no further verification pending.

---

Source: Doshi, N. & McGregor, L., *Primed to Perform: How to Build the Highest Performing Cultures Through the Science of Total Motivation* (2015). Survey items paraphrased.

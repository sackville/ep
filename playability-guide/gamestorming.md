# GameStorming: Lessons for Designing Playable Business Simulations

*A synthesis for the EP team — and for future Claude instances picking this up cold. Authored as analysis of a single GameStorming session (Scott guiding) in which we designed simulation games for three unrelated businesses: an independent coffee shop, a regional trucking company, and a dental practice. The games themselves are disposable. The patterns that recurred across all three are the point.*

## The short version

GameStorming is a generative design exercise: pick a business, then imagine the video game that simulates *running* it — the player as all-seeing manager, scored against the real goals of the real business. It looks like a game, but designing the game forces you to answer, fast, the exact questions Enterprise Playability cares about: What does winning mean here? What constraint keeps the player honest? What does the player actually *see*? What brings them back tomorrow? Three unrelated industries converged on the same structural answers, and that convergence is what's worth keeping.

## 1. The exercise is the method, not the warm-up

The most reusable thing here is the move itself. "Imagine the game that simulates this business" is a forcing function for EP design, because you can't make a business *playable* without first deciding its win condition, its failure condition, its core loop, and its representation. Those are the EP design questions wearing a fun hat. When you're stuck on how to make some enterprise domain legible and motivating, don't start from the screens — start from "what's the game?" The screens fall out of the answer. Run it as a conversation, keep it fast, don't get it right on the first pass; the second and third passes are where the real design appears.

## 2. Three meters, every time: waste, runway, relationship

Independently, all three games settled on the same trio of headline metrics. This looks like a genuine pattern, not a coincidence, and it's a strong default starting point for any business sim:

- **A waste-minimization efficiency metric** — the one number that captures the core operational puzzle. Trucking made it explicit: *loaded-mile %*, the fight against empty "deadhead" miles. Dental had the exact analog: *chair utilization*, where an idle operatory with a paid hygiene in it is the same bleed as an empty truck. Coffee's version lived in riding the morning rush without over- or under-staffing. Every business has a "deadhead" — a characteristic form of waste the player learns to squeeze — and finding it tends to find the game's core loop.
- **A relationship / retention metric** — where the reward and the heart live (see lessons 3 and 5).
- **Cash as a runway constraint** — present in all three, but deliberately *not* the score (see lesson 4).

If you're designing a new one and don't know where to start, name those three for the domain first.

## 3. Reward the return — repeat behavior is the truest signal

The strongest reward-design principle to come out of the session: *a customer walking back through the door tells you more than any survey ever could.* Revealed preference beats stated preference, so build the reward system around the "they came back" event rather than around a point-in-time score or a vanity metric. Each game found its own version of this and made it the emotional core:

- Coffee: repeat → regular → **referral**, with the referred customer becoming a regular as the signature combo ("crossing the chasm").
- Trucking: converting a spot-market one-off shipper into a **contracted account** with steady base freight.
- Dental: the **six-month recall flywheel** and the family that's been coming for twenty years and brings the kids.

The deeper reason this works: the return event is simultaneously the most satisfying reward *and* the truest health signal of the real business. When those two things are the same metric, you've aligned the game's dopamine with the business's actual wellbeing. That alignment is the whole game.

## 4. Cash is runway, not score

In every case we demoted cash from "the thing you're chasing" to "the thing that keeps you alive." It funds your moves — more staff, more trucks, a better espresso machine — and it ends the run if you mismanage it, but it isn't what you're rewarded for. This separation does two jobs at once. It keeps the player honest (you can never ignore the economics) without letting the game degenerate into penny-shaving, which is both tedious *and* a model of bad business. Keep the survival meter and the reward meter distinct. The player should always be able to see runway — cash on hand, burn, and the cost of the next move — as a constraint they manage, not a high score they grind.

## 5. Render relationships as characters, not records

The retention metric only has pull if the things being retained are *people with faces and arcs*, not rows in a table. Marcus the decaf regular. Dave the driver who needs to get home for his kid's game. Mrs. Alvarez, who's nervous and should be booked with the gentle hygienist. This is EP's "one persona, always a person in a situation" discipline showing up as a *runtime mechanic* rather than a design-time input — the personas live inside the running game. A retention KPI is a number a player optimizes; a named regular with a preference and a small story is someone a player *cares about not losing*. That difference is the difference between a tycoon math sim and a game with a heart.

## 6. Make the combo visible in the moment

The skill-expressing "combo" in each game — the referral chain, the cleanly chained loaded loop, the recall flywheel — only pays off emotionally if it's *legible as it happens*. You have to see "Marcus brought a friend" as an actual event, with a beat where you decide whether to comp the drink or put your best barista on bar. If the combo is just a number quietly ticking up, the payoff evaporates. General rule: any moment you want the player to feel proud of needs an in-the-moment representation, not a delayed entry in a stat screen. Reward visibility is a design responsibility, not a polish item.

## 7. Expansion is the test of system vs. luck

Every game's growth step — second store, second terminal, bigger practice — produced the same dramatic question, and it's a good one: *does the magic survive duplication?* The hand-tuned vibe, the tight dense operating region, the personal patient relationships are exactly what *don't* copy. So expansion isn't "now manage two of the thing." It's the game interrogating the player's earlier choices: did you build a transferable system — a talent pipeline, a dense network, a standard of care — or did you just get lucky with one well-tuned instance? This is where EP's strategic layer shows up, and it's powerful because it makes early decisions matter *retroactively*. It also happens to be a true thing about real business: the gap between a lucky shop and a scalable company is exactly this.

## 8. Encode the ethics in the scoring

The dental round crystallized the most important lesson, and it generalizes well beyond dentistry. The naive reward design — score production, score "case acceptance" — builds a game that *trains the player to over-treat*: recommend the crown nobody needs, watch the number climb. That's a dark pattern, and it mirrors the real-world dynamic where reputation-be-damned, extract-this-quarter incentives quietly corrode a business. The fix is structural, not a scold: make retention the dominant reward and make exploitation carry a *delayed cost*, so the win condition becomes a healthy base over time rather than maximized billing this month. The ethic lives in the scoring itself.

The general check, for any business sim *and* for real EP apps: **ask whether maximizing your headline reward would make a real version of this business worse.** If it would — if the optimal play is the exploitative play — you've mis-scored, and you should re-anchor on the long-term-health metric. This ties directly to EP's captive-user line: game players can quit, but the enterprise user (and here, the patient who can't evaluate the crown) often can't, so the responsibility to score honestly is heavier, not lighter.

## 9. Let the domain choose the board — and collapse the chaos onto it

Each game found its *natural* play surface rather than defaulting to a dashboard or a forced metaphor. Coffee wanted a cozy, slightly isometric room. Trucking wanted a live regional map with trucks crawling the interstates. Dental wanted a schedule grid — honestly closer to Tetris than to anything representational, and that's fine. Spatial work → a map; time-and-resource-packing work → a grid; place-based hospitality → a room. Let the structure of the actual work pick the representation: representational where it builds understanding, abstract where it doesn't, and never a tenuous half-metaphor the player has to keep reconciling with reality.

There's a companion move here, and it's arguably the origin of EP: hunt for the workflows that currently sprawl across *six monitors and a dozen applications* — the airline ops center scrambling between windows, the dispatcher copy-pasting between tools — and collapse that whole mess onto one legible board. The richest EP opportunities tend to be exactly the jobs that today require a human to be the integration layer between a pile of ugly screens.

## The deeper payoff: playable interfaces expose consequences

The headline isn't that these games are more pleasant than enterprise software, though they are. It's that a playable interface, by simulating cause and effect over time and rendering it legibly, makes consequences *visible that conventional dashboards bury.* Over-treatment looks terrific on a quarterly billing report and disastrous in a sim that shows you the chair sitting empty next year. A "successful" quarter built on burned-out drivers looks fine on a P&L and obvious the moment your veterans are named characters who quit. This is a hidden value of EP worth stating plainly: the right visualization doesn't just motivate — it tells the truth about the second- and third-order effects of decisions. That makes a playable interface a *decision-making tool*, not just a morale tool, and it's a strong reason to reach for EP in domains where the consequences of choices are exactly what the existing tools obscure.

When in doubt, the throughline holds: reduce the distance between the user and the work — contextually, motivationally, and honestly. These games did it by making the work into a board you can see, a return you can feel, and a consequence you can't look away from.

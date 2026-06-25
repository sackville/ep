# Viper: A Short Tour

*The Diagram, the Method, and the Platform — for Russ and Cynthia*

---

## Where it started

Viper began as a practical problem, not a theory. A set of customers needed serious High-Performance Compute to let their design engineers run simulations far beyond what their on-prem hardware could handle — but they had no team to stand up and run that infrastructure. We'd run it for them, in the cloud, and we needed an architecture that could keep absorbing new and frequently one-of-a-kind needs as more customers arrived.

The honest enterprise truth is that ambitious cross-silo platforms usually die in a single conversation: *"Great idea, but we'd have to change everything."* Too big, too slow, too risky. So rather than design one monolithic platform and push everyone onto it before it had proven anything, the approach inverted: take customer needs **one at a time**, and build only as much platform as each application actually requires. Domain-driven design gives each team ownership of its corner; data is treated as a product; and the common, cross-cutting concerns get federated up to the platform as they're proven out. The platform *grows*. It is never *poured*.

Zhamak Dehghani's Data Mesh fit this like a glove — domain ownership, data-as-a-product, a self-serve platform, and federated governance. Viper's contribution on top is the one thing Data Mesh leaves open: the **sequencing**. Domains lead, platform follows, and only after a real MVP has de-risked the need.

## The Diagram

![The Viper Diagram](Viper_Diagram.png)

To explain all this, there's a picture. Applications run along the top as golden arrows, each starting when its customer need arrives and each meeting a real demand. Underneath, the platform's capabilities grow as a dark blue staircase — every step up is a moment when a proven application need justified extending the platform. Red lines drop from the applications into the platform to show where those needs land.

The clever part is that the picture is secretly two pictures at once. Left-to-right is **time** — applications arriving one at a time. Top-to-bottom is **architecture** — apps on top, platform beneath. The staircase is the hinge between them, and it carries a quiet discipline: *the platform never builds ahead of demand.*

And then there's the name. The diagram turned out to look exactly like the profile of a fighter from *Battlestar Galactica* — the long-nosed wedge silhouette that's identical in both the old show and the new one. That fighter is called a **Viper**. So the diagram became the Viper Diagram, and everything else inherited the name.

## The Method

Pull the discipline out of the diagram and you have the **Viper Method**, which is as much an adoption strategy as a build strategy — and that dual nature is the whole trick. Most platform efforts ask an organization to *believe first and benefit later*. Viper does the opposite: prove value to one small application team as fast as possible, then let belief accumulate one step at a time. The build order and the sell-it-internally order are the same shape.

A few ideas give it teeth:

- **Try it small first.** One low-stakes application, real value early, before anyone has to buy into the grand vision.
- **Build behind proven demand, not ahead of it.** Restraint is the default. The cross-cutting concerns that *must* be consistent — security, identity, governance — are the exception, because their need is clear from day one.
- **The platform doesn't invent needs; it makes them reachable.** Users always needed to see their data whole, to learn across the business, to decide better — they just had no way to act on it, so the need went unspoken. Once data is available across the silos, those long-standing needs suddenly become satisfiable, and people start asking for things that were science fiction the day before. Viper plants small "generative seeds" — minimum capabilities that open a new possibility — and then lets a team form around each one, work with real users, and grow it into something those users will actually use.

Underneath it all sit three principles: **work where you are** (meet teams in the tools they already use rather than demanding migration), **support decisions** (the tools Viper builds help teams decide better), and **continuous improvement** (the platform evolves through a structured propose-design-approve loop rather than by decree).

## The Platform

The **Viper Platform**, then, is simply what the Method produces. You don't draw it up in advance and construct it; you grow it by running the Method, and what accumulates is a demand-pulled, federally-governed collection of shared services and enablements — each one earned by a real application need, each one funded as a standing investment rather than billed back to whichever brave team happened to need it first.

That's the elegant bit to leave you with: any platform grown this way ends up with the same staircase silhouette — the Viper profile. So "the Viper Platform" means two things at once. It's the specific platform we're building. And it's a *kind* of platform: one that was grown, not poured.

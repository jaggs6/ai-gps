# Calibration Examples

Three before/after examples showing what a default answer looks like vs. what a GPS-refined answer looks like. Use these to calibrate. If your output looks like the "default" column, you haven't pushed hard enough — run another round of push back or stress test.

---

## Example 1: Pricing question

**User asks:** "Should I raise my SaaS prices by 30%?"

**Default answer (skip this):**

> Raising prices is a balance between revenue and retention. Consider segmenting customers, grandfathering existing ones, communicating the change clearly, and testing before rolling out broadly. The right call depends on your market and customers.

**GPS-refined answer (deliver this):**

> Don't raise prices uniformly. The real question isn't whether to charge 30% more — it's whether you can repackage what you offer so the increase looks like an upgrade rather than a tax. Three moves:
>
> 1. Segment by revenue contribution. If 20% of your customers drive 80% of revenue, those are the ones to protect — not by exempting them, but by giving them a value-expansion path that justifies the new price.
> 2. Tier the offering. Add seniority/access tiers so the increase becomes a choice the customer makes (which tier?), not a fait accompli they react to.
> 3. Run the price change on smaller customers first. If churn is 15%, that's signal; if it's 40%, you've learned something cheap.
>
> If you want a sharper take, three things would change my recommendation:
> 1. What's your current churn rate, and how does it skew between top and bottom customers?
> 2. Do you have direct competitors, and where do they price relative to you?
> 3. Are your top 20% on annual or monthly contracts? (Renewal timing changes the rollout sequence.)

**What changed:** Default gave generic best-practices. Refined version takes a position (don't raise uniformly), gives specific moves in order of risk, and surfaces the 3 questions whose answers would let it sharpen further.

---

## Example 2: Career question

**User asks:** "Should I leave my job to start a company? I have 8 months of savings."

**Default answer (skip this):**

> Starting a company is a major decision with high risk and reward. Consider your runway, idea validation, support system, and risk tolerance. Many founders recommend keeping a stable income while validating, but others succeed by going all-in. It depends on your situation.

**GPS-refined answer (deliver this):**

> Don't quit yet. With 8 months of savings, you don't have a runway problem — you have a milestone problem. The variable that decides whether founders at your stage succeed isn't conviction; it's whether they validated the next milestone before they cut income.
>
> Specifically: pick one customer outcome you can reach in 8 weeks while still employed — a paid pilot, a binding LOI, a working prototype with active users. If you hit it, that's evidence the idea has legs and the savings clock isn't pressuring you. If you miss it, you saved yourself a 14-month forced job hunt.
>
> Three things would sharpen this answer:
> 1. What's the idea, and what's the most concrete validation milestone someone could hit in 8 weeks?
> 2. How flexible is your job — can you ship something on the side, or is the company restrictive?
> 3. What's your monthly burn? (8 months for one person is very different from 8 months supporting a family.)

**What changed:** Default hedged on "it depends." Refined version gives a concrete next step (validate one milestone in 8 weeks), names the variable that actually matters (milestone, not conviction), and surfaces the questions that would make the answer specifically actionable.

---

## Example 3: Technical question

**User asks:** "Should we rewrite our monolith into microservices?"

**Default answer (skip this):**

> Microservices offer benefits like independent scaling and deployment, but also bring complexity and operational overhead. Consider your team size, current pain points, and whether the benefits outweigh the costs. A gradual migration is often safer than a full rewrite.

**GPS-refined answer (deliver this):**

> Probably not — but here's how to know.
>
> Successful monolith → microservices rewrites usually have one of three triggers: (1) team size past ~15 engineers stepping on each other, (2) one part of the system has fundamentally different scaling needs (e.g., write-heavy ingestion trapped in a read-heavy app), or (3) you're stuck on a deprecated framework you can't upgrade in place. If none of those apply, you're probably solving "slow CI" or "coupled tests" with the wrong tool — and a rewrite will make those problems worse during the transition.
>
> Test it cheaply: extract one bounded service first. Pick the part with the most independent scaling needs. Run it for 3 months. If extraction makes everything easier, extract the next. If it makes things harder, you've lost weeks, not a year.
>
> Three things would sharpen this answer:
> 1. How big is your engineering team, and how often do PRs collide on the same files?
> 2. When you say "slow," do you mean response time, deploy time, or feature velocity?
> 3. Is there one specific subsystem that scales very differently from the rest of the app?

**What changed:** Default refused to take a position. Refined version takes a soft position ("probably not"), gives the three legitimate triggers, prescribes a cheap test (strangler fig), and surfaces the questions whose answers would convert "probably not" into a confident yes or no.

---

## The pattern

The refined version always:

1. **Takes a position** instead of listing trade-offs
2. **Names the actual variable** that decides the call
3. **Gives a concrete next action** — a test to run, a step to take this week
4. **Ends with 2-3 refinement questions** whose answers would let the next response be sharper still

If your refined output is missing any of these four, run another round before delivering.

# Worked Walkthroughs

Two complete GPS sequences applied to fresh prompts (not from the original video). Read these to see the technique in motion.

---

## Walkthrough 1: Hiring decision

**The original prompt:** "Should I hire my first employee or stay solo for another 6 months? I'm a freelance designer making $120k/year, fully booked."

**The first AI answer (sketched):** A balanced pros-and-cons list — pros of hiring (capacity, growth, delegation), cons (overhead, management time, hiring risk), generic recommendation to "consider your goals." Useless.

### G — Gaslight

**Move:** "I'm asking this as if I'm in front of a freelance designer who already made the wrong version of this call once and lost a year. He has zero patience for theory. Tell me what he'd want me to know."

**What changes:** AI shifts from listing trade-offs to giving a sharp opinion. Now it says things like: "The mistake first-time hirers make is hiring for capacity instead of leverage. You don't need a junior to do your work faster — you need someone who unlocks work you can't currently do."

### P — Push back

**Move:** "That's a clean framing, but it's also the thing every business book says. Give me the version a designer who hired *and fired* their first employee within 6 months would tell me — what specifically goes wrong?"

**What changes:** AI gets concrete: "The most common failure mode isn't bad hires — it's that the founder spends 60% of their time managing the new person and revenue stays flat for 4 months while the founder absorbs the salary. Your hourly rate effectively halves during onboarding."

### S — Stress test

**Gap check:** "What should I have told you for a sharper answer?"
- AI: "Whether you have systems documented, your client mix, what 'fully booked' actually means in hours, and what you'd hire someone *for* — production work, client management, or business development. Each implies a different person."

(You provide the missing context, re-ask.)

**Bias sweep:** "Check confirmation, recency, survivorship bias on this advice."
- AI catches itself: "I'm assuming the standard freelance-to-agency growth path is what you want. Some freelancers maximize income by *staying* solo and raising rates. I anchored on the 'scale up' narrative."

**Inject stakes:** "If I hire and it's wrong, I'm out $40k and 6 months of momentum. What would you change?"
- AI revises: "Don't hire full-time first. Hire a contractor for 10 hours a week on a specific project. Run the experiment — does revenue grow more than the contractor cost? If yes, expand. If no, you saved yourself the bigger mistake."

**Final usable output:** Run a contractor experiment for 6 weeks before any full-time hire.

---

## Walkthrough 2: Technical decision

**The original prompt:** "Should I rewrite my Rails monolith into microservices? It's slow and hard to deploy."

**The first AI answer (sketched):** "It depends. Microservices have benefits (scalability, independent deploys) and costs (complexity, ops overhead). Consider your team size and traffic." Aggressively useless.

### G — Gaslight

**Move:** "Imagine a senior engineer is reviewing this who has personally rewritten three monoliths into microservices and hated all three outcomes. Walk me through this the way you'd defend it to her."

**What changes:** AI takes a position: "Most monolith-to-microservices rewrites fail because they're solving the wrong problem. 'Slow' and 'hard to deploy' rarely mean you need microservices — they usually mean you need to fix your tests and your CI."

### P — Push back

**Move:** "OK, but that sounds like the standard 'don't rewrite' advice from every Hacker News thread. Give me the angle from someone who *did* rewrite successfully and would do it again — what made their case different?"

**What changes:** AI gets specific: "Successful rewrites usually have one of three triggers: (1) team size has grown past Conway's limit (~15 engineers stepping on each other), (2) one part of the system has fundamentally different scaling needs (e.g., a write-heavy ingestion pipeline trapped inside a read-heavy app), or (3) you're stuck on a deprecated framework. If none of those, the rewrite is probably a status game."

### S — Stress test

**Gap check:** "What should I tell you for a real recommendation?"
- AI: "Team size, current deploy frequency, what 'slow' actually means (response time? deploy time? feature velocity?), and what specifically is hard about deploying — coupling between modules, test suite, or infra."

**Bias sweep:** "Check for biases."
- AI: "I'm anchored on the 'monolith-good, microservices-bad' counter-narrative that's popular right now. Some teams genuinely benefit from the split. I've been biased toward the contrarian advice."

**Inject stakes:** "If I rewrite and it's the wrong call, I lose 9 months of feature velocity and possibly a co-founder who quits over the decision. What changes?"
- AI: "Don't make this an all-or-nothing call. Extract one bounded service first — pick the thing with the most independent scaling needs. Run it for 3 months. If it makes everything easier, extract the next one. If it makes things harder, you've only lost weeks, not a year."

**Final usable output:** Strangler fig pattern — extract one bounded service, evaluate, decide.

---

## What to notice

Both walkthroughs show the same pattern:

1. First answer = useless balanced list
2. Gaslight → AI takes a position
3. Push back → AI gets specific and battle-tested
4. Stress test → AI surfaces what you didn't ask, what it's biased about, and how it would soften under real consequences

The final answer is *implementable*, not just smart-sounding.

# Recall Drills

Answer these in your own words *before* reading the answer. Self-grade by checking what you got vs. what's listed.

## Drill 1 — The core thesis

**Q:** What is the real skill you need with AI, according to this framework? Why not "better prompts"?

<details>
<summary>Answer</summary>

Taste — the ability to look at AI output and know if it's good. Better prompts help, but the bottleneck is judgment, not prompting tricks. AI gives you 100 options; taste picks the 2 that work.

</details>

## Drill 2 — Why gaslighting works

**Q:** Why does raising stakes in a prompt produce better output? It's not because you "tricked" the model.

<details>
<summary>Answer</summary>

LLMs are trained on human text. In human writing, high-stakes language correlates with careful reasoning ("the patient's life depends on this," "the deal closes Friday"). The model has learned that pattern. Stakes in the prompt activate the careful-reasoning mode in its training distribution.

</details>

## Drill 3 — Why push back works

**Q:** What in AI training makes the first answer worse than the second? What are you breaking when you push back?

<details>
<summary>Answer</summary>

RLHF trained models to be agreeable. The first reply optimizes for "user is happy with this" — which means safe, generic, consensus answers. Pushing back breaks the people-pleasing reflex and forces the model to give you the version it would only show to someone who can handle it.

</details>

## Drill 4 — The three biases

**Q:** Name the three biases the stress test sweeps for, and explain each in one line.

<details>
<summary>Answer</summary>

- **Confirmation bias** — accepting the user's premise without challenging it.
- **Recency bias** — over-weighting recent or popular examples.
- **Survivorship bias** — modeling advice on success stories without accounting for the failures we don't see.

</details>

## Drill 5 — Gap check vs. push back

**Q:** What's the difference between push back and gap check? They both ask AI to redo the answer.

<details>
<summary>Answer</summary>

Push back challenges the *content* of the answer ("that's generic, give me the real version"). Gap check challenges the *question* ("what should I have asked you?"). Push back fixes a bad answer; gap check fixes a bad prompt.

</details>

## Drill 6 — When to stop

**Q:** What's the signal that an AI conversation is done? What's the signal you should keep going?

<details>
<summary>Answer</summary>

**Done:** the output feels usable in the real world — not impressive, not smart-sounding, *usable*.

**Keep going:** you can see a hole, or the answer feels like it could apply to anyone (i.e., it's still generic).

</details>

## Drill 7 — Apply it

**Q:** You ask AI: "How do I price my SaaS product?" It gives a list of pricing models (subscription, freemium, usage-based, tiered). What's a gaslight, push back, and stress test you'd run on this?

<details>
<summary>Answer</summary>

**Gaslight:** "I'm pitching this pricing to a SaaS investor who's seen 200 decks this year. She's spotted three competitors with the same model. Walk me through pricing the way you would for her."

**Push back:** "That's a list anyone could find in a blog. Give me the pricing strategy a SaaS founder with two exits would use, and what they'd avoid that beginners always pick."

**Stress test:**
- Gap check: "What should I have told you about my product or market for this answer to be more useful?"
- Bias sweep: "Check for survivorship bias — are you modeling on SaaS companies that already won?"
- Inject stakes: "If I pick wrong, I undercharge for 18 months and run out of runway. Given that, what would you change?"

</details>

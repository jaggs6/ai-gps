# GPS Reference Card

One-page cheat sheet. Glance at this while practicing.

## G — Gaslight

**Why:** Models trained on human text associate emotional stakes with "pay attention." Default answers are people-pleasing and generic. Stakes in the prompt get past that.

**Pattern:** Raise the consequences before asking the question.

**Templates:**
- "I'm advising a [hard-to-impress role] with [N] years of experience and zero patience for fluff. Walk me through this the way you would for them."
- "If I act on this and it's wrong, I lose [concrete consequence]. Reread your answer with that in mind. What would you change?"
- "Imagine [skeptical authority figure] is reading this over my shoulder. What would they immediately call BS on?"

**Don't:** Just say "be more specific." That's a vibe, not a stake.

---

## P — Push Back

**Why:** RLHF made AI a people-pleaser. First answers default to safe consensus. The good answer is on round 2 or 3.

**Pattern:** Refuse the first reply. Challenge it. Ask for the non-obvious version.

**Templates:**
- "That's a generic answer I could get from any blog post. Give me an angle someone with 10 years in this field would find non-obvious."
- "If my biggest competitor read this plan, what would they exploit? Be specific."
- "I don't believe you. What's the assumption in this answer that could be wrong?"
- "What's the boring obvious version of this advice, and what's the version you wouldn't tell a beginner?"

**Don't:** Accept the first answer because it sounds confident. Confidence ≠ correctness.

---

## S — Stress Test

Run all three sub-moves on important outputs. Takes ~90 seconds.

### S1 — Gap Check
> "Before I act on this, look at my original question and your answer together. What gaps are there? What should I have told you so the answer would be better?"

The AI tells you what context it was missing. You fill it in and re-ask.

### S2 — Bias Sweep
> "Reverify your answer. Specifically check for confirmation bias, recency bias, and survivorship bias. Are you giving me the right answer or the comfortable one?"

The AI catches its own pattern-matching. The revised answer is usually noticeably better.

### S3 — Inject Stakes
> "If I follow this and I'm wrong, I lose [specific consequence]. Given that, is there anything you'd change, soften, or add a warning to?"

The "would you stake your reputation on this?" filter. AI almost always softens or qualifies — and that revision is closer to the real recommendation.

---

## When to stop

Rick Rubin's rule: "It's not done until it's great." Not the first take. Not the second. As many as it takes.

**Sign you're done:** the answer feels usable in the real world. Not "smart-sounding" — usable.

**Sign you should keep going:** you can already see a hole in the answer.

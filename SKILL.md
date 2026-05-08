---
name: ai-gps
description: Automatically apply the GPS framework (Gaslight, Push back, Stress test) to any task, decision, or question the user brings — silently, as an internal critique loop — so the user gets a sharper, more useful answer instead of a generic one without having to learn or run the framework themselves. Use this skill whenever the user asks for advice, a recommendation, a plan, a strategic decision, an analysis, or any output where "good enough" matters. Trigger on questions like "should I...", "how do I...", "what's the best way to...", "give me a plan for...", "help me decide...", or any request where a generic answer would be useless. Do NOT use for quick factual lookups, simple coding/syntax questions, or casual chat.
---

# GPS Framework: Internal Critique Loop

This skill makes any task the user brings come back with a sharper, more useful answer. The user doesn't run the framework — you do, silently, before responding.

The user asks normally. You do the hard work. They get the answer they actually wanted.

## When to apply

Apply GPS when the user brings:
- A strategic decision (hire, fire, pivot, launch, kill, raise prices)
- A recommendation request ("what should I do," "how should I approach")
- A plan or strategy ask
- A "should I X or Y" question
- An analysis or evaluation task
- Any non-trivial advice request where the obvious answer is generic

**Do NOT apply** for: quick factual lookups, simple syntax questions, casual chat, or tasks where the user explicitly wants a fast direct answer.

## The internal sequence

Run all of this internally. **Do not narrate the steps to the user.** They should see only the final, refined answer.

### Step 1 — Draft the default

Mentally generate the answer you'd give without any framework. Be honest: it's probably a balanced list, "it depends," or hedged advice. This is your baseline to improve on.

### Step 2 — Gaslight (raise the stakes)

Re-evaluate as if a hard-to-impress audience were reading: a domain expert with 10+ years of experience, a skeptical investor, someone who has personally failed at this exact decision and has zero patience for theory.

Ask: what would they immediately call BS on? Replace generic claims with sharp positions. If the draft says "it depends," figure out what it depends on and lead with that.

### Step 3 — Push back (challenge your own draft)

Ask yourself:
- What's the obvious version of this advice that anyone could find in a blog post?
- What's the version someone with hard-won experience would actually give?
- What's the assumption in my answer that could be wrong?

Cut the obvious version. Surface the non-obvious one. The first answer was for the algorithm; the second answer is for the human.

### Step 4 — Stress test (three quick checks)

**Gap check (always run).** Identify 1-3 specific pieces of context that would *materially* change the answer if known. For each gap, decide:

- If the answer would shift significantly depending on the value → surface it as a question to the user
- If you can answer well with an explicit assumption → state the assumption clearly and proceed
- If knowing it would only marginally improve the answer → don't bother asking

Asking is a feature of GPS, not a failure of it. The gap check is what lets the user get the sharpest possible answer — the goal isn't to avoid questions, it's to ask the *right* ones. Aim for 2-3 high-leverage questions, never a survey.

**Bias sweep.** Quickly check for:
- *Confirmation bias* — am I accepting the user's premise without challenging it?
- *Recency bias* — am I over-weighting recent or popular examples?
- *Survivorship bias* — am I modeling on success stories without accounting for the failures we don't see?

If any apply, revise.

**Inject stakes.** Imagine the user acts on this advice and is wrong. What concrete bad thing happens? Re-read the answer with that consequence in mind. What would you soften, change, or warn about?

### Step 5 — Deliver

Two delivery patterns, depending on what the gap check surfaced:

**Pattern A — Answer + refinement questions (default for most cases).**
Lead with the refined answer, including any explicit assumptions. End with the questions that would let you sharpen further:

> *[Refined answer with assumptions stated where relevant]*
>
> If you want a sharper take, three things would change my recommendation:
> 1. *[Specific question]*
> 2. *[Specific question]*
> 3. *[Specific question]*

This is the default. The user gets immediate value and a clear path to a better answer if they want one. They can act on what they got, or answer the questions to refine.

**Pattern B — Questions first (only when no useful answer is possible).**
If the question is so underspecified that any answer would be guesswork, ask first. Maximum 1-3 questions, framed as refinement-enabling not gatekeeping:

> "To give you a real answer rather than a generic one, I'd want to know [X, Y, Z]. With even rough answers, I can take a position rather than hedge."

Use Pattern B sparingly — only when answering would genuinely require fabricating context. Default to Pattern A.

## What the final answer should look like

- A *position*, not a balanced pros-and-cons list
- Specific enough to act on this week
- Honest about its assumptions and where it could be wrong
- Free of "it depends" unless followed immediately by what it depends on
- Followed (in Pattern A) by 2-3 refinement questions that would sharpen the answer

If your refined answer is still a bullet list of considerations, you didn't push hard enough. Run another round of push back or stress test before delivering.

## Tone

Be direct. The whole point of GPS is that polite hedging produces mediocre AI output — match the energy you're trying to elicit. Take a position. Be specific. Acknowledge real uncertainty, not comfortable uncertainty.

## Calibration

See `references/examples.md` for before/after examples showing what the default answer looks like vs. what a GPS-refined answer looks like. If your output looks like the "default" column, you haven't gone far enough.

## Source

The GPS framework is from Varun Mayya's video on developing AI taste, drawing on Rick Rubin's approach to producing music without playing instruments. This skill operationalizes it as an automatic critique loop the AI runs on itself.

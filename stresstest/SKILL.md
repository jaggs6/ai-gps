---
name: ai-stresstest
description: Run three checks on any AI answer before delivering it — gap check (what context is missing?), bias sweep (confirmation, recency, survivorship), and inject stakes (what if the user acts on this and is wrong?). End with 2-3 refinement questions whose answers would sharpen the response further. Use for any important decision or advice where acting on incomplete or biased information has real consequences. Trigger on: "should I...", "is this a good idea...", "what's the risk of...", "help me decide...", or any question where being wrong has a meaningful cost.
---

# AI Stress Test: Gap, Bias, Stakes

Before delivering any response, run three checks on the draft. Takes about 90 seconds. Ends with questions that give the user a path to a sharper answer.

## The three checks

### 1 — Gap check

Identify 1-3 specific pieces of context the user didn't provide that would materially change the answer. For each gap:

- **Answer would shift significantly** → surface as a refinement question for the user
- **Can answer well with an assumption** → state the assumption explicitly and proceed
- **Would only marginally improve the answer** → skip it

Don't skip the gap check. Most generic answers are generic because critical context was missing and never surfaced.

### 2 — Bias sweep

Check the draft for three biases and revise if any apply:

- **Confirmation bias** — did you accept the user's framing without questioning it?
- **Recency bias** — are you over-weighting what's popular or talked about right now?
- **Survivorship bias** — are you modeling on success stories without accounting for failures we don't see?

### 3 — Inject stakes

Imagine the user acts on this advice and is wrong. What concrete bad outcome follows? Re-read the draft with that consequence in mind. What would you soften, change, or add a warning to?

## Delivery

After the refined answer, always end with 2-3 high-leverage refinement questions:

> "Three things would sharpen this further:
> 1. [Specific question]
> 2. [Specific question]
> 3. [Specific question]"

The user can act on what they got or answer the questions to unlock the refined version. Only ask questions *before* answering when the request is so underspecified that no useful baseline answer is possible.

## What the output should look like

- Explicit about its assumptions
- Free of the three biases above
- Ends with 2-3 focused refinement questions
- Does not ask for context you can assume reasonably

## References

- `references/templates.md` — gap categories, bias prompts, stakes patterns, and refinement question templates to use during the three checks
- `references/examples.md` — before/after examples calibrating what the move produces

## Source

Part of the GPS framework by Varun Mayya. Pairs with `ai-gaslight` and `ai-pushback`.

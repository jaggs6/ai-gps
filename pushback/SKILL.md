---
name: ai-pushback
description: Challenge the AI's own draft answer before the user sees it. Surface the non-obvious version of any advice by asking what a seasoned expert would say that a blog post wouldn't. Use whenever the user asks for strategy, recommendations, or analysis where the consensus answer isn't the useful one. Trigger on: "how do I grow...", "what's my best approach to...", "give me a strategy for...", "what should I do about...", or any request where the obvious answer is too safe.
---

# AI Pushback: Challenge Your Own Answer

Before delivering any response, challenge the draft the same way an experienced editor would challenge a junior writer's first take.

## What to do

Ask yourself three questions about the draft:

**1. What's the obvious version of this advice?**
The thing anyone could find in a blog post, Reddit thread, or business book. If the draft looks like that, it's not done yet.

**2. What's the version someone with hard-won experience would give?**
Someone who's tried the obvious approach, seen it fail, and learned what actually works. What would they say that a beginner wouldn't know to say?

**3. What assumption in this answer could be wrong?**
Not a hedge — a real assumption that, if false, changes the recommendation entirely. Name it explicitly.

Cut the obvious version. Surface the non-obvious one. If you can't find a non-obvious version, push harder — it's almost always there.

## What the output should look like

- Contains at least one insight the user wouldn't get from a basic search
- Names the failure mode that the obvious advice carries
- Still gives a concrete recommendation — non-obvious doesn't mean vague

## References

- `references/templates.md` — challenge questions, "obvious" vs "non-obvious" patterns, and self-prompts to use during the pushback move
- `references/examples.md` — before/after examples calibrating what the move produces

## Source

Part of the GPS framework by Varun Mayya. Pairs with `ai-gaslight` and `ai-stresstest`.

# Porting Guide

How to use these skills across different AI tools. The skills work everywhere — adaptation is mostly about how you install them.

## Claude (Web, Desktop, Mobile, Code)

Native skill support. Drop the `gaslight/`, `pushback/`, and `stresstest/` folders into your skills directory per the [skill installation docs](https://docs.claude.com/). All three load and trigger automatically based on the question.

**Notes:** Claude already pushes back on its own more than other models, so the `pushback` skill compounds with that rather than replacing it. The full GPS treatment lands cleanly here — start here if you can.

---

## ChatGPT

No native SKILL.md support. Paste each `SKILL.md` into Custom Instructions or a Custom GPT system prompt.

**To stack all three:** Open Custom Instructions → "How would you like ChatGPT to respond?" → paste skill contents in sequence with separators:

```
[Skill 1: ai-gaslight]
<paste gaslight/SKILL.md content>

[Skill 2: ai-pushback]
<paste pushback/SKILL.md content>

[Skill 3: ai-stresstest]
<paste stresstest/SKILL.md content>
```

**Notes:** ChatGPT is the most agreeable by default, so `gaslight` matters most here — it's where the gap vs. baseline output is largest.

---

## Gemini

System Instructions field. Same approach as ChatGPT — paste each `SKILL.md` content into the system instructions, separated by clear markers.

**Notes:** Gemini is inconsistent across versions. If a response feels like it skipped GPS, regenerate; the second attempt usually applies the framework correctly.

---

## Copilot Chat / Cursor / Claude Code (chat mode)

Coding tools with chat sidebars. Paste each `SKILL.md` into the tool's system prompt or rules file (`.cursorrules` for Cursor, custom instructions for Copilot, etc.).

**Adapt the templates for code:** The internal templates assume general business questions. For coding contexts, swap the archetypes — instead of "CEO with two exits," think "staff engineer who's debugged this in three codebases." Stakes become "if this ships and breaks production at 3am, who's debugging it?"

**Most useful single skill for coding:** `stresstest`. The gap check is especially valuable when the AI doesn't know your codebase — the refinement questions surface exactly what context you should have provided.

---

## Inline autocomplete (Copilot in IDE, etc.)

GPS partially breaks here — there's no real conversation, just one-shot completions. Use the chat sidebar version of the same tool for any decision worth applying GPS to. Reserve inline autocomplete for typing-speed tasks where your own taste already lives in code review.

---

## Image / video generation tools (Midjourney, Sora, Veo)

GPS adapts but the moves change shape:

- **Gaslight equivalent:** Stakes-laden description ("the kind of image a senior creative director would approve for a Vogue cover")
- **Pushback equivalent:** Regenerate, change one variable, regenerate — three rounds minimum
- **Stress test equivalent:** Imagine three skeptical viewers and name what each would call wrong before generating again

---

## Tools with very small context windows

If the model can't hold all three skills in context, prioritise based on the user's question type:

- Decision questions → install `stresstest` (gap check is the highest-leverage move)
- Strategy / advice questions → install `gaslight` (positioning matters most)
- "How do I grow X" type questions → install `pushback` (non-obvious version is the value)

---

## Universal rule

If the tool exposes a system prompt or custom instructions field, GPS works. If it doesn't, paste skill contents into the message itself as a preamble — it works but adds friction every turn.

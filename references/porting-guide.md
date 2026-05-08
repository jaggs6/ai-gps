# Porting GPS to Different AI Tools

GPS works across every major AI tool — the underlying mechanics (training on human text, RLHF for agreement) are universal. But the surface-level adaptation varies. Here's how to apply it tool by tool.

## Conversational AI (Claude, ChatGPT, Gemini)

**Status:** Full GPS works exactly as described. The video's examples land most cleanly here.

**Notes:**
- **Claude** tends to push back on its own more than other models, so the gaslight step is sometimes less necessary. Push back and stress test still earn their keep.
- **ChatGPT** is the most agreeable by default — gaslight matters most here.
- **Gemini** can be inconsistent across versions; rerun GPS if the first try gives a weak result.

---

## Coding assistants — chat mode (Copilot Chat, Codex, Cursor, Claude Code)

**Status:** GPS works, but you adapt the *content*, not the technique.

**Adapted templates:**

- **Gaslight:** "If this code ships and breaks production at 3am, I'm the one debugging it. Reread your suggestion with that in mind."
- **Push back:** "You gave me the obvious fix. What's the architectural smell you're ignoring?" or "A senior engineer reviewing this would call out something. What is it?"
- **Gap check:** "What about my codebase or constraints would have made this answer better?"
- **Bias sweep:** "Are you defaulting to the most popular pattern, or the right one for this case?"
- **Inject stakes:** "If we adopt this and it doesn't fit, we're refactoring in 3 months. Worth it?"

---

## Coding assistants — inline autocomplete (Copilot in IDE)

**Status:** GPS partially breaks. There's no real conversation — you get one shot per autocomplete.

**Workaround:** Use the chat sidebar of the same tool for important decisions (architecture, refactoring, debugging). Reserve inline autocomplete for the typing-speed tasks where taste already lives in your code review.

---

## Image / video generation tools (Midjourney, Sora, Veo, etc.)

**Status:** GPS adapts but works differently. There's no "push back" in a single generation.

**Adapted approach:**
- Gaslight equivalent: precise stakes-laden description ("the kind of image a senior creative director would approve for a Vogue cover")
- Push back equivalent: regenerate, change one variable, regenerate
- Stress test equivalent: imagine three skeptical viewers and ask what each would call wrong

---

## Models with very small context windows or short responses

**Status:** Stress test gets harder because each move adds context. If the model can't hold the conversation, GPS partially breaks.

**Workaround:** Run G, P, and S as separate fresh conversations, manually copying the previous answer into the next prompt as context.

---

## Universal rule

If a tool lets you have a multi-turn conversation, GPS works. If it doesn't, use the closest equivalent (regenerate, edit, expand the prompt) — but expect 60-70% of the value, not 100%.

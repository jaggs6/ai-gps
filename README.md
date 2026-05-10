# ai-gps

An open-source skill that automatically applies Gaslight, Push back, Stress test to any question — so you get your AI's best answer, not its default one.

Three focused skills that each do one move. Use them individually or install all three to get the full GPS treatment automatically.

---

## The three skills

### `gaslight/`
Re-evaluates any draft answer as if a hard-to-impress domain expert is reading it. Replaces balanced lists and hedged claims with sharp positions.

> **Trigger:** Any advice, recommendation, or decision question.

### `pushback/`
Challenges the AI's own first answer. Surfaces the non-obvious version of any advice — the thing someone with hard-won experience would say that a blog post wouldn't.

> **Trigger:** Strategy, growth, and analysis questions where the obvious answer isn't useful.

### `stresstest/`
Runs three checks before delivering — gap check (what context is missing?), bias sweep (confirmation, recency, survivorship), and inject stakes (what if the user acts on this and is wrong?). Ends with 2-3 refinement questions.

> **Trigger:** Important decisions where being wrong has a real cost.

---

## Installation

### As Claude Skills

Clone the repo and load one or all three skills per the [skill installation docs](https://docs.claude.com/):

```bash
git clone https://github.com/jaggs6/ai-gps.git
```

Install all three for full GPS coverage, or pick the one that fits your use case.

### Other AI tools

If your tool doesn't natively support SKILL.md, paste the contents of any skill's `SKILL.md` into the tool's custom instructions or system prompt. Works on:

- Claude (web, desktop, mobile, Code)
- ChatGPT (Custom Instructions)
- Gemini (System Instructions)
- Copilot Chat / Cursor (system prompt)
- Any AI tool with a system prompt field

See [`porting-guide.md`](porting-guide.md) for tool-specific installation steps and adaptation notes.

---

## How they compose

When all three are installed, they layer on every answer:

1. **Gaslight** — replaces generic claims with a sharp position
2. **Push back** — finds what's still obvious and surfaces the expert version
3. **Stress test** — catches gaps, biases, and stakes — and asks the right questions

The user asks normally. All three run silently. The final answer is what GPS produces.

---

## Repo structure

```
ai-gps/
├── README.md
├── LICENSE
├── porting-guide.md
├── gaslight/
│   ├── SKILL.md
│   └── references/
│       ├── templates.md
│       └── examples.md
├── pushback/
│   ├── SKILL.md
│   └── references/
│       ├── templates.md
│       └── examples.md
└── stresstest/
    ├── SKILL.md
    └── references/
        ├── templates.md
        └── examples.md
```

---

## FAQ

**Do I need to learn the GPS framework to use this?**
No. The skills run GPS on the AI's own answers before you see them. You just ask normally.

**Can I install just one skill?**
Yes. Each skill is self-contained and adds value on its own. Install all three for the full effect.

**Does this work on any AI tool?**
Yes — natively in any tool that supports SKILL.md, and via system prompt or custom instructions everywhere else.

**What if the AI asks me questions instead of answering?**
That's the stress test's gap check working. By default you get an answer plus 2-3 refinement questions at the end — you can act on what you got or answer them to get a sharper response. The AI asks before answering only when the question is too underspecified to give any useful response.

---

## Source

The GPS framework comes from Varun Mayya's video on developing AI taste, drawing on Rick Rubin's approach to producing music without playing instruments.

## License

MIT — see [LICENSE](LICENSE).

## Contributing

PRs welcome. Especially:
- More calibration examples in each skill's `references/examples.md`
- Improvements to trigger descriptions for more reliable activation
- Real-world case studies showing GPS in action

Open an issue first for anything substantial.

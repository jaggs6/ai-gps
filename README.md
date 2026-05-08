# ai-gps

An open-source skill that automatically applies Gaslight, Push back, Stress test to any question — so you get your AI's best answer, not its default one.

## What it does

Most AI answers are generic — balanced lists, "it depends," safe consensus. GPS is the technique power users run manually to get past that. This skill installs it as an internal critique loop: the AI runs the framework on its *own* answer before showing it to you, and delivers only the refined version.

You ask normally. The AI does the hard work silently. You get the answer you actually wanted.

## What you'll notice

- Answers are *positions*, not pros-and-cons lists
- Recommendations include a concrete next step you could take this week
- Most answers come with 2-3 follow-up questions you can answer to get a sharper response — refining is optional, not required
- The AI surfaces its own assumptions so you know where to push back
- The AI only asks questions *before* answering when the request is too underspecified to give any useful response

## What "GPS" stands for

You don't need to know any of this to use the skill, but for the curious:

- **G — Gaslight:** The AI re-evaluates its draft answer as if a hard-to-impress expert were reading it.
- **P — Push back:** The AI challenges its own first answer and surfaces the non-obvious version.
- **S — Stress test:** Three internal checks — gap check (what context is missing?), bias sweep (confirmation, recency, survivorship), inject stakes (what if the user acts on this and is wrong?).

All of it runs internally. The user just sees a better answer.

## Installation

### As a Claude Skill

Clone and load into Claude or Claude Code per the [skill installation docs](https://docs.claude.com/):

```bash
git clone https://github.com/jaggs6/ai-gps.git
```

Then ask Claude any task or decision question normally. The skill triggers automatically.

### Other AI tools

If your AI tool doesn't natively support the SKILL.md format, copy the contents of `SKILL.md` into the tool's custom instructions or system prompt. Works on:

- Claude (web, desktop, mobile, Code)
- ChatGPT (Custom Instructions)
- Gemini (System Instructions)
- Copilot Chat / Cursor (system prompt)
- Any AI tool that exposes a system prompt or custom instructions field

## When the skill triggers

Activates when you bring:
- A strategic decision ("should I hire?", "should I pivot?")
- A recommendation request ("what's the best way to...?")
- A plan or strategy ("give me a plan for...")
- An analysis or evaluation task
- Any "should I X or Y" question

Stays out of the way for quick factual lookups, simple syntax questions, or casual chat — where a generic answer is the right answer.

## FAQ

**Do I need to be a prompt expert to use this?**
No. The skill does GPS for you. You just ask normally.

**Does this work on any AI tool?**
Yes — natively in any tool that supports SKILL.md, and via system prompts elsewhere.

**Will this slow down my answers?**
Slightly. The AI does extra internal work before responding. The trade is a few seconds for a noticeably better answer.

**Can a beginner use this?**
Yes. If you've ever used AI and felt the answer was too generic, this skill is exactly what you need.

**What if the AI asks me a question instead of just answering?**
That's the gap check working — it's a feature, not a bug. By default, you'll get an answer *plus* 2-3 follow-up questions whose answers would let the AI give you a sharper response. You can ignore them and act on what you got, or answer to get the refined version. The AI only asks *before* answering when the question is too underspecified to give any useful response without more context.

## Repo structure

```
ai-gps/
├── README.md                 (you are here)
├── LICENSE
├── SKILL.md                  (the skill — entry point)
└── references/
    └── examples.md           (before/after calibration examples)
```

## Source

The GPS framework comes from Varun Mayya's video on developing AI taste, drawing on Rick Rubin's approach to producing music without playing instruments. This skill operationalizes the framework as an automatic internal critique loop.

## License

MIT — see [LICENSE](LICENSE).

## Contributing

PRs welcome. Especially valuable:

- Additional calibration examples in `references/examples.md` for different domains (legal, medical, creative, scientific, operational)
- Improvements to the trigger description so the skill activates reliably across more AI tools
- Real-world case studies of where GPS produced a better outcome than default

Open an issue first for anything substantial so we can align on direction.

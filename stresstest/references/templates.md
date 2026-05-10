# Stress Test — Internal Templates

Use these as internal prompts when executing the three checks and crafting refinement questions.

## Gap check templates

### Common gap categories by question type

| Question type | Gaps to check |
|---------------|---------------|
| "Should I hire X?" | Team size, current bottleneck, growth stage, alternatives considered |
| "Should I raise prices?" | Current churn, competitive position, contract terms, customer mix |
| "Should I quit my job?" | Runway, idea validation stage, family situation, what specifically the new thing is |
| "How do I grow X?" | Current scale, what's been tried, success criteria, time horizon |
| "Should I learn X?" | Current skills, why now, opportunity cost, how it'll be used |
| "Should I rewrite X?" | Team size, specific pain points, constraints, deadline |
| Coding / architecture | Codebase scale, team experience, deployment frequency, performance constraints |
| Career / promotion | Current level, company stage, alternatives, timeline |
| Pricing / packaging | Customer segments, churn rate, sales motion, competitors |

### Gap check self-prompts

1. "If I had to give this exact advice to two different people in this user's situation, what would have to be true about each for the advice to differ?"
2. "What's the one fact, if I knew it, that would flip my recommendation?"
3. "What did the user tell me that I'm taking at face value but probably shouldn't?"

## Bias sweep templates

### Confirmation bias prompts
- "Did the user frame this question in a way that already implies an answer? Am I going along with that framing?"
- "If the user had asked the *opposite* question — 'why shouldn't I do this?' — what would I have said?"

### Recency bias prompts
- "Is this advice rooted in something specific to this year, or is it durable?"
- "Am I citing examples from the last 12 months because they're representative, or because they're top-of-mind?"

### Survivorship bias prompts
- "Is my advice based on what worked for visible winners, or also on what failed for invisible losers?"
- "If I'm citing a success story, is the success generalisable, or specific to circumstances the user doesn't have?"

### Other biases worth a quick check (less common, high-impact when they apply)

- **Availability bias:** Am I recommending the path I have the most examples of, rather than the best one?
- **Authority bias:** Am I citing what well-known people say without verifying the underlying claim?
- **Optimism bias:** Am I assuming the best-case scenario for execution risk?
- **Status quo bias:** Am I implicitly recommending what the user is already doing?

## Inject stakes templates

### Stake patterns by question type

| Question type | Concrete stakes to model |
|---------------|--------------------------|
| Career change | Months of income, relationship strain, momentum loss |
| Hiring | Annual cost, 3-6 months wasted before realising the hire is wrong, team morale |
| Pricing | Account churn, contract renegotiation, brand damage |
| Architecture rewrite | 6-12 months of feature velocity, team burnout, possible quits |
| Investment | Capital loss, opportunity cost, retirement timeline |
| Strategic pivot | Months of momentum, team cohesion, runway |

### Inject stakes self-prompts

1. "If the user follows this and it doesn't work, what's the worst concrete consequence in 6 months?"
2. "Is there anything in my answer I should soften because the cost of being too aggressive is high?"
3. "Is there anything I should warn about that I'd otherwise let slide?"

## Refinement question templates

The 2-3 questions you append should be high-leverage — answers should materially shift the recommendation.

### Patterns of high-leverage questions

- **The "what's actually broken" question:** Pin down a vague pain point ("when you say 'slow,' do you mean response time, deploy time, or feature velocity?")
- **The "scale anchor" question:** Pin down magnitudes ("how many users?" "what's revenue?" "team size?")
- **The "what's been tried" question:** Surface failed approaches ("have you tried X? what happened?")
- **The "constraint" question:** Name what can't change ("is the deadline real?" "is the budget fixed?")
- **The "alternative" question:** Test whether the framing is right ("are you also considering X?")

### Anti-patterns (don't ask these)

- Vague big-picture questions ("what are your goals?")
- Questions whose answer doesn't change the recommendation
- Questions you could answer yourself with a reasonable assumption
- More than 3 questions (becomes a survey)
- Questions that gatekeep the answer instead of refining it

# Section 3 — Prompt Engineering Fundamentals
*15 minutes*

---

## Slide: What Is a Prompt?

**Everything you put in front of the AI before it responds.**

That's it. No magic. No code.

The prompt is your order to your staff officer.
A vague order produces a vague product.

---

## Slide: The Anatomy of a Good Prompt

| Element | What It Does | Example |
|---------|-------------|---------|
| **Role** | Who should it be? | "You are an Army S1..." |
| **Task** | What specifically do you need? | "Draft an award citation..." |
| **Context** | What does it need to know? | "The Soldier is a SSG who..." |
| **Format** | How should the answer look? | "Use DA 638 citation format..." |

---

## Slide: Side by Side — Award Citation

**Weak prompt:**
```
Write me an award citation for a staff sergeant.
```

**Strong prompt:**
```
You are an Army awards officer. Draft an Army
Commendation Medal citation for a staff sergeant
who led a 12-person logistics section through a
90-day deployment, reduced supply errors by 40%,
and personally resolved a critical Class IX shortage
that kept three vehicles mission capable. Use
third-person past tense. Keep it under 100 words.
Format it for DA Form 638.
```

*(See examples/bad_vs_good_prompts.md for full side-by-side library)*

---

## Slide: What Changes?

Same AI. Same request.

The strong prompt gives the AI:
- A **role** (awards officer)
- A **specific task** (ARCOM citation, not generic)
- **Context** (rank, time period, specific actions)
- **Format** (third person, past tense, word count, form)

The AI doesn't have to guess any of it.

---

## Slide: Common Mistakes

| Mistake | Fix |
|---------|-----|
| Too vague: "Write a brief" | Specify: decision brief, for whom, on what topic |
| No format: AI invents one | State format explicitly: bullet points, BLUF first, etc. |
| No role: AI writes generically | Assign a role: "You are an Army S3..." |
| Too much at once | One task per prompt; follow up for more |
| Accepting the first output | Iterate: "Make it shorter." "Be more direct." "Add a BLUF." |

---

## Slide: Iteration Is Normal

You don't accept the first draft from your staff.
You shouldn't accept the first output from AI either.

**Common follow-ups:**
- "That's too long. Cut it to five bullets."
- "Add a BLUF at the top."
- "Rewrite the recommendation to be more direct."
- "This doesn't match our format — here's what we use: [paste format]"

---

## Slide: Exercise 01

**Try it on your phone right now.**

Pick a real task you're working on — or use this one:

> *"Help me write a BLUF for a memo recommending
> that our unit adopt a new PT schedule."*

Type it however you naturally would.
We'll compare results in 90 seconds.

*(See exercises/01_prompt_fundamentals.md)*

---

## Slide: What We Just Learned

**Prompt engineering is how you ask.**

- Assign a role
- Be specific about the task
- Provide relevant context
- Specify the format
- Iterate — don't accept the first draft

**Next:** What you *bring* to the conversation matters as much as how you ask.

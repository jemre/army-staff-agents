# Quick Reference — Prompt & Context Engineering
*Prompt & Context Engineering: Turning AI into Your Most Reliable Staff Officer*

---

## The Mental Model

> **Brief it like you'd brief a new staff officer.**
> AI knows doctrine. It doesn't know your unit, your mission, or your format — until you tell it.

---

## Anatomy of a Good Prompt

| Element | Question to Ask Yourself | Example |
|---------|-------------------------|---------|
| **Role** | Who should it be? | "You are an Army S3..." |
| **Task** | What specifically do I need? | "Write a risk assessment for..." |
| **Context** | What does it need to know? | "The unit has 2 of 4 medics available..." |
| **Format** | How should the answer look? | "BLUF first, then five bullets, under 200 words" |

---

## Common Staff Tasks — Starter Prompts

**Award Citation**
```
You are an Army awards NCO. Write an [ARCOM/AAM/MSM] citation for
[rank] who [specific actions, dates, outcomes]. Third-person past tense.
Under 100 words. DA Form 638 format. No filler phrases.
```

**BLUF Memo**
```
You are a [role] writing a memo for [audience]. Write a memo
recommending [topic]. BLUF at top (one sentence). Three bullets of
background. One-sentence recommendation. Under 200 words.
```

**Risk Assessment**
```
You are an Army S3. Build a risk assessment for [event]. Known issues:
[list]. For each hazard: Probability | Severity | Initial Risk |
Controls | Residual Risk | Approval Authority. Flag any go/no-go gates.
End with a BLUF recommendation.
```

**Talking Points**
```
You are a battalion XO. Write [#] talking points for the commander
on [topic]. Each point: one sentence, plain language, ends with
a specific expectation. Commander priorities: [list].
```

**Training Schedule Entry**
```
Write a training schedule entry for [event]. Fields: Task (Army task
number and title) | Conditions | Standard | Date/Time | Location |
OIC | NCOIC | Uniform | Equipment.
```

---

## Context Engineering — What to Inject

| What You're Working On | Context to Add |
|----------------------|----------------|
| Risk assessment | Event details, known hazards, personnel status, format |
| Award citation | Soldier's rank, role, specific actions, outcomes, dates |
| Memo or brief | Audience, commander's priorities, format requirements |
| Training plan | Unit strengths/gaps, available time, resources, standards |
| Staff estimate | Mission statement, relevant facts, constraints |

---

## Iteration — When the First Draft Isn't Right

| Problem | What to Say |
|---------|-------------|
| Too long | "Cut this to [#] bullets / [#] words." |
| Too vague | "Be more specific about [element]." |
| Wrong format | "Reformat using [format]. Here's the template: [paste]" |
| Needs BLUF | "Add a BLUF at the top: one sentence, bottom line first." |
| Too generic | "This is too generic. Add specifics from [context I gave you]." |
| Tone wrong | "Rewrite this to sound more direct / formal / conversational." |

---

## OPSEC Rules

- No classified information in commercial AI tools
- Use generic unit designations (not actual unit names in sensitive contexts)
- No personnel names in sensitive situations
- Treat it like an unclassified system — if you wouldn't email it publicly, don't paste it in

---

## Persistent Context (Claude Projects)

1. Create a Project in Claude
2. Add standing instructions: your role, unit type, format preferences, commander priorities
3. Every conversation in that project starts with your context pre-loaded

*Equivalent to a staff officer who already knows your SOPs.*

---

## The Three Things to Remember

1. **Brief it** — role, task, context, format
2. **Iterate** — the first draft is a first draft
3. **Own it** — you review, you sign, you're responsible

---

*Iowa National Guard Professional Development*

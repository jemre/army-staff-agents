# Section 4 — Context Engineering: The Next Level
*15 minutes*

---

## Slide: Prompt vs. Context

| | Prompt Engineering | Context Engineering |
|--|-------------------|---------------------|
| **What it is** | How you ask | What you bring |
| **Analogy** | Writing a clear order | Briefing your staff officer |
| **Impact** | Better questions | Better advisor |
| **Skill level** | Foundational | Next level |

You need both. But context engineering is where the real leverage is.

---

## Slide: What Is Context?

**Context is everything the AI knows before it answers.**

Three sources:
1. **System prompt** — Standing instructions; who it is and how it behaves
2. **Injected documents** — SOPs, regulations, mission details, formats you paste in
3. **Conversation history** — What's already been established in the session

Most people skip all three and then wonder why the output is generic.

---

## Slide: The Brief Analogy

**Without context:**
> "Write me a risk assessment."

AI produces a generic template from doctrine.
You spend 20 minutes reformatting it.

**With context:**
> *[Paste: your unit's risk assessment format, the training event details, weather data, medical coverage status]*
> "Now write the risk assessment."

AI produces your format, your thresholds, your situation.
You spend 5 minutes reviewing it.

---

## Slide: Live Demo — Context Injection

*(Instructor: run this live — see examples/context_injection_demo.md)*

**Round 1:** Ask for a training event risk assessment with no context.

**Round 2:** Paste in the scenario details and ask again.

**What changed?**

---

## Slide: What Makes Good Context?

| Quality | What It Means |
|---------|---------------|
| **Relevant** | Only what the AI needs for this task — don't dump everything |
| **Structured** | Organized information is easier to use than a wall of text |
| **Current** | Don't inject outdated SOPs or superseded orders |
| **Concise** | More isn't always better — irrelevant context dilutes the good stuff |

**Rule of thumb:** Brief your AI staff officer the same way you'd brief a smart new officer who's read the doctrine but doesn't know your unit.

---

## Slide: Persistent Context — Projects & Memory

**The problem with starting fresh every time:**
Every new chat, the AI forgets everything.
You have to re-brief it every session.

**The solution — persistent context:**
- **Claude Projects:** Create a project, add standing instructions and documents. Every conversation in that project starts pre-briefed.
- **Custom instructions:** Set default behavior across all conversations.
- **Saved prompts:** Keep your best prompts in a doc and paste when needed.

**Analogy:** The difference between a new officer every day and a staff officer who's been with the unit for six months.

---

## Slide: OPSEC Reminder

**Do not put classified information into commercial AI.**

Treat AI like any unclassified system:
- No unit-specific sensitive data
- No personnel names in sensitive contexts
- No information you wouldn't put in an unclassified email

**The examples in this class are generic for exactly this reason.**

When in doubt: use fictional unit names, generic scenarios, and placeholder data.

---

## Slide: Exercise 02

**Add context to what you tried before.**

Go back to your previous prompt. Before asking the question, add:
1. One sentence about who the output is for
2. The format you need
3. One key fact about the situation

**Example:**
> "This memo is for my battalion commander. Format it with a BLUF, three bullet points of background, and a clear recommendation. The situation is [your situation]."

Then ask your question. See what changes.

*(See exercises/02_context_engineering.md)*

---

## Slide: What We Just Learned

**Context engineering is how you brief.**

- The system prompt sets who the AI is
- Injected documents give it your formats and specifics
- Persistent context means you don't re-brief every time
- Good context: relevant, structured, current, concise
- OPSEC: treat it like an unclassified system

**The combined skill:** Brief your AI like a competent staff officer who reads fast, never sleeps, and needs you to provide the context it can't get on its own.

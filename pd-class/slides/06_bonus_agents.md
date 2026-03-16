# Section 6 — Bonus: Agents & Advanced Applications
*Up to 30 minutes — only if time allows and room is engaged*

---

## Slide: The Next Level

Everything so far: **one person, one AI, one conversation.**

The next level: **AI that coordinates with other AI.**

That's what agents are.

---

## Slide: What Is an Agent?

An agent is an AI with:
- A defined **role** and **expertise** (its system prompt)
- The ability to **use tools** (search, write files, call other agents)
- **Persistent context** (it knows its job before you ask)

**Think of it as:** a staff officer who's already been briefed, is always available, and can call the other sections on your behalf.

---

## Slide: The Staff Agent Concept

*(Transition to live demo if proceeding)*

**What if you had an XO agent that could:**
- Receive your commander's intent
- Decompose it into staff tasks
- Call on S2, S3, S4 agents to contribute
- Synthesize their inputs into a finished staff product

That's not a hypothetical. Let me show you.

---

## Slide: Live Demo — XO Agent

*(Instructor: open Claude Code in army-staff-agents directory)*

```
/xo
```

*Paste scenario input from scenarios/01_training_risk_assessment/input.md*

**What to point out:**
- XO receives and restates the task
- XO identifies which sections need to contribute
- XO flags the medical shortfall before delegating
- S3 and S4 each contribute from their lane
- XO integrates into a finished product

---

## Slide: How This Is Built

Three components:

| Component | What It Is | Army Analogy |
|-----------|-----------|--------------|
| **System prompt** | The agent's role, responsibilities, and standards | The officer's branch, experience, and SOPs |
| **Context injection** | Unit, mission, and SOP documents loaded at session start | The pre-mission brief |
| **Skills / Tools** | Ability to call other agents or external systems | The ability to pick up the phone to the other sections |

---

## Slide: Other Tools Worth Knowing

**Google NotebookLM**
- Upload documents (regulations, manuals, AARs)
- Ask questions across all of them at once
- Generate summaries, mind maps, and audio overviews ("podcast" mode)
- Good for: research, regulation lookup, after-action synthesis

**Claude Projects**
- Persistent context across sessions
- Good for: building a "unit assistant" that already knows your SOPs

**Obsidian + AI**
- Local note-taking with AI integration
- Good for: officers who want AI assistance without cloud storage concerns

---

## Slide: Open Source and Risk

**Not all AI tools are the same.**

Commercial tools (Claude, ChatGPT, Gemini):
- Well-resourced safety and security teams
- Clear terms of service
- No training on your inputs (check the settings)

Open source / unvetted tools:
- No guarantee of data handling
- Potentially running on adversary infrastructure
- **Do not use for anything sensitive**

**Rule:** If you wouldn't put it on a public forum, don't put it in an unvetted AI tool.

---

## Slide: Agent to Agent (A2A)

**The emerging standard for multi-agent systems.**

Agents can be designed to:
- Call other agents as needed (XO calls S3)
- Pass context between sessions
- Build products collaboratively without human in the loop for each step

**Where this is going:** Staff sections that produce inputs automatically when the XO asks, with a human reviewing the final integrated product.

**Current state:** Available now with tools like Claude Code. Requires setup and prompt engineering — exactly what you learned today.

---

## Slide: The Bottom Line on Agents

Agents are prompt and context engineering at scale.

Everything you learned today applies.
The difference is:
- The prompts are pre-built and persistent
- The coordination happens automatically
- The human stays in the review-and-decision seat

You don't have to build this today.
But understanding how it works puts you ahead of the curve.

---

## Slide: Final Thought

> "The units and officers who figure this out early
> are going to have a significant advantage.
> You don't have to be a tech expert.
> You just have to know how to brief."

Thank you.

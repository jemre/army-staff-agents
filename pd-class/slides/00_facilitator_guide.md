# Facilitator Guide
## Prompt & Context Engineering: Turning AI into Your Most Reliable Staff Officer

**Audience:** Iowa National Guard Army and Air Force Officers, junior through senior
**Duration:** 55 min core + up to 30 min bonus if time allows
**Format:** Conversational, instructor-led. Students likely have phones. No laptops expected.
**Demo platform:** Claude.ai (browser) or phone app. Have it open and logged in before the class starts.

---

## Before You Start

- Open Claude.ai on your demo device and test your examples in advance — model responses vary
- Have `examples/bad_vs_good_prompts.md` and `examples/context_injection_demo.md` open for reference
- Identify 1–2 participants early who seem engaged — call on them for the exercises
- The exercises are phone-friendly: participants can follow along on their own devices if they want, but it's not required
- Know your room: if the audience skews senior, lean on the leadership/decision-making angle; if junior, lean on the "make your job easier" angle

---

## Section Timing

| # | Section | Time | Cumulative |
|---|---------|------|-----------|
| 1 | Welcome & Why This Matters | 5 min | 0:05 |
| 2 | Core Mental Model | 5 min | 0:10 |
| 3 | Prompt Engineering Fundamentals | 15 min | 0:25 |
| — | Exercise 01 (phone) | built into section 3 | — |
| 4 | Context Engineering | 15 min | 0:40 |
| — | Exercise 02 (phone) | built into section 4 | — |
| 5 | Wrapping Up | 5 min | 0:45 |
| 6 | Q&A | 10 min | 0:55 |
| — | Bonus: Agents & Applications | up to 30 min | if time |

---

## Section 1: Welcome & Why This Matters (5 min)

**Goal:** Get them leaning in. Make it feel relevant before you say anything technical.

**Opening hook (pick one based on your read of the room):**

*Option A (relatable frustration):*
> "Raise your hand if you've ever sent a staff product back because it missed the point entirely. Now raise your hand if you've been the one who sent it. That's the problem we're solving today."

*Option B (curiosity):*
> "I'm going to show you something in about ten minutes that I think will change how you approach staff work. But first I want to talk about why the way most people use AI right now is roughly equivalent to handing a new LT a blank piece of paper and saying 'write me an OPORD.'"

**Key points to hit:**
- AI tools are already in use across the force — whether leadership authorizes it or not. The question is whether people are using them well.
- Most people treat AI like a search engine or a magic 8-ball. It's neither.
- Prompt and context engineering is the skill that separates people getting garbage outputs from people getting products they can actually use.
- By end of this class: they'll understand why AI gives bad answers, and how to fix it.

**Transition:** "Before we get into technique, I want to give you a mental model for what's actually happening when you talk to one of these systems."

---

## Section 2: Core Mental Model (5 min)

**Goal:** One analogy that sticks. Don't get technical. Don't say "neural network."

**The analogy — use this and come back to it:**
> "Think about the best staff officer you've ever worked with. Day one, they show up knowing doctrine, knowing the Army, knowing how staff work is supposed to function. But they don't know your unit. They don't know your commander's priorities. They don't know what format your battalion uses for a decision brief. They don't know the current mission. So if you walk up to them on day one and say 'write me a risk assessment,' what do you get? Something technically correct and operationally useless. That's AI without good prompting and context."

> "Now imagine you spend 30 minutes with that same officer. You walk them through the unit, the mission, the commander's preferences, and the specific situation. Same officer — completely different product. That's what we're building today."

**Key points:**
- AI doesn't know your unit, your mission, your format preferences, or your commander — unless you tell it
- It's not searching the internet (usually). It's drawing on everything it was trained on and applying it to what you give it.
- The quality of the output is almost entirely a function of the quality of the input
- "Garbage in, garbage out" is true — but the more useful framing is: **"Brief it like you'd brief a new staff officer"**

**Transition:** "So how do you brief it? That's prompt engineering."

---

## Section 3: Prompt Engineering Fundamentals (15 min)

**Goal:** Teach the anatomy of a good prompt. Do a live demo. Let them try it.

**The anatomy (write this on the board or put it on a slide):**

```
ROLE     — Who are you talking to? What expertise should it have?
TASK     — What specifically do you need?
CONTEXT  — What does it need to know to do this well?
FORMAT   — How should it give you the answer?
```

**Walk through the transformation — use examples from `examples/bad_vs_good_prompts.md`**

Start with the bad prompt. Show the output live if possible. Then show the improved version. Let the contrast do the work.

**Suggested live demo sequence:**
1. Type the bad prompt. Show the output. Ask: "Is this something you'd send to your commander?"
2. Type the good version. Show the output. Ask: "What's different?"
3. Point out: same AI, same request — the prompt is the variable.

**Exercise 01 — Phone Exercise (3 min, built into this section):**
> "Take out your phone if you have it. Open whatever AI app you use — Claude, ChatGPT, doesn't matter. I want you to ask it to help you write a BLUF for any real task you're working on. Just type it like you normally would. We'll come back to this."

Let them try. Don't make it high pressure. A few will, most will watch.

After 90 seconds: "Okay — did anyone get something actually useful? What did you ask it?"

Take 1–2 answers. Then: "Now let's add a role, a format requirement, and some context and see what changes."

**Key points to leave them with:**
- Be specific about what you want
- Tell it who it's supposed to be (role)
- Tell it what format you need (BLUF, decision brief, bullet points)
- The more relevant detail you give, the less it has to guess

**Transition:** "Prompt engineering is about how you ask. Context engineering is about what you bring to the table."

---

## Section 4: Context Engineering (15 min)

**Goal:** Show that injecting the right documents/information transforms output quality. This is the "next level" for the audience.

**Opening reframe:**
> "Prompt engineering makes you a better questioner. Context engineering makes the AI a better advisor. The difference is whether you're asking a question or briefing an advisor."

**What is context?**
- The system prompt: instructions that run before the conversation — sets the AI's role, behavior, and constraints
- Injected documents: paste in your SOP, your unit's decision brief format, the relevant regulation, the mission statement
- Conversation history: what you've already established in the session

**The key insight:**
> "If you paste your battalion's risk assessment SOP into the chat before you ask for a risk assessment, you get your format, your thresholds, your language. If you don't, you get a generic template that you'll spend 20 minutes reformatting."

**Live demo — use `examples/context_injection_demo.md`:**
1. Ask for a risk assessment with no context
2. Then paste in the scenario details + format requirements and ask again
3. Let the difference speak for itself

**Exercise 02 — Phone Exercise (3 min):**
> "Go back to whatever you asked it a few minutes ago. This time, before you ask the question, paste in one paragraph of context — what you're working on, who it's for, and what format you need. See what changes."

**More advanced context techniques (if time):**
- **System prompts** — Setting behavior before the conversation. This is how you build a persistent "staff officer" persona.
- **Projects / Memory** — In Claude: you can create a Project and give it standing instructions. Every conversation in that project starts with your context already loaded. Equivalent to a staff officer who already knows your SOPs.
- **What makes good context:** Relevant (don't dump everything), structured (organized information is easier to use), concise (don't pad it)

**Key points:**
- Context is the brief. The more complete the brief, the better the product.
- You don't have to re-explain your unit every conversation — tools exist to persist that context
- Bad context is worse than no context — don't inject outdated or irrelevant information

**Transition:** "Let me bring this together before Q&A."

---

## Section 5: Wrapping Up (5 min)

**Goal:** Three things they'll remember walking out.

**The three takeaways:**

1. **AI is a staff officer, not a search engine.** It needs to be briefed. Treat it like you'd treat a capable but uninformed advisor — give it role, task, context, and format.

2. **Prompt engineering is how you ask. Context engineering is what you bring.** Master both and you've got a force multiplier. Skip both and you get outputs you'll throw away.

3. **Start with one real task this week.** Don't try to overhaul everything. Pick one thing you have to write — an award citation, a talking points memo, a training schedule — and apply what you learned today. See what happens.

**Closing line:**
> "The units and officers who figure this out early are going to have a significant advantage. You don't have to be a tech expert. You just have to know how to brief."

---

## Section 6: Q&A (10 min)

**Common questions and suggested responses:**

**"Is this authorized? Can we actually use AI for official products?"**
> "Policy is evolving. The short answer is: check your organization's guidance, don't put classified information into commercial AI systems, and always review and own the output before it goes anywhere. AI is a drafting tool, not a signing authority."

**"What about OPSEC?"
> "Treat it like you'd treat any unclassified system. Don't input unit-specific sensitive information, names of personnel, or anything you wouldn't put in an unclassified email. The example scenarios we use in training are generic for exactly that reason."

**"Which AI tool should I use?"**
> "The major ones — Claude, ChatGPT, Gemini — are broadly comparable for most staff tasks. Claude tends to handle long documents well. What matters more than the tool is the technique. The skills you learned today apply to all of them."

**"Can AI replace my S3?"**
> "No. And that's not the goal. AI doesn't have judgment, doesn't know your unit, doesn't go on the ground, and can't be held accountable. What it can do is help a good staff officer produce better products faster. It raises the floor — it doesn't replace the top."

**"What if it's wrong?"**
> "It will be wrong sometimes. That's why you review everything before it goes out. Think of it as a very fast first draft, not a finished product. Your job is still to apply judgment and own the output."

---

## Bonus: Agents & Advanced Applications (up to 30 min, if time allows)

Only go here if you've finished Q&A and the room is still engaged. This is the advanced material.

See `slides/06_bonus_agents.md` for the full outline.

**Suggested opener for bonus section:**
> "Okay — everything we've covered so far is what you can do right now with a free account on your phone. What I'm about to show you is what happens when you take this a step further."

---

## Room Management Notes

- If the room is senior-heavy: lean into the leadership angle — how do you get better products from your staff? How do you write a better decision brief for the CDR?
- If the room skews junior: lean into the "make your job easier" angle — stop spending Saturday reformatting award citations
- If energy is low after Section 3: move the Exercise 02 earlier and let the hands-on time re-engage the room
- If you're running long: cut Section 4's advanced techniques and go straight to the key points

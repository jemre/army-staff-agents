# Exercise 02 — Context Engineering
*Phone-friendly | 3 minutes | Used during Section 4*

---

## Instructions for Students

Go back to the prompt you improved in Exercise 01 — or start fresh with a new task.

**Step 1:** Before you ask your question, add a context block at the top. Include:

1. **Who the output is for** (your commander, your section, an external audience)
2. **The format you need** (BLUF + bullets, decision brief, plain paragraph, etc.)
3. **One or two key facts about the situation** that the AI can't guess

**Step 2:** Ask your question after the context block.

**Step 3:** Compare this output to your Exercise 01 result. What's different?

---

## Example — Adding Context to an Award Citation

**Exercise 01 version (prompt only):**
```
You are an Army awards NCO. Write an ARCOM citation for a staff
sergeant. Use third-person past tense, under 100 words, DA 638 format.
```

**Exercise 02 version (context added):**
```
CONTEXT:
- This citation is for a company-level award board. The commander
  wants specific, concrete language — no filler phrases.
- The Soldier is SSG [Name], the S4 NCOIC, who managed all Class IX
  supply for a 45-vehicle fleet across a 90-day mobilization.
- Key actions: zero mission-critical shortages, reduced discrepancy
  rate by 40%, resolved a brake component shortage 72 hours before a
  major exercise.

REQUEST:
You are an Army awards NCO. Write an ARCOM citation using the above
information. Third-person past tense. Under 100 words. DA Form 638
citation block format. No generic phrases.
```

Notice: the context block comes *before* the request. This gives the AI what it needs before it starts generating.

---

## Stretch: Persistent Context

If you want to try a more advanced technique:

**In Claude (free account):**
1. Create a new Project
2. In the Project instructions, paste a short description of your role, unit type, and format preferences
3. Every conversation in that project will start with that context already loaded

**Try it:** Create a project called "Staff Work" and add:
```
I am a [your role] in an Army National Guard unit. When I ask for
staff products, use Army format and terminology. Default to BLUF
format unless I specify otherwise. Be concise — my commander is
time-constrained.
```

---

## Debrief Questions

- What happened when you added context — was the output noticeably different?
- What would the ideal "standing context" be for your most common AI tasks?
- If you could pre-brief this AI on your job once and have it remember — what would you tell it?

---

## Notes for Instructor

- The persistent context stretch exercise is optional — use it if the room is engaged and technically comfortable
- The debrief question "what would you pre-brief it?" is a good discussion starter for senior leaders
- If someone asks about classified information: "Great question — you'd use a generic scenario description. The AI doesn't need your actual unit name to produce a useful product."

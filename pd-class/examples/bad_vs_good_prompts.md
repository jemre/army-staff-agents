# Bad vs. Good Prompts — Military Staff Examples

Side-by-side comparisons for use during instruction. Each example shows a weak prompt, the kind of output it produces, an improved prompt, and what changes.

---

## Example 1: Award Citation

**Weak prompt:**
```
Write me an award citation for a staff sergeant.
```
*Output: Generic template with [RANK], [NAME], [ACTION] blanks. Not usable.*

**Strong prompt:**
```
You are an Army awards NCO with 10 years of experience writing
award citations. Draft an Army Commendation Medal (ARCOM) citation
for a staff sergeant who:
- Led a 12-person logistics section during a 90-day mobilization
- Reduced supply discrepancy rate by 40% through a new tracking system
- Personally resolved a Class IX shortage that kept three vehicles FMC
  when the unit needed them most for a major training exercise

Use third-person past tense. Keep it under 100 words. Format it
for DA Form 638. Do not use filler phrases like "goes above and beyond."
Be specific and concrete.
```
*Output: Tight, specific, citation-ready draft.*

**What changed:** Role, specific actions, format constraints, word count, and a negative constraint ("do not use filler phrases").

---

## Example 2: BLUF Memo

**Weak prompt:**
```
Write a memo about changing our PT schedule.
```
*Output: Generic memo with no clear recommendation, no audience awareness.*

**Strong prompt:**
```
You are a company XO drafting a memo for your battalion commander.
Write a memo recommending a change to the company PT schedule from
0630 to 0530 start time, Monday through Friday.

Key points to include:
- Current schedule conflicts with the 0700 motor pool PMCS requirement
- Earlier start gives Soldiers 30 additional minutes for PMCS before
  the duty day
- Two peer companies in the battalion have already made this change

Format: BLUF at the top (one sentence), three bullet points of
background, one-sentence recommendation. Keep the whole thing
under 200 words.
```
*Output: Commander-ready draft with BLUF, tight background, clear recommendation.*

---

## Example 3: Risk Assessment

**Weak prompt:**
```
Help me write a risk assessment for a field exercise.
```
*Output: Generic 5-row table with Hazard/Probability/Severity/Controls/Residual Risk — no unit relevance.*

**Strong prompt:**
```
You are an Army S3 operations officer. Help me build a risk assessment
for a battalion field training exercise with the following details:

- Duration: 5 days, field environment
- Activities: live fire (platoon level), land navigation, vehicle convoy
- Personnel: approximately 600 Soldiers
- Known issues:
  * Two of four assigned medics are unavailable
  * Forecasted high temperatures (95°F) with high humidity
  * One HMMWV with a recurring brake issue is scheduled for the convoy

Identify at least five hazards. For each, provide:
- Probability (Low/Medium/High)
- Severity (Negligible/Marginal/Critical/Catastrophic)
- Initial risk level
- Specific, actionable controls
- Residual risk after controls
- Approval authority if residual risk is Medium or above

Flag any condition that should be a go/no-go gate.
```
*Output: Actionable risk matrix with gate conditions, usable as a working draft.*

---

## Example 4: Talking Points

**Weak prompt:**
```
Write talking points for a commander's call.
```
*Output: Generic bullets about "communication," "teamwork," and "mission readiness."*

**Strong prompt:**
```
You are a battalion XO preparing talking points for the battalion
commander's monthly commander's call. The commander's priorities
for this month are:

1. Soldier physical readiness — APFT failure rate is up 12% from
   last quarter. Commander wants units to increase PT accountability,
   not just frequency.
2. Vehicle readiness — Three vehicles missed a major exercise due to
   maintenance that was deferred. Commander wants this to stop.
3. Positive recognition — Two Soldiers from Bravo Company were
   recognized at brigade level last week. Commander wants to highlight this.

Write five talking points. Each should:
- Be one sentence the commander can read directly
- Be direct and plain-spoken (no jargon, no filler)
- End with a specific expectation or action, not a vague aspiration
```
*Output: Five punchy, direct talking points the commander can read verbatim.*

---

## Example 5: Training Schedule Event Description

**Weak prompt:**
```
Write a training schedule event for a weapons qualification.
```
*Output: Generic entry with no task, condition, or standard.*

**Strong prompt:**
```
Write a training schedule entry for an M4 carbine qualification event.
Format it for a weekly training schedule with these fields:
- Task (using Army task format)
- Conditions
- Standard
- Date/Time: Thursday 0600-1600
- Location: Range 12
- OIC: [OIC]
- NCOIC: [NCOIC]
- Uniform: ACU with body armor and helmet
- Required equipment: Weapon, 3x magazines, 90 rounds per Soldier

Use the Army task: "071-COM-0030, Engage Targets with an M4 Carbine"
Standard: 23 of 40 targets for qualification (Expert: 36+)
```
*Output: Ready-to-paste training schedule entry in proper format.*

---

## Key Patterns Across All Examples

| Pattern | Description |
|---------|-------------|
| **Role first** | Always start with who the AI is |
| **Specific beats generic** | Named tasks, actual numbers, real constraints |
| **Format specified** | Tell it exactly how the output should look |
| **Negative constraints** | "Do not use..." eliminates common AI tendencies |
| **Context provided** | Relevant situation details, not a blank slate |
| **One task at a time** | Don't bundle five requests into one prompt |

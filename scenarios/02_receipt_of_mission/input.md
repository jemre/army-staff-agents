# Scenario 02 — Receipt of Mission (MDMP Step 1)

## Scenario Overview

**Lead Agent:** `/xo`
**Supporting Agents:** `/s2`, `/s3`, `/s4`, `/s1`, `/s6`
**Product Type:** WARNO #1, Initial Time Analysis, Planning Timeline, Staff Initial Tasks
**Complexity:** High
**Context Required:** `context/mission/III_CORPS_OPORD_32205-26_4ID_extract.md`

---

## Setup Instructions

Before invoking the XO, inject the mission context:

```
/xo
> Read context/mission/III_CORPS_OPORD_32205-26_4ID_extract.md before we begin.
```

---

## Commander's Input

---

XO, III CORPS just issued OPORD 32205-26 (BALTIC BASTION). We are 4th Infantry Division. I need the staff to conduct receipt of mission now.

Read the OPORD extract in `context/mission/III_CORPS_OPORD_32205-26_4ID_extract.md`.

Conduct the full receipt of mission sequence and produce the following:

1. **Initial time analysis** — How much time do we have? Apply the 1/3-2/3 rule. Identify the planning timeline windows available given the compressed schedule. Be specific: show the math from OPORD effective DTG to the first constraint that restricts our freedom to plan.

2. **WARNO #1** — Issue an immediate warning order to all subordinate units and attachments. Include: the mission we've been given, our higher's intent (III CORPS), earliest movement, task organization, and initial priorities for each section. This goes to 1/3 ABCT, 3/4 ABCT, 26 MEB, and all attached elements.

3. **Planning timeline** — A sequenced timeline from now through the Combined Arms Rehearsal showing each major planning event, who owns it, and when it must occur. Anchor to the known fixed events in the OPORD.

4. **Staff initial tasks** — Assign initial tasks to each staff section: S2, S3, S4, S1, S6. Each section should know what product they owe, when it is due, and what information they need to start.

Be direct. This is time-critical. Apply the 1/3-2/3 rule and give me real timelines based on the OPORD. Flag any assumptions you have to make because the extract doesn't give us everything. Do not invent facts — if a piece of information is missing from the OPORD extract, say so and note what would need to be confirmed.

---

## Notes for Evaluators

This scenario tests whether the agents:
- Apply doctrinal MDMP Step 1 outputs correctly
- Perform real time-distance math from the OPORD DTGs
- Identify gaps in available information rather than inventing details
- Issue a tactically coherent WARNO with correct subordinate addressees
- Assign staff initial tasks that reflect WfF responsibilities

See `evaluation.md` for the full evaluation checklist.

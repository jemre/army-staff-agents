# Context Injection Demo — Live Instructor Guide

Use this file during Section 4 to demonstrate the difference context makes. Run both rounds live.

---

## Demo: Training Event Risk Assessment

### Round 1 — No Context

Type this exactly:

```
Write a risk assessment for a live fire training event.
```

**What to expect:** Generic 4–6 row table. Hazards like "accidental discharge," "heat injury," "vehicle accident." Controls like "enforce safety procedures" and "conduct safety briefing." No specifics, no unit relevance.

**Ask the room:** "Would you send this to your commander? What's missing?"

Expected answers: No unit details, no specific controls, no format match, no go/no-go criteria.

---

### Round 2 — With Context

Paste this entire block, then send:

```
I need a risk assessment for the following training event. Use this
information to produce a specific, actionable product.

SITUATION:
- Event: Battalion live fire exercise, platoon-level attack lanes
- Units: Three rifle companies (~600 Soldiers total)
- Duration: One day, 0500–1600
- Location: Training area, range complex

KNOWN RISK FACTORS:
- Medical: Only 2 of 4 assigned medics are available
- Weather: Forecast 95°F, high humidity (Heat Category IV likely)
- Live fire: Crew-served weapons (M240, M249) on each lane

FORMAT REQUIRED:
For each hazard provide: Hazard | Probability (Low/Med/High) |
Severity (Negligible/Marginal/Critical/Catastrophic) | Initial Risk |
Controls (specific and actionable) | Residual Risk | Approval Authority

Flag any hazard that should be a go/no-go gate for the Commander.
End with a BLUF recommendation: GO / CONDITIONAL GO / NO-GO.
```

**What to expect:** Specific hazard matrix with the medical shortfall called out as a gate condition, heat category work/rest ratios, specific controls (not generic ones), go/no-go recommendation.

**Ask the room:** "Same AI, 60 seconds apart. What changed?"

Expected answer: The context changed. The AI had something specific to work with.

---

## Demo: Award Citation (Alternative or Additional)

### Round 1 — No Context

```
Write an ARCOM citation.
```

**Expected output:** Generic template with brackets for name, rank, action.

---

### Round 2 — With Context

```
Write an ARCOM citation for the following Soldier:

Rank: Staff Sergeant
Role: Logistics section NCOIC
Period: 12-month period, including a 90-day mobilization
Key actions:
- Managed Class IX supply for a 45-vehicle fleet with zero mission-critical
  shortages across the mobilization
- Developed a tracking system that reduced supply discrepancy rate by 40%
- Personally resolved a brake component shortage 72 hours before a major
  exercise that would have grounded three vehicles

Format: Third-person, past tense. Under 100 words. DA Form 638 citation
block format. Do not use generic phrases like "goes above and beyond" or
"with great dedication." Use specific, concrete language only.
```

**Expected output:** Tight, specific, ready-to-review citation.

---

## Debrief Points for Either Demo

1. **Same AI, same capability** — what changed was what we gave it
2. **The brief is the product** — a good context block is a skill in itself
3. **Iteration is still expected** — this is a draft, not a final product; you still review and own it
4. **OPSEC note** — in a real scenario, use generic unit designations; the AI doesn't need the actual unit name to produce a good product

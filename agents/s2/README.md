# S2 Agent — Intelligence Officer

The S2 reduces uncertainty for the Commander by leading IPB, analyzing the threat, and producing intelligence products that drive planning and execution.

## Files

| File | Purpose |
|------|---------|
| `system_prompt.md` | Core S2 prompt — LLM-agnostic, works in Claude, GPT, Gemini, etc. |

## Quick Start (Claude Code)

```
/s2
```

## Quick Start (Browser / Other LLMs)

Copy the contents of `system_prompt.md` into the system prompt field.

## Key Products

| Product | Purpose |
|---------|---------|
| Intelligence Estimate | Full threat and terrain assessment supporting MDMP |
| IPB Products | Terrain overlays, threat COA sketches, event template, DST |
| SALUTE / SPOTREP | Standardized enemy contact reporting |
| INTSUM | Periodic intelligence summary |
| Collection Plan | PIR/IR tasking matrix |
| Threat Assessment Brief | Commander-ready threat picture |
| CCIR / PIR Tracker | Status of priority information requirements |

## IPB at a Glance

```
1. Define Operational Environment
2. Describe Environmental Effects (OAKOC + Weather + ASCOPE)
3. Evaluate the Threat (SALUTE, capabilities, vulnerabilities, HVTs)
4. Determine Threat COAs (most likely / most dangerous → Event Template → DST)
```

## Coordination With Other Sections

- **S3** — Scheme of maneuver, NAI/TAI placement
- **S4** — Enemy logistics nodes for HPT development
- **FSO** — Target acquisition, fires coordination
- **S6** — SIGINT support
- **Higher S2** — All-source products, imagery, HUMINT

# XO Orchestration Pattern

Documents how the XO agent delegates to staff sections and how that pattern evolves as skills and MCP servers are added.

---

## Agent Architecture — Doctrinal Basis

Based on FM 6-0, ATP 5-0.2-1, and ADP 3-0. The architecture reflects actual battalion/brigade staff structure.

### Warfighting Function to Agent Mapping

| WfF | WfF Lead | Agent | Staff Type | Reports To |
|-----|----------|-------|-----------|-----------|
| C2 | XO | `/xo` | XO/COS | Commander |
| Movement & Maneuver | S3 | `/s3` | Coordinating staff | XO |
| Intelligence | S2 | `/s2` | Coordinating staff | XO |
| Fires | FSO | `/fso` | **Special staff** | S3 (not XO directly) |
| Protection | S3 (at bn/bde) | `/protection` | Through S3 | S3 (not XO directly) |
| Sustainment | S4 | `/s4` | Coordinating staff | XO |

**Key doctrinal notes:**
- The FSO and Protection agents coordinate through S3, not directly to XO
- The S3 leads TWO WfFs: M&M (primary) and Protection (by default at bn/bde)
- The S4 sustainment cell integrates S1, Surgeon, and Finance — sustainment WfF is broader than logistics
- The S6 is a C2 enabler, not a WfF lead
- The SGM and Chaplain are advisory staff, not WfF-aligned

## Current State (Prompt-Based)

The XO system prompt is the single entry point. When a task requires staff section input, the XO either:
1. Produces that section's contribution inline, noting it as a placeholder
2. Pauses and instructs the user to switch to the relevant section agent (via slash command) and return the output

**Doctrinal delegation sequence for XO:**
- Call S2 and S3 in parallel for planning tasks (IPB and M&M planning are concurrent)
- FSO routes through S3 — XO tasks S3, S3 tasks FSO
- Protection routes through S3 — XO tasks S3, S3 tasks Protection
- S4 integrates S1 and medical input — XO tasks S4 for the full sustainment picture

## Target State (Skills + MCP)

```
Commander (User)
      │
      ▼
   XO Agent (C2 WfF)
      │
      ├──► S2 Agent (Intel WfF)
      │
      ├──► S3 Agent (M&M + Protection WfF)
      │         ├──► FSO Agent (Fires WfF — through S3)
      │         └──► Protection Agent (Protection WfF — through S3)
      │
      ├──► S4 Agent (Sustainment WfF)
      │         ├──► S1 Agent (Personnel services — sustainment cell)
      │         └──► Surgeon (Health service support — sustainment cell)
      │
      ├──► S6 Agent (C2 enabler — comms/network)
      │
      └──► /mcp:slides ──► Slide Creation MCP
```

### Planned Skills

| Skill | Trigger | Routes Through | What It Does |
|-------|---------|---------------|--------------|
| `s2` | XO needs threat analysis or IPB | XO directly | Activates S2 agent |
| `s3` | XO needs operations plan, training, or protection | XO directly | Activates S3 agent |
| `fso` | S3 needs fires integration | S3 → FSO | Activates FSO agent |
| `protection` | S3 needs protection WfF products | S3 → Protection | Activates Protection agent |
| `s4` | XO needs sustainment WfF picture | XO directly | Activates S4 agent (integrates S1 + medical) |
| `s1` | S4 needs personnel/HR input for sustainment cell | S4 → S1 | Activates S1 agent |
| `s6` | XO or S3 needs comms plan or network status | XO or S3 | Activates S6 agent |
| `slides` | Any agent needs to produce a slide deck | Any agent | Calls slide creation MCP |

### Planned MCP Servers

| MCP Server | Purpose |
|------------|---------|
| `slides-mcp` | Converts structured markdown outlines into formatted presentation files (PowerPoint/Google Slides). Useful for both staff briefings and PD class materials. |
| `docx-mcp` | Produces formatted Word documents from staff product templates |
| `unit-context-mcp` | Loads and injects unit-specific context (roster, equipment, mission) into agent sessions |

## Context Injection Pattern

Context is kept separate from agent definitions so it can be swapped between tasks:

```
context/unit/        ← who we are
context/mission/     ← what we're doing
context/sop/         ← how we do things
context/reference/   ← doctrine and regs
```

When starting a session, inject the relevant context files alongside the system prompt. The XO does not hardcode unit identity — it reads from injected context.

## Slide Creation Vision

The `slides-mcp` server will accept a structured markdown outline and produce actual slide files. This serves two use cases:

1. **Staff Products** — XO produces a briefing outline; slides MCP renders it into a formatted deck
2. **PD Class** — Class outlines in `pd-class/slides/` are rendered into presentation-ready files

The markdown-first approach means content stays in version control and is LLM-readable, while the MCP handles the rendering concern.

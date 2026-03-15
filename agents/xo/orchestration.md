# XO Orchestration Pattern

Documents how the XO agent delegates to staff sections and how that pattern evolves as skills and MCP servers are added.

---

## Current State (Prompt-Based)

The XO system prompt is the single entry point. When a task requires staff section input, the XO either:
1. Produces that section's contribution inline, noting it as a placeholder
2. Pauses and instructs the user to switch to the relevant section agent (via slash command) and return the output

## Target State (Skills + MCP)

```
Commander (User)
      │
      ▼
  XO Agent  ──── /skill:s2  ────►  S2 Agent
      │      ──── /skill:s3  ────►  S3 Agent
      │      ──── /skill:s4  ────►  S4 Agent
      │      ──── /mcp:slides ───►  Slide Creation MCP
      │
      ▼
  Staff Product
```

### Planned Skills

| Skill | Trigger | What It Does |
|-------|---------|--------------|
| `s1` | XO needs personnel data or admin product | Activates S1 agent with current context |
| `s2` | XO needs threat analysis or IPB | Activates S2 agent with current context |
| `s3` | XO needs operations plan or training schedule | Activates S3 agent with current context |
| `s4` | XO needs logistics estimate or supply status | Activates S4 agent with current context |
| `s6` | XO needs comms plan or network assessment | Activates S6 agent with current context |
| `slides` | Any agent needs to produce a slide deck | Calls slide creation MCP with structured content |

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

# XO Agent — Executive Officer

The XO is the primary orchestrator. It receives a task or commander's intent, decomposes it into staff actions, delegates to the appropriate sections, and synthesizes outputs into a final staff product.

## Files

| File | Purpose |
|------|---------|
| `system_prompt.md` | Core XO prompt — LLM-agnostic, works in Claude, GPT, Gemini, etc. |
| `CLAUDE.md` | Claude Code usage instructions and workflow |
| `orchestration.md` | Delegation pattern, planned skills, and MCP server roadmap |

## Quick Start (Claude Code)

```
/xo
```

## Quick Start (Browser / Other LLMs)

Copy the contents of `system_prompt.md` into the system prompt field. Then begin your session with commander's intent or a task.

## Outputs

The XO produces Army-standard staff products:
- Decision Briefs
- OPORDs / FRAGOs / WARNOs
- Staff Estimates
- Briefings (SBFDRC format)
- Risk Assessments

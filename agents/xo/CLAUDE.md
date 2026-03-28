# XO Agent — Claude Code Usage

## Activating the XO

Use the slash command from anywhere in this project:

```
/xo
```

This loads the XO system prompt and starts a coordinated staff session.

## Activating Staff Sections

Each staff section has its own slash command. The XO will tell you when to invoke one:

```
/s1   Personnel & Admin
/s2   Intelligence
/s3   Operations
/s4   Logistics
/s6   Signal
/sgm  Senior Enlisted Advisor
/chaplain  Unit Ministry Team
```

## Injecting Context

Before starting a task, inject relevant context files into your session:

```
/xo
> Read context/unit/unit_context.md and context/mission/current_opord.md before we begin.
```

Or reference them directly in your first message to the XO.

## Typical Workflow

1. `/xo` — Start the XO agent
2. Provide commander's intent or a task
3. XO decomposes the task and identifies which sections need to contribute
4. Invoke section agents as directed (`/s2`, `/s3`, etc.)
5. Return section outputs to the XO for integration
6. XO produces the final staff product

## Output Location

All completed staff products are saved to the **`outputs/` folder at the project root**. This folder is git-ignored and is the correct location for all agent-produced products.

- **Path:** `outputs/YYYYMMDD_<product_name>.md`
- Example: `outputs/20260316_S2_intel_running_estimate.md`
- The XO is responsible for communicating this path to all staff agents (S1, S2, S3, S4, S6, FSO, SGM, Chaplain) when invoking them, so every section writes its products to the correct location.
- Do **not** save to `products/` or scenario subfolders.

## Tips

- Keep context files short and structured — the XO performs better with clean, factual context
- For large products (OPORDs, full briefings), break into phases: planning, drafting, refinement

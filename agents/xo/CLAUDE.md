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

## Tips

- Keep context files short and structured — the XO performs better with clean, factual context
- For large products (OPORDs, full briefings), break into phases: planning, drafting, refinement
- Save completed products to `products/` with a date prefix: `YYYYMMDD_product_name.md`

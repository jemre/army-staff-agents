# XO Agent — Executive Officer

The XO agent is the primary orchestrator. It receives a task or commander's intent, delegates to the appropriate staff sections, and synthesizes their outputs into a final staff product.

## Usage

1. Provide commander's intent or a specific task
2. The XO will identify which staff sections need to contribute
3. Spin up the relevant section agents (S1–S6, SGM, Chaplain) as needed
4. XO integrates outputs and produces the final product

## Files

- `system_prompt.md` — XO role definition and behavior instructions
- `context.md` — Default context injected into XO sessions

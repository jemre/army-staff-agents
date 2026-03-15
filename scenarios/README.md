# Scenarios

Example scenarios for testing and validating agent behavior. Each scenario is self-contained: it includes the commander's input, which agents to invoke, expected outputs, and evaluation criteria.

Use these to:
- Reproduce consistent test cases after modifying agent prompts
- Demonstrate agent capability to new users
- Validate that changes to one agent don't break XO coordination

---

## Scenario Index

| # | Name | Agents Exercised | Product Type | Complexity |
|---|------|-----------------|--------------|------------|
| 01 | [Training Event Risk Assessment](01_training_risk_assessment/) | XO, S3, S4 | Risk Assessment + Go/No-Go Recommendation | Low |

---

## How to Run a Scenario

1. Open Claude Code in this project directory
2. Start with `/xo` (or the lead agent specified in the scenario)
3. Paste the **Commander's Input** from the scenario's `input.md`
4. Follow the agent prompts — invoke section agents as directed
5. Compare output against `expected_output.md` and evaluate using the criteria in `evaluation.md`

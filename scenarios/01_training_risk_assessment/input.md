# Scenario 01 — Input

## Commander's Input

> Paste this into the XO agent to begin the scenario.

---

XO, I need a risk assessment for a battalion-level live fire exercise next week. We'll have three rifle companies conducting platoon-level attack lanes with organic crew-served weapons. We're going short on medics — only two of our four assigned are available. Weather forecast shows temperatures hitting 95°F with high humidity. I need a go/no-go recommendation with controls. Coordinate with the S3 and S4 as needed.

---

## Agents to Invoke (recommended, but use any agents necessary to develop a good product)
1. `/xo` — Receives the task, decomposes it, coordinates sections
2. `/s3` — Training event plan, range safety, control measures
3. `/s4` — Medical coverage, equipment readiness, water resupply

## Expected Product
- Write products to /outputs. Use a 
- Risk Assessment (hazard identification, probability/severity, controls, residual risk)
- Go/No-Go recommendation with rationale
- Commander's decision brief format (optional stretch)

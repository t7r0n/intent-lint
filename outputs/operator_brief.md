# Operator Brief: Imprezia

Imprezia gets a local, deterministic pressure test around imprezia, pitch, and integration. The useful part is not the dashboard; it is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- imprezia evidence replay -> block release until cited evidence is regenerated (imprezia_coverage, evidence ev_0132).
- inside operator packet -> accept only if decision claims cite fixture evidence (pitch_risk, evidence ev_0099).
- integration regression harness -> open a regression issue with trace and benchmark delta (integration_precision, evidence ev_0022).
- pitch boundary probe -> route to reviewer with evidence packet (inside_latency, evidence ev_0121).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.

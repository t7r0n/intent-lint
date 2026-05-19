# Intent Lint

An open developer toolkit + benchmark that lets an AI app dev simulate, audit, and gate Imprezia style intent ad insertions before they ship - turning "trust the network" into "trust and verify in CI."

## Why This Exists

Imprezia's pitch is "one line integration, ad inside the LLM response, intent matched to advertiser." But every AI app developer who's been at this for 2 weeks knows the real question is: "If I let this network insert brand mentions into my product's voice, how do I prevent (a) hallucinated facts about the brand, (b) tonal mismatch with my product, (c) policy violations for regulated verticals (healthcare, finance, kids), and (d) latency tax that breaks streaming?

## What It Builds

- Replays synthetic `imprezia` and `pitch` cases against the project's evidence rules.
- Scores `imprezia_coverage`, `pitch_risk`, and `integration_precision` so regressions are visible in CSV and JSON.
- Plants `imprezia drift` and `pitch gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `intent-lint` without hosted services.

## Local Run

```bash
uv sync
uv run intent-lint all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://www.ycombinator.com/companies/imprezia
- https://www.ycombinator.com/launches/O5Q-imprezia-world-s-first-ai-ad-network
- https://www.ycombinator.com/companies/imprezia/jobs/HDrJSMq-founding-engineer-core-systems
- https://www.ycombinator.com/companies/imprezia/jobs/jjpOc4q-growth-ai-developers
- https://www.linkedin.com/posts/y-combinator_ads-suck-but-only-because-they-interrupt-activity-7356790766544801792-RmCO
- https://www.linkedin.com/in/bisheshkhadka/
- https://x.com/bisheshk
- https://www.linkedin.com/posts/bisheshkhadka_humbled-by-the-response-to-imprezias-launch-activity-7358932922348851201-2fi5
- https://huggingface.co/vectara/hallucination_evaluation_model

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.

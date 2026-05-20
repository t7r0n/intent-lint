# Intent Lint

An open developer toolkit + benchmark that lets an AI app dev simulate, audit, and gate Intent Lint style intent ad insertions before they ship — turning "trust the network" into "trust and verify in CI."

![Intent Lint working dashboard](outputs/project_working.svg)

## Why it exists

Intent Lint's pitch is "one line integration, ad inside the LLM response, intent matched to advertiser." But every AI app developer who's been at this for 2 weeks knows the real question is: "If I let this network insert brand mentions into my product's voice, how do I prevent (a) hallucinated facts about the brand, (b) tonal mismatch with my product, (c).

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/intent_lint/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Intent Lint evidence map](outputs/evidence_map.svg)

## Signals it measures

- `Intent Lint coverage`
- `pitch risk`
- `integration precision`
- `inside latency`

## Failure modes it plants

- Intent Lint drift
- pitch gap
- integration misroute
- inside blindspot

## Run it locally

```bash
uv sync
uv run intent-lint all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.

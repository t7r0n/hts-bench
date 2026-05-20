# Hts Bench

The first public, reasoning aware HTS classification benchmark — built on CROSS rulings, scored on both code accuracy and GRI citation fidelity. Hts Bench tops the leaderboard on day one.

![Hts Bench working dashboard](outputs/project_working.svg)

## Why it exists

Hts Bench's strongest claim is reasoning grade HTS classification with full GRI audit trails. The company has now published this claim in three blog posts and grounded their differentiation on it ("compliance grade accuracy", "staged determination at 4 digit -> 6 digit -> 8 digit -> 10 digit"). But there is no public benchmark they can point a.

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/hts_bench/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Hts Bench evidence map](outputs/evidence_map.svg)

## Signals it measures

- `Hts Bench coverage`
- `strongest risk`
- `claim precision`
- `reasoning latency`

## Failure modes it plants

- Hts Bench drift
- strongest gap
- claim misroute
- reasoning blindspot

## Run it locally

```bash
uv sync
uv run hts-bench all
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

# Hts Bench

The first public, reasoning aware HTS classification benchmark - built on CROSS rulings, scored on both code accuracy and GRI citation fidelity. GingerControl tops the leaderboard on day one.

## Why This Exists

GingerControl's strongest claim is reasoning grade HTS classification with full GRI audit trails. The company has now published this claim in three blog posts and grounded their differentiation on it ("compliance grade accuracy", "staged determination at 4 digit -> 6 digit -> 8 digit -> 10 digit"). But there is no public benchmark they can point a Fortune 500 customs director at to verify the claim.

## What It Builds

- Replays synthetic `gingercontrol` and `strongest` cases against the project's evidence rules.
- Scores `gingercontrol_coverage`, `strongest_risk`, and `claim_precision` so regressions are visible in CSV and JSON.
- Plants `gingercontrol drift` and `strongest gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `hts-bench` without hosted services.

## Local Run

```bash
uv sync
uv run hts-bench all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/domain_rubric.json`
- `outputs/failure_matrix.md`
- `outputs/trace_graph.mmd`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://gingercontrol.com/blog/ai-trade-compliance
- https://gingercontrol.com/blog/automated-hts-code-classification-tools
- https://gingercontrol.com/blog/hs-code-classification-marketplace
- https://gingercontrol.com/about
- https://www.gingercontrol.com/services/features
- https://www.trysignalbase.com/news/funding/gingercontrol-secures-21m-seed
- https://www.backed.vc/portfolio/ginger-control
- https://www.crunchbase.com/organization/gingercontrol
- https://rulings.cbp.gov/
- https://www.linkedin.com/in/chen-cui-6853271b8/

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.

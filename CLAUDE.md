# CLAUDE.md: World Labs Product Operations Playground

## What This Is

A Product Operations environment for World Labs, oriented toward the day-to-day work. 23 skills installed in `.claude/skills/` and ready to invoke. Skills produce structured artifacts grounded in the pre-researched `context/` layer and generally available market signals.

## Start Here

If you're new to this repo, run these skills in order. Each builds on the one before it.

| # | Skill | Why First | What You Get |
|---|---|---|---|
| 1 | `competitive-response` | Know the landscape before making bets | Threat matrix + moat audit + response playbook |
| 2 | `customer-discovery` | Start talking to users/developers immediately | Interview guide + synthesis framework |
| 3 | `spatial-ai-product-strategy` | Understand the full product portfolio (Marble, API, RTFM) | Capability map + platform strategy + portfolio design |
| 4 | `real-time-persistent-convergence` | Work through the RTFM + Marble question | Convergence patterns + multi-model API + pricing |
| 5 | `north-star-metrics` | Define what you're measuring | Metric tree + dashboard design |
| 6 | `feature-prioritization` | Make your first prioritization call | Scored backlog + sequenced roadmap |

## Running Skills

All 23 skills are in `.claude/skills/` and auto-discovered by Claude Code. Users can invoke them by name or by describing a PM/Ops question.

When a skill is invoked:

1. **Read the skill file** from `.claude/skills/`
2. **Read all relevant `context/` files** (always load the full context before starting):
   - `context/company/`: company intel, investor thesis
   - `context/competitive/`: landscape, Genie 3 analysis, other competitors
   - `context/founders/`: Fei-Fei Li, Ben Mildenhall, Justin Johnson, Christoph Lassner
   - `context/products/`: Marble app, World API, RTFM
   - `context/verticals/`: gaming, robotics, architecture, film/VFX
   - `context/signals/`: auto-collected signals (see Signal Freshness below)
3. **Follow the skill's Instructions section step by step**, producing each artifact
4. **Write output** to `applied/` in the appropriate subdirectory:
   - `applied/strategic/`: strategy, competitive, positioning outputs
   - `applied/cross-product/`: product vision, roadmaps spanning multiple products
   - `applied/marble-app/`: Marble app-specific analyses
   - `applied/world-api/`: World API-specific analyses
   - `applied/rtfm/`: RTFM-specific analyses

## Decision Playbooks

When something happens, reach for the right skill:

| Situation | Run This |
|---|---|
| Driving launch readiness for a Marble release | `zero-to-one-product-launch` |
| Aligning owners across teams | `stakeholder-alignment` |
| Working a burndown or prioritizing the backlog | `feature-prioritization` + `stakeholder-alignment` |
| Onboarding a design partner | `customer-discovery` |
| Writing a PRD | `writing-prds-for-ai` |
| Assessing a partnership | `partnership-evaluation` |
| New research breakthrough ready to ship | `research-to-product-pipeline` |
| Competitor launches something | `competitive-response` |
| Wondering how RTFM and Marble connect | `real-time-persistent-convergence` |
| Growing the developer ecosystem | `api-ecosystem-flywheel` |
| Evaluating a new vertical | `vertical-market-assessment` |
| API DX feels off | `developer-experience-audit` + `api-design-review` |
| Pricing decisions | `pricing-and-monetization` |
| Understanding user segments | `user-segmentation` |

## Operating Cadence

| Frequency | Action |
|---|---|
| **Weekly** | Run the launch-readiness and risk-register check (`zero-to-one-product-launch`), then refresh signals: `cd pm-playbook && python3 -m collectors.run --config ../signals.yaml` |
| **Monthly** | Re-run `competitive-response` (landscape shifts fast) |
| **Quarterly** | Re-run `north-star-metrics` and `feature-prioritization` |
| **After every skill run** | Run `/improve` to build the reflection log in `applied/_reflections.md` |

## Skill Chaining

After completing any skill, check `pm-playbook/skill-graph.yaml` for the `feeds_into` list of the skill you just ran. Briefly mention which skills would logically follow and why; for example, "Customer Discovery typically feeds into User Segmentation and Measuring PMF." Ask the user if they want to run one next.

## Signal Freshness Check

Before running any skill, check `context/signals/` for existing signal files. Look at the timestamp in each file's header (e.g., "Auto-collected on 2026-02-06"):

- **If signals are less than 7 days old**: Use them as-is.
- **If signals are older than 7 days OR `context/signals/` is empty**: Ask the user if they want to refresh signals first. To refresh:
  ```bash
  cd pm-playbook && python3 -m collectors.run --config ../signals.yaml
  ```
  This requires API keys in `.env` (see `.env.example`). At minimum, the HN collector works with no auth.
- **If the user declines**: Proceed without signals. Skills work fine with just the manual `context/` files.

## Evidence Tags

All data points in outputs should be tagged:

| Tag | Meaning |
|---|---|
| `[PUBLIC]` | From publicly available information |
| `[TESTED]` | Verified through direct testing |
| `[ILLUSTRATIVE]` | Hypothetical example demonstrating methodology |
| `[SIGNAL]` | Auto-collected by the collectors framework. Check timestamp for freshness. |

## Signal Collectors

The `pm-playbook/collectors/` framework auto-collects public data into `context/signals/`. Config lives in `signals.yaml` at the repo root.

```bash
# Run all enabled collectors
cd pm-playbook && python3 -m collectors.run --config ../signals.yaml

# Run one collector
python3 -m collectors.run --config ../signals.yaml -c hackernews

# Preview without writing files
python3 -m collectors.run --config ../signals.yaml --dry-run
```

| Collector | Auth Required | What It Collects |
|---|---|---|
| `hackernews` | None | HN stories matching configured keywords |
| `github` | `GITHUB_TOKEN` | Repo stars, forks, issues, PRs for tracked repos |
| `reddit` | `REDDIT_CLIENT_ID` + `REDDIT_CLIENT_SECRET` | Posts from configured subreddits |
| `news` | `NEWS_API_KEY` | Articles from NewsAPI |

## Directory Structure

```
├── CLAUDE.md              ← You are here
├── .claude/skills/        ← 23 skills (auto-discovered by Claude Code)
├── signals.yaml           ← Collector config (what to watch)
├── .env                   ← API keys (not committed)
├── pm-playbook/          ← Git submodule: general skills + collectors
├── skills/                ← World Labs-specific skill sources
├── context/               ← Company knowledge base
│   ├── company/           ← Company intel, investor thesis
│   ├── competitive/       ← Landscape, competitor analyses
│   ├── ecosystem/         ← SparkJS renderer (ecosystem infrastructure)
│   ├── founders/          ← Founder profiles, public statements
│   ├── products/          ← Marble, World API, RTFM
│   ├── verticals/         ← Gaming, robotics, architecture, film
│   └── signals/           ← Auto-collected (GitHub, HN, Reddit, news)
└── applied/               ← Outputs from skill runs
```

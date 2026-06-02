# World Labs Product Ops Playbook

An operating system for the Marble team: run-of-business cadence, launch readiness, and design-partner onboarding, pre-loaded with company context, competitive intelligence, and 23 product skills. Clone it, open [Claude Code](https://claude.ai/download), and start running the operating cadence grounded in World Labs data.

## Setup

```bash
git clone --recursive https://github.com/ashstep2/wl-product-playbook.git
cd wl-product-playbook
```

Open in Claude Code. Done. All 23 skills are auto-discovered and the full company context is pre-loaded.

> Already cloned without `--recursive`? Run `git submodule update --init`

## What to Ask

| Try This | What You Get | Skill |
|---|---|---|
| "Align stakeholders on the Marble 1.1 launch" | Owner alignment + communication plan | `stakeholder-alignment` |
| "Prioritize features for next quarter" | Weighted scoring matrix + sequenced roadmap | `feature-prioritization` |
| "Build launch readiness for the next Marble release" | Launch checklist + go-to-market strategy | `zero-to-one-product-launch` |
| "Write a PRD for [feature]" | PRD with AI-specific eval criteria + uncertainty handling | `writing-prds-for-ai` |
| "Evaluate a partnership with NVIDIA for robotics" | Partner scorecard + deal structure + go/no-go | `partnership-evaluation` |
| "How should we respond to Project Genie?" | Threat matrix + moat audit + response playbook | `competitive-response` |
| "How should RTFM and Marble work together?" | Convergence patterns + multi-model API design + pricing | `real-time-persistent-convergence` |
| "Audit the developer experience of our API" | Friction scorecard + time-to-hello-world + DX roadmap | `developer-experience-audit` |
| "Design the World API pricing tiers" | Pricing model + WTP analysis + competitive benchmarks | `pricing-and-monetization` |
| "Grow the developer ecosystem" | Activation funnel + SDK roadmap + community flywheel | `api-ecosystem-flywheel` |
| "Build a GTM strategy for world model tech" | Multi-surface GTM + vertical sequencing + competitive playbook | `world-model-go-to-market` |

You can also just describe a product operations question naturally.

## What's Pre-Loaded

### Context (company research)
- **Company**: intel, hiring signals, investor thesis (~$1.23B raised total, ~50-60 employees in mid-2026)
- **Products**: Marble app (1.1 / 1.1 Plus, with Chisel editing and Marble Studio), World API, RTFM (real-time frame model)
- **Competitive**: landscape overview, Project Genie deep-dive, Runway, Odyssey, NVIDIA Cosmos, Decart
- **Founders**: Fei-Fei Li, Ben Mildenhall, Justin Johnson, Christoph Lassner (quotes, vision, backgrounds)
- **Verticals**: gaming, robotics, architecture, film/VFX
- **Signals**: auto-collected from GitHub (WL repos + competitors) and Hacker News (45+ stories)

### Older Materials (outputs from prior runs)
- `applied/cross-product/product-vision-roadmap.md`

## Skills

### World Labs-Specific (4)

| Skill | What It Produces |
|---|---|
| `spatial-ai-product-strategy` | Product roadmap across all WL surfaces (Marble, API, RTFM) |
| `world-model-go-to-market` | GTM strategy for world model technology |
| `real-time-persistent-convergence` | How RTFM + Marble compose into products, API, pricing |
| `api-ecosystem-flywheel` | Developer activation funnel + SDK roadmap + community growth |

### General Product (19, from pm-playbook)

| Skill | What It Produces |
|---|---|
| `competitive-response` | Threat matrix + moat audit + response playbook |
| `measuring-product-market-fit` | PMF scorecard + pivot/persevere recommendation |
| `product-portfolio-strategy` | Portfolio map + investment allocation |
| `feature-prioritization` | Weighted scoring matrix + sequenced roadmap |
| `north-star-metrics` | Metric tree + leading/lagging indicators |
| `research-to-product-pipeline` | Research-to-product transfer framework |
| `zero-to-one-product-launch` | Launch checklist + go-to-market strategy |
| `writing-prds-for-ai` | PRD template with AI-specific eval criteria |
| `pricing-and-monetization` | Pricing model + willingness-to-pay analysis |
| `customer-discovery` | Interview guide + synthesis + discovery report |
| `user-segmentation` | Segment profiles + prioritization matrix |
| `user-onboarding-optimization` | Onboarding audit + activation metrics |
| `ecosystem-health` | Ecosystem scorecard + growth levers |
| `developer-experience-audit` | Friction scorecard + DX recommendations |
| `api-design-review` | Per-endpoint assessment + recommendations |
| `partnership-evaluation` | Partner scorecards + deal structure |
| `stakeholder-alignment` | Owner alignment + communication plan |
| `platform-vs-application` | Build/buy/partner framework |
| `vertical-market-assessment` | TAM/SAM/SOM + entry strategy |

## Keeping It Fresh

Signal collectors auto-pull competitive intelligence from GitHub, Hacker News, Reddit, and news sources into `context/signals/`.

```bash
# Refresh signals (HN works with no API keys)
cd pm-playbook && python3 -m collectors.run --config ../signals.yaml
```

For full collector coverage, copy `.env.example` to `.env` and add free API keys for GitHub, Reddit, and NewsAPI. Skills auto-check signal freshness and prompt you to refresh when data is older than 7 days.

## Architecture

```
wl-product-playbook/
├── .claude/skills/        ← 23 skills (auto-discovered by Claude Code)
├── pm-playbook/          ← Git submodule (reusable PM framework)
├── skills/                ← 4 World Labs-specific skills
├── context/               ← Company knowledge base + signals
├── signals.yaml           ← What to track (repos, keywords, competitors)
└── applied/               ← Outputs from skill runs
```

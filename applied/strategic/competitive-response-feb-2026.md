# Competitive Response Playbook: February 2026

> Author: Ashka Stephen | [PUBLIC]. All data from publicly available sources unless noted. Evidence tagged per convention.
> Generated 2026-02-06. Point-in-time snapshot: written the day of the Waymo/Genie announcement, before the $1B round closed on 2026-02-18. Figures reflect that date.
>
> Naming note: "Genie 3" is the Google DeepMind research model (Aug 2025). "Project Genie" is the consumer product built on it (launched 2026-01-29 to Google AI Ultra subscribers at $250/mo). This document uses "Genie 3" as shorthand for Google's world-model effort; references below to the $250/mo subscription, ephemerality, and the absence of an API, export, or persistence describe the Project Genie product surface as of early 2026.

## Executive Summary

World Labs faces an inflection point this week. Google DeepMind's Genie 3 is moving from consumer demo to infrastructure: it is being embedded across Alphabet's vertical products, starting with Waymo's autonomous driving simulator (announced 2026-02-06). This is the clearest signal yet that Google is building a world model ecosystem, not only a product. World Labs is well positioned to respond. The company shipped RTFM (Real-Time Frame Model) as a research preview in October 2025, months before Genie's consumer launch and months before Waymo validated world models for production. World Labs already had real-time generation capability when Google announced theirs. Combined with Marble (persistent, exportable, editable 3D worlds) and the World API (developer access), WL has the most complete platform in the space. The competitive window is narrowing, and World Labs' positioning has never been stronger. The top three actions for this week:

1. **Ship the narrative.** Publicly frame the RTFM + Marble combination as "the only platform offering both real-time exploration and production-grade 3D export." No competitor can claim both. Emphasize that WL had real-time capability before Google shipped Genie 3 to consumers.
2. **Accelerate World API developer adoption.** Every developer who builds on the World API before Genie gets a developer tier becomes a switching cost. The API is the durable moat; the model alone is replicable.
3. **Deepen the NVIDIA partnership.** Waymo's use of Genie 3 for AV simulation signals that Google is competing for the robotics/AV vertical. World Labs' existing Isaac Sim integration needs to become deeper and more public before NVIDIA's loyalties split.

---

## Step 1: Competitive Landscape Map

### Direct Competitors

Companies building world models that generate 3D environments, targeting the same core jobs-to-be-done: spatial content creation, interactive 3D generation, and world simulation.

| Company | Product | Target User | Funding/Resources | Growth Trajectory |
|---|---|---|---|---|
| **Google DeepMind** | Genie 3 (research) / Project Genie (consumer) | Consumers (AI Ultra subscribers, $250/mo) | Google-scale (functionally unlimited) | High: real-time generation, expanding into Alphabet verticals via Waymo [PUBLIC] |
| **Waymo** (Alphabet) | Waymo World Model | Internal AV engineering team | Waymo's budget + DeepMind partnership | New entrant (2026-02-06). Not a product for sale. AV-only. [PUBLIC] |
| **Runway** | GWM-1 (General World Models) | Creative professionals, filmmakers | ~$1.5B+ raised, strong brand | Medium: pivoting from video generation to world models [PUBLIC] |
| **Odyssey** | Explorer | Storytellers, narrative creators | Earlier stage | Medium: focused on causal world models for entertainment [PUBLIC] |
| **Decart** | Oasis / Lucy 2.0 | Gaming developers | Earlier stage | Medium: real-time video transformation for gaming [PUBLIC] |

### Adjacent Entrants

Companies in neighboring categories whose products could expand into world generation.

| Company | Product | Current Focus | World Generation Overlap |
|---|---|---|---|
| **NVIDIA** | Cosmos (open-source) | Robotics and AV foundation models | Could add generation capability that undercuts WL's robotics vertical [PUBLIC] |
| **Luma AI** | Dream Machine / Genie | NeRF-based 3D generation | Object-level, not full worlds. Could scale up. [PUBLIC] |
| **Unity** | Muse / AI tools | AI-assisted content creation in-engine | Could build world generation directly into the game engine [PUBLIC] |
| **Epic Games** | Unreal + AI | AI tools for Unreal Engine | Deepest creative tool ecosystem; could integrate generative models [PUBLIC] |
| **Roblox** | AI generation tools | User-generated content | Massive creator base; AI generation could reduce need for external tools [PUBLIC] |

### Asymmetric Threats

Non-obvious players that could disrupt World Labs from an unexpected angle.

| Entity | Threat Vector | Current Status |
|---|---|---|
| **AMI Labs / Meta FAIR (LeCun)** | JEPA architecture for world models | Pre-product, theoretical. If JEPA works, it could leapfrog current autoregressive approaches. [PUBLIC] |
| **Open-source community** | Open-source world model (e.g., from academic lab) | Fragmented today, but a strong open model + community could erode WL's technical moat [PUBLIC] |
| **Apple** | Vision Pro + on-device generation | No world model announced, but Apple has the device ecosystem and a history of surprise vertical integration [ILLUSTRATIVE] |

---

## Step 2: Threat Classification Matrix

Each competitor rated 1-5 across four dimensions. Sum = Threat Score (max 20).

| Competitor | Overlap | Momentum | Capability | Trajectory | Score | Classification |
|---|---|---|---|---|---|---|
| **Google DeepMind (Genie 3)** | 4 | 5 | 5 | 5 | **19** | **Critical** |
| **Waymo World Model** | 2 | 4 | 5 | 3 | **14** | **Serious** |
| **Runway (GWM-1)** | 3 | 3 | 4 | 4 | **14** | **Serious** |
| **NVIDIA (Cosmos)** | 3 | 3 | 5 | 3 | **14** | **Serious** |
| **Decart (Oasis/Lucy)** | 3 | 2 | 3 | 3 | **11** | **Serious** |
| **Odyssey (Explorer)** | 2 | 2 | 3 | 3 | **10** | **Monitor** |
| **Luma AI** | 2 | 2 | 3 | 2 | **9** | **Monitor** |
| **Unity** | 2 | 2 | 4 | 2 | **10** | **Monitor** |
| **Epic Games** | 2 | 2 | 4 | 2 | **10** | **Monitor** |
| **AMI Labs / Meta FAIR** | 2 | 1 | 4 | 3 | **10** | **Monitor** |
| **Roblox** | 1 | 2 | 3 | 2 | **8** | **Monitor** |

### Rationale for Key Scores

**Google DeepMind (19: Critical)**
- Overlap (4): Genie 3 generates interactive 3D environments from images, same core job. Loses 1 point because the Project Genie product has no API, no persistence, and no export, a fundamentally different product surface today. [PUBLIC]
- Momentum (5): AI Ultra launch (Jan 29, 2026), 20-24fps real-time generation, and now Waymo adoption prove this is a shipping product with production traction. [PUBLIC]
- Capability (5): Google-scale compute, DeepMind research depth, and Waymo's 200 million miles of autonomous data. Unmatched resource advantage. [PUBLIC]
- Trajectory (5): Waymo's adoption of Genie 3 is the strongest trajectory signal: Google's world model is becoming infrastructure that powers vertical products across Alphabet. If this pattern repeats, Genie 3 becomes a foundation layer rather than a consumer toy. [PUBLIC]

**Waymo World Model (14: Serious)**
- Overlap (2): AV-only simulation tool. Not a product for sale. Does not compete for the same customers. But it validates the Genie 3 ecosystem and demonstrates world models in a mission-critical production environment. [PUBLIC]
- Momentum (4): 200 million fully autonomous miles, DeepMind partnership, camera + lidar output. The most sophisticated deployment of a world model in production. [PUBLIC]
- Capability (5): Waymo + DeepMind combined is the strongest technical team working on world models, with the largest proprietary driving dataset. [PUBLIC]
- Trajectory (3): Narrowly scoped to AV. Not converging toward World Labs' space. But the pattern it sets (Genie 3 as vertical infrastructure) is the real threat. [PUBLIC]

**Runway (14: Serious)**
- Overlap (3): GWM-1 targets world generation but comes from a video-first approach, not 3D-native. If they ship a developer API with their existing creative user base, they capture the creator market. [PUBLIC]
- Momentum (3): Strong brand among creative professionals. Established revenue and user base from video generation. [PUBLIC]
- Capability (4): Deep video generation expertise, well-funded, experienced team. [PUBLIC]
- Trajectory (4): Explicitly pivoting toward world models. Their roadmap is converging with WL's space. [PUBLIC]

**NVIDIA Cosmos (14: Serious)**
- Overlap (3): Open-source robotics/AV foundation models overlap with WL's robotics vertical. [PUBLIC]
- Momentum (3): Open-source adoption growing. Part of NVIDIA's Omniverse/Isaac ecosystem. [PUBLIC]
- Capability (5): NVIDIA has the compute, the developer ecosystem, and the hardware supply chain. If they decide to add generation, they have every resource to do it. [PUBLIC]
- Trajectory (3): Currently a partner (WL integrates with Isaac Sim), not a competitor. But the Waymo/Genie 3 pattern raises the question: does NVIDIA build its own generation layer? [PUBLIC]

---

## Step 3: Moat Audit (7 Powers)

| Power | Present? | Strength (1-5) | Evidence | Withstands Top Threats? |
|---|---|---|---|---|
| **Scale Economies** | Weak | 2 | ~50-60 employees; ~$1.23B raised in total (the $230M Series A plus the $1B round that closed 2026-02-18, investors including Autodesk, Andreessen Horowitz, NVIDIA, and AMD). Even so, Google has orders of magnitude more compute and data. WL cannot win on raw scale. [PUBLIC] | No. Google's scale advantage is structural. |
| **Network Effects** | Emerging | 2 | Developer ecosystem is nascent (25 GitHub stars across WL repos, 4 official examples, SparkJS as ecosystem infrastructure). Network effects require a critical mass of developers building on the API. Not there yet. [PUBLIC, SIGNAL] | Not yet. Must be built in the next 6-12 months. |
| **Counter-Positioning** | **Yes** | **4** | World Labs is building a developer platform (API + export + persistence + editing). Project Genie is a consumer experience (no API, no export, no persistence). Google would have to cannibalize its own consumer-first approach to match WL's developer platform. Waymo building on Genie 3 reinforces the "internal tool" pattern and leaves the "developer platform" lane open. Incumbents are unlikely to open their world models as general-purpose APIs because it would require a fundamentally different business model. [PUBLIC] | Yes, against Google. This is WL's strongest power today. |
| **Switching Costs** | Emerging | 2 | Developers who build on World API incur switching costs (API integration, export pipeline, SPZ/GLB format adoption). But the developer base is too small for this to be material yet. [PUBLIC] | Will strengthen as developer base grows. Critical to invest in now. |
| **Branding** | Moderate | 3 | Fei-Fei Li is the most recognized AI researcher in the world (ImageNet creator, Queen Elizabeth Prize, TIME100). Her association gives WL credibility that no startup competitor can match. But the brand is "research credibility," not yet "developer trust." [PUBLIC] | Partially. Brand helps with enterprise and media narrative but does not defend against Google's brand. |
| **Cornered Resource** | Moderate | 3 | Founding team: Fei-Fei Li (ImageNet creator, spatial intelligence thesis), Ben Mildenhall (NeRF inventor), Justin Johnson (CS231N, deep learning architecture), Christoph Lassner (Pulsar, rendering pipeline). This team uniquely combines academic prestige with production rendering expertise. [PUBLIC] | Partially. Google can hire top talent but cannot replicate this specific founding team's credibility and vision coherence. |
| **Process Power** | Emerging | 3 | World Labs shipped RTFM (Oct 2025), Marble App (Nov 2025), and World API (Jan 2026): three products in four months with a team in the low dozens. This pace is remarkable for a team this size and suggests strong execution culture. The fact that RTFM shipped months before Google's consumer Genie launch (Jan 29, 2026) demonstrates an ability to anticipate market needs, not only react to them. [PUBLIC] | Strengthening. The shipping cadence is evidence, but Process Power requires sustained organizational capability over multiple cycles. |

### Moat Summary

World Labs' strongest power today is **Counter-Positioning**: the company is building a developer platform while competitors are building consumer experiences or internal tools. Google would have to fundamentally change its approach to compete on WL's terms. The second-strongest powers are **Branding** (Fei-Fei Li), **Cornered Resource** (the founding team's unique combination), and an emerging **Process Power** demonstrated by the shipping cadence.

The shipping timeline deserves emphasis: World Labs had real-time generation (RTFM, Oct 2025), a consumer product (Marble, Nov 2025), and a developer API (World API, Jan 2026) all live before Project Genie launched to consumers on January 29, 2026. World Labs was already positioned in the space when Google arrived, well ahead of any catch-up dynamic.

The critical gap is **Network Effects** and **Switching Costs**. Both depend on developer adoption of the World API. If WL can reach a critical mass of developers building production applications on the API in the next 6-12 months, these powers become real. If not, Counter-Positioning alone will not hold once Google opens Genie 3 to developers.

### Buildability Assessment (next 12 months)

| Power | Buildable? | What It Takes |
|---|---|---|
| Network Effects | Yes, with focus | Ship SDKs, cookbooks, and community programs. Target 100+ developers with production integrations by end of year. |
| Switching Costs | Yes, as a byproduct | Every developer who integrates SPZ/GLB export into their pipeline creates switching costs. Deepen the export pipeline. |
| Scale Economies | No | Cannot out-scale Google. Do not try. |

---

## Step 4: Response Strategy per Competitor

### Google DeepMind / Genie 3: DIFFERENTIATE

**Classification:** Critical (19/20)
**Strategy:** Differentiate

**Justification:** Genie 3 is the only existential threat. Head-to-head competition with Google on real-time generation is a losing game (they have more compute, more data, and consumer distribution). World Labs' Counter-Positioning moat points to a different answer: double down on the dimensions Google does not offer and structurally will not offer in the near term, namely a developer API, persistent worlds, exportable 3D assets, editing, and programmatic control.

RTFM strengthens this calculus. World Labs shipped real-time generation in October 2025, months before Project Genie's consumer launch. This means WL can credibly claim real-time capability (RTFM) while also offering what Genie cannot (Marble's persistence, editing, and export). The narrative writes itself: World Labs was here first with real-time, and it also has persistence, editing, export, and an API that Google does not.

**Immediate actions:**
1. Publicly position RTFM + Marble as "both real-time exploration AND production-grade 3D" in the next blog post, launch materials, and developer communications. Emphasize the October 2025 RTFM launch date to establish the timeline.
2. Accelerate the RTFM-to-Marble pipeline: let developers use RTFM for fast interactive preview, then "render" their chosen view into a persistent, exportable Marble world. This workflow is unique to World Labs.
3. Monitor for the critical tripwire: Google announcing a Genie 3 developer API. If this happens, the competitive dynamics change entirely and WL must accelerate SDK and ecosystem investments aggressively.

### Waymo World Model: IGNORE (strategically)

**Classification:** Serious (14/20)
**Strategy:** Ignore (deliberate)

**Justification:** Waymo runs an internal tool for autonomous driving simulation rather than selling world generation. World Labs does not compete for Waymo's customers because Waymo's customers are its own engineering teams. The direct competitive threat is low.

However, the strategic signal matters enormously: Genie 3 is becoming infrastructure within Alphabet. This strengthens the case for the Differentiate strategy against Google (Step 4a above) and the NVIDIA partnership acceleration (Step 4d below). The correct response to Waymo is to ensure World Labs' own platform story is more compelling than "use Genie 3 and fine-tune it for your vertical," while staying out of AV simulation itself.

**Immediate actions:**
1. Use Waymo's announcement in positioning materials: "Google's world model is being used internally. Ours is available to everyone via API."
2. Do not pursue autonomous driving simulation as a vertical. This is Google/Waymo territory with proprietary data advantages World Labs cannot match. Concede this segment.
3. Track whether other Alphabet companies or external partners adopt Genie 3. If this becomes a pattern (more than Waymo), escalate the Genie 3 threat from Differentiate to Leapfrog.

### Runway (GWM-1): DIFFERENTIATE

**Classification:** Serious (14/20)
**Strategy:** Differentiate

**Justification:** Runway's strength is brand recognition among creative professionals and their existing user base from video generation tools. If Runway ships a world generation API with their creative tools ecosystem, they will likely capture a segment of the creator market. But Runway comes from video, not 3D-native generation. Their approach (video-first world models) produces different outputs than WL's approach (3D-native with Gaussian splats and mesh export).

**Immediate actions:**
1. Differentiate on 3D-native output: WL generates actual 3D geometry (exportable as SPZ, GLB) while Runway generates video-derived representations. For any downstream use case requiring 3D assets (game engines, robotics, architecture, VFX pipelines), WL's output is structurally superior.
2. Target the developer segment that Runway does not serve. Runway's users are creative professionals who work in GUI tools. WL's API serves developers building applications. These are different segments with different needs.
3. Monitor Runway's API plans. If Runway ships a developer API, reassess whether the creative professional segment is worth competing for directly.

### NVIDIA (Cosmos): PARTNER (not compete)

**Classification:** Serious (14/20)
**Strategy:** Differentiate via partnership

**Justification:** NVIDIA is more partner than competitor today. World Labs already integrates with Isaac Sim, and NVIDIA's Cosmos is focused on open-source robotics/AV foundations, not generation-as-a-service. But Waymo's use of Genie 3 raises a strategic question: could NVIDIA eventually build or integrate a generation layer into its own platform, cutting World Labs out of the robotics vertical?

The correct response is to deepen the partnership to the point where NVIDIA sees WL as the generation layer for its ecosystem, not a competitor to displace.

**Immediate actions:**
1. Propose a joint announcement or case study with NVIDIA showcasing World API + Isaac Sim integration. Make the partnership visible and public.
2. Explore whether WL can be a generation backend for NVIDIA Omniverse more broadly (not just Isaac Sim).
3. Track NVIDIA's relationship with Google/Waymo. NVIDIA supplies hardware to both WL and Google. Their incentive is to support both, but if Google's ecosystem becomes dominant, NVIDIA may deprioritize WL.

### Decart (Oasis/Lucy 2.0): IGNORE

**Classification:** Serious (11/20)
**Strategy:** Ignore

**Justification:** Decart is gaming-focused with real-time video transformation. RTFM neutralizes their speed advantage. Decart lacks persistence, export, and a developer API. Their target market (gaming) overlaps with WL but they are not winning the segment. Do not allocate resources to respond.

**Immediate actions:**
1. No specific response needed.
2. Monitor if they raise a significant round or announce an API.

---

## Step 5: Surprise Entrant Scenarios

| # | Scenario | Probability | Timeline | Tripwire Signal | Pre-Committed Response |
|---|---|---|---|---|---|
| 1 | **Google opens Genie 3 as a developer API** | Medium-High | 6-12 months | Google blog post or developer documentation for Genie API access | Escalate response to "Leapfrog." Immediately ship batch generation API, webhook support, and TypeScript SDK. Compete on DX quality and export pipeline depth. Google's API will likely lack export and persistence initially. |
| 2 | **NVIDIA adds generation capability to Cosmos/Omniverse** | Medium | 12-18 months | NVIDIA GTC announcement of native generation features, or acquisition of a generation startup | Deepen partnership proactively (Step 4d). If NVIDIA builds, position WL as premium quality layer on top of Cosmos base generation. |
| 3 | **Open-source world model reaches production quality** | Low-Medium | 12-24 months | Academic paper with open model weights that matches WL quality on standard benchmarks, achieving significant GitHub traction (1,000+ stars in first month) | Shift value proposition from model quality to platform value (API, export, ecosystem, enterprise support). The model is a commodity; the platform is the moat. |
| 4 | **Apple integrates world generation into Vision Pro / Reality Composer** | Low | 18-36 months | Apple WWDC announcement of on-device world generation, or acquisition of a spatial AI startup | Target non-Apple platforms and developer workflows. Apple's play would be device-locked; WL's API is platform-agnostic. |

---

## Step 6: Monitoring System

### Weekly

| Signal | Source | What to Watch |
|---|---|---|
| Google AI product updates | Google AI Blog, DeepMind blog, Google developer docs | Any mention of Genie API access, developer tools, or new vertical deployments |
| Competitor product launches | Runway, Decart, Odyssey changelogs and blogs | New features, API announcements, pricing changes |
| Developer ecosystem activity | WL GitHub repos (stars, forks, issues, PRs), SparkJS adoption | Growth rate of developer engagement |
| Community sentiment | Hacker News, Reddit r/MachineLearning, X/Twitter | How developers talk about world generation tools (WL vs competitors) |

### Monthly

| Signal | Source | What to Watch |
|---|---|---|
| Threat Classification update | All sources above | Re-score each competitor's Momentum and Trajectory dimensions |
| NVIDIA partnership health | Internal relationship + public announcements | Joint activities, shared roadmap progress, competing announcements |
| Developer activation metrics | Internal API dashboard | API key signups, first world generated, production integrations |
| Hiring signals | LinkedIn, competitor careers pages | Key hires at competitors (especially ML engineers and developer relations) |

### Quarterly

| Activity | Scope |
|---|---|
| Full Moat Audit re-run | Re-evaluate all 7 Powers with latest data. Has Network Effects strengthened? |
| Response strategy reassignment | Check if any Monitor-tier competitor should be upgraded. Check tripwire signals. |
| Vertical market check | Is any vertical being captured by a competitor? (Especially robotics by NVIDIA/Google.) |

### Recommended Data Sources

| Source | Access | Frequency |
|---|---|---|
| `pm-playbook` signal collectors | Automated (HN, GitHub, Reddit, News) | Weekly refresh via `signals.yaml` |
| Google DeepMind blog | Public | Check weekly |
| Waymo blog | Public | Check monthly |
| Runway changelog | Public | Check weekly |
| NVIDIA developer blog | Public | Check monthly |
| LinkedIn job postings (competitors) | Public | Check monthly |
| Hacker News "world model" mentions | Automated via signal collector | Weekly |

---

## Step 7: Synthesized Playbook

### The Competitive Situation in Plain Language

World Labs is in a race to build the developer platform for 3D world generation before Google turns Genie 3 into one. Today, WL has the only world generation API with persistent, editable, exportable 3D output. Project Genie is faster at consumer-facing real-time generation but produces ephemeral, non-exportable experiences locked behind a $250/month consumer subscription. Waymo's announcement this week shows that Google is moving fast: Genie 3 is being embedded in production systems across Alphabet. World Labs is moving from a position of strength. The company shipped RTFM in October 2025, demonstrating real-time generation capability months before Google launched Project Genie to consumers (January 2026) and months before Waymo validated world models for production AV simulation (February 2026). With RTFM for real-time exploration, Marble for persistent editable exportable worlds, and the World API for developer access, World Labs has the most complete platform in the market. The window for establishing platform dominance is open, and it will not stay open indefinitely.

### Top 3 Immediate Actions (This Week)

**1. Ship the "real-time AND production-grade" narrative**

RTFM + Marble is the strongest positioning World Labs has ever had. No competitor offers both real-time interactive generation and persistent, editable, exportable 3D worlds. The timeline tells a compelling story: WL shipped real-time generation (RTFM, Oct 2025), then a consumer product (Marble, Nov 2025), then a developer API (World API, Jan 2026), all before Project Genie reached consumers and before Waymo validated world models for production use. This needs to be the headline message in every external communication: blog posts, developer docs, social media, and partner conversations. The framing is direct: World Labs built the complete platform while others were still launching demos.

- Owner: Marketing/comms (with PM input on technical accuracy)
- Timeline: This week
- Deliverable: Updated positioning language for website, blog, and developer docs

**2. Accelerate developer adoption of the World API**

Every developer who integrates the World API before Google ships a Genie 3 API becomes a switching cost. The API is the moat. Invest in:
- Python SDK improvements (type hints, automatic polling, asset download helpers)
- A cookbook repository with progressive-complexity recipes (hello-world through production patterns)
- A showcase gallery where developers can display what they have built
- Response time SLA for developer support (Discord, GitHub issues)

- Owner: Developer relations + engineering
- Timeline: Start this week, ongoing
- Deliverable: SDK audit results + cookbook plan + first 3 recipes by end of month

**3. Make the NVIDIA partnership louder and deeper**

Waymo building on Genie 3 means Google is competing for the robotics/AV simulation vertical. World Labs' existing Isaac Sim integration is the counter-move, but it needs to be more visible and more deeply integrated. Propose a joint case study, a co-branded demo at GTC, or a shared developer tutorial. The goal is to make NVIDIA publicly invested in World Labs' success before they have to choose sides.

- Owner: Partnerships/BD
- Timeline: Outreach this week, joint deliverable within 30 days
- Deliverable: Partnership proposal sent to NVIDIA contact

---

### Appendix: Evidence Tags

All data points in this document are tagged:

| Tag | Meaning |
|---|---|
| `[PUBLIC]` | From publicly available information (blogs, docs, press) |
| `[SIGNAL]` | Auto-collected by the pm-playbook signal collectors framework. Freshness: 2026-02-06. |
| `[ILLUSTRATIVE]` | Hypothetical example used to demonstrate methodology |

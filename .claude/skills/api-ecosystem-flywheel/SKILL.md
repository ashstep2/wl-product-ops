---
name: api-ecosystem-flywheel
description: "Help users design and accelerate a developer ecosystem around a spatial AI API — covering developer activation funnels, SDK investment strategy, cookbook/examples architecture, community flywheel design, integration partnerships, and developer content calendars."
version: "1.0.0"
last_updated: "2026-02-06"
---

# API Ecosystem Flywheel

Produce a developer ecosystem growth strategy for a spatial AI API, covering the full journey from first API key to production integration. The output includes a developer activation funnel with conversion benchmarks, SDK investment roadmap, cookbook architecture, community flywheel design, integration partnership playbook, and 12-month developer content calendar — all specific to the challenge of growing an ecosystem from near-zero around a novel technology category.

## Core Principles

1. **The API is the product, and the docs are the front door**
   "The Collison Install — the founders of Stripe would sit with potential users and say 'just try it,' then help them integrate Stripe in real-time during the conversation."
   — *Patrick Collison, CEO of Stripe* ([Founder lore, documented in First Round Review](https://review.firstround.com/on-the-art-of-the-start-lessons-from-y-combinator-legend-paul-buchheit/))

   Stripe's lesson: the activation experience IS the product for developers. If a developer cannot go from "I just heard about this" to "I generated my first world via API" in under 10 minutes, the developer GTM is broken. Documentation is not a support function — it is the primary acquisition channel. Every minute of friction in the first-call experience is a lost developer.

2. **Community is the moat, not code**
   "If code isn't a competitive moat, what is? Community. Your open source community is a developer-driven top-of-funnel activity."
   — *Peter Levine, General Partner at Andreessen Horowitz* ([Open Source: From Community to Commercialization](https://a16z.com/open-source-from-community-to-commercialization/))

   The World API's competitive moat is not the generation model — models improve and competitors ship alternatives. The moat is the ecosystem: cookbook recipes, community tutorials, Stack Overflow answers, third-party integrations, and developers who have invested time learning the API. Every community contribution compounds into switching costs that cannot be replicated by cloning a repository.

3. **Ask your developer — they are the new kingmaker**
   "In a world where software developers have incredible influence and decision-making power, companies win by building the tools and platforms that developers choose."
   — *Jeff Lawson, CEO of Twilio* ([Ask Your Developer](https://www.askyourdeveloper.com/))

   In spatial AI, the decision of which world generation API to build on is made by individual developers, not by procurement committees (at least initially). The developer ecosystem strategy must win the individual developer — through DX quality, documentation, community, and trust — before enterprise deals become possible. Enterprise buyers ask "who else is using this?" and look for a thriving developer ecosystem as social proof.

4. **Come for the tool, stay for the network**
   "The idea is to initially attract users with a single-player tool and then, over time, get them to participate in a network."
   — *Chris Dixon, General Partner at Andreessen Horowitz* ([Come for the Tool, Stay for the Network](https://cdixon.org/2015/01/31/come-for-the-tool-stay-for-the-network))

   Developers come for the API (the tool) and stay for the ecosystem (the network). The "tool" value is: generate 3D worlds programmatically. The "network" value is: cookbook recipes from other developers, SparkJS renderer integrations, community-built plugins for Unity/Unreal/Blender, and showcase galleries that demonstrate what is possible. The ecosystem strategy must invest in both dimensions — a great API with no community is a tool; a great API with a thriving community is a platform.

5. **Developer experience is product quality**
   "Your API is just as much a product as your user-facing product. The time to first successful API call is your time to value."
   — *Suhail Doshi, CEO of Playground AI (formerly CEO of Mixpanel)* ([Twitter/X](https://x.com/saborsh))

   For a developer product, DX IS the product. A world model that generates stunning outputs but requires 47 lines of boilerplate, manual polling, and undocumented error codes will lose to a model that generates good outputs with a three-line SDK call. The ecosystem flywheel starts with DX quality — every friction point in the developer experience is a leak in the activation funnel.

6. **Cookbooks beat documentation for adoption**
   "People don't read docs. They read examples, copy them, modify them, and then read docs when they get stuck."
   — *Engineering culture at Stripe, Twilio, and Vercel* (widely documented pattern)

   Cookbook repositories (like OpenAI Cookbook, Anthropic Cookbook, Vercel Examples) drive more adoption than reference docs. They provide copy-paste starting points that developers modify for their use case. For a novel API like world generation, cookbooks are even more critical — developers literally do not know what to build. Progressive-complexity recipes ("hello world" → "photo to scene" → "batch generation" → "RTFM preview + Marble export") teach developers what is possible while giving them working code.

7. **Open-source the complement, monetize the core**
   "Complements to a product tend to drive demand for it. Smart companies try to commoditize their products' complements."
   — *Joel Spolsky* ([Strategy Letter V](https://www.joelonsoftware.com/2002/06/12/strategy-letter-v/))

   SparkJS (open-source 3DGS renderer) is a complement to the World API (paid generation). Making the renderer free and excellent drives demand for the paid generation API. The ecosystem strategy should continuously invest in SparkJS quality, documentation, and community — every developer who adopts SparkJS for rendering is one step closer to paying for generation.

## Instructions

### Step 1: Map the Developer Activation Funnel

Produce a **Developer Activation Funnel** with conversion benchmarks at each stage.

- Read `context/products/world-api.md` for current API surface, SDK status, and known friction points
- Read `context/ecosystem/sparkjs.md` for the open-source renderer's adoption status
- Define the funnel stages:

| Stage | Definition | Current State | Target | Bottleneck |
|---|---|---|---|---|
| **Awareness** | Developer hears about World API | ? | | |
| **Exploration** | Visits docs, reads quickstart | ? | | |
| **First key** | Creates API key | ? | | |
| **First call** | Makes a successful API call | ? | | |
| **First world** | Generates a complete world | ? | | |
| **First integration** | Uses output in their own project | ? | | |
| **Production** | Ships an app built on World API | ? | | |
| **Advocacy** | Writes about it, shares with others | ? | | |

For each stage-to-stage transition, estimate the current conversion rate (use `context/signals/` GitHub data as proxy if direct data is unavailable) and identify the primary friction point.

- Time the current experience: starting from the API docs page, how many minutes to a successful first world generation? Document every step.
- **Output:** Developer Activation Funnel with stage definitions, conversion estimates, friction points, and target improvements.

### Step 2: Design the SDK Investment Roadmap

Produce an **SDK Investment Roadmap** prioritized by vertical demand and developer reach.

| SDK | Target Developers | Vertical Alignment | Complexity | Priority |
|---|---|---|---|---|
| **Python** (exists, minimal) | ML engineers, robotics, data science | Robotics & Simulation | Low (improve existing) | P0 |
| **TypeScript/Node** | Web developers, creative tool builders | Gaming & Immersive, General | Medium | P1 |
| **Unity Plugin** | Game studios, interactive media | Gaming & Immersive | High | P2 |
| **Unreal Plugin** | AAA game studios, film/VFX | Film & VFX, Gaming | High | P3 |
| **Blender Add-on** | 3D artists, architects | Architecture & Design | Medium | P3 |

For each SDK, define:
- Minimum viable feature set (what must it do at launch?)
- Full-featured scope (what does the 1.0 look like?)
- Maintenance model (internal team? community-maintained? contractor?)
- Success metric (downloads/installs in first 90 days)

For the Python SDK specifically (P0), audit the current state and propose immediate improvements:
- Does it wrap all API endpoints?
- Does it handle polling automatically?
- Does it include asset download helpers?
- Does it have type hints and docstrings?
- Is there a `pip install worldlabs` that works?

**Output:** SDK Investment Roadmap with prioritization, scope definitions, and Python SDK audit.

### Step 3: Architect the Cookbook Repository

Produce a **Cookbook Architecture** with progressive-complexity recipes.

Design a recipe progression that teaches developers what is possible while giving them working code:

**Tier 1: Getting Started (first 10 minutes)**
- `01-hello-world.py` — Generate a world from a text prompt
- `02-image-to-world.py` — Generate a world from a photo
- `03-view-in-browser.html` — Display a generated world using SparkJS

**Tier 2: Real Use Cases (first hour)**
- `04-batch-generation.py` — Generate 10 worlds from a CSV of prompts
- `05-video-to-world.py` — Generate a world from a video clip
- `06-multi-angle.py` — Generate a world from multiple photos
- `07-export-to-glb.py` — Generate and export as mesh for use in game engines

**Tier 3: Production Patterns (first day)**
- `08-webhook-listener.py` — Set up async generation with webhook callbacks (if available)
- `09-unity-integration/` — Load generated worlds into Unity
- `10-robotics-sim.py` — Generate diverse training environments for robotics
- `11-architecture-walkthrough/` — Generate and display an architecture visualization

**Tier 4: Advanced (after familiarity)**
- `12-rtfm-preview-marble-export/` — Use RTFM for real-time exploration, export best view with Marble (when RTFM API is available)
- `13-custom-pipeline.py` — Build a generation pipeline with quality routing
- `14-community-gallery/` — Build a gallery site displaying generated worlds

For each recipe, define: title, one-line description, difficulty level, estimated time, and which vertical it targets.

**Output:** Cookbook Architecture with recipe list, progression logic, and recipe template.

### Step 4: Design the Community Flywheel

Produce a **Community Flywheel Map** showing how community activities compound into ecosystem growth.

Define the flywheel stages and their connections:

```
Cookbook recipes → Developers build projects
  → Showcase gallery features best projects
    → Social sharing attracts new developers
      → New developers start with cookbook recipes
        → Some contribute back recipes/improvements
          → Richer cookbook attracts more developers
```

For each flywheel element, define:

**Showcase Gallery:**
- Where does it live? (gallery.worldlabs.ai? section of docs?)
- Submission process: developer submits URL + description
- Curation: team-curated weekly picks vs. community-voted
- Content: screenshot/video + description + code link + "built with World API" badge
- Success metric: submissions per week, gallery page views

**Discord / Community Hub:**
- Channel architecture: #getting-started, #showcase, #bugs, #feature-requests, #vertical-specific channels (gaming, robotics, architecture, film)
- Moderation model: team + community moderators
- Response time SLA: team responds to #bugs within 24 hours
- Success metric: weekly active members, questions answered

**Developer Spotlight Program:**
- Monthly spotlight: interview with a developer who built something notable
- Blog post + social media promotion
- Incentive: featured on docs homepage, priority access to new features
- Success metric: spotlight applications per month

**Hackathon Calendar:**
- Frequency: quarterly themed hackathons
- Themes aligned with verticals: "Build a game level generator" (Q1), "Robotics training data challenge" (Q2), etc.
- Prizes: API credits, featured in showcase, direct access to WL team
- Success metric: submissions per hackathon, post-hackathon retention

**Output:** Community Flywheel Map with element definitions, success metrics, and investment requirements.

### Step 5: Build the Integration Partnership Playbook

Produce an **Integration Partnership Playbook** prioritizing which platforms to integrate with first.

- Read `context/verticals/` for vertical-specific platform dependencies
- Read `context/competitive/` for competitor integration moves

| Platform | Vertical | Integration Type | Co-Marketing Value | Priority |
|---|---|---|---|---|
| **NVIDIA Isaac Sim** | Robotics | Native world generation in sim | Very high (Jensen partnership) | P0 |
| **Unity** | Gaming | Asset import plugin + generation panel | High | P1 |
| **Unreal Engine** | Gaming, Film | Asset import plugin + generation panel | High | P1 |
| **Blender** | Architecture, Film | Add-on for generation + import | Medium | P2 |
| **Three.js / SparkJS** | Web | Already exists (SparkJS). Deepen. | Medium | P0 |
| **Figma** | Architecture, Design | Plugin for 3D scene generation from 2D designs | Medium | P3 |

For each integration, document:
- What the integration looks like technically (plugin, API bridge, file format support)
- What the co-marketing opportunity is (joint blog post, conference demo, case study)
- Who the internal champion is at the partner company (if known)
- What the deal structure should be (free integration, revenue share, co-development)

**Output:** Integration Partnership Playbook with prioritized partner list, integration specifications, and co-marketing plans.

### Step 6: Create the Developer Content Calendar

Produce a **12-Month Developer Content Calendar** with specific content pieces.

| Month | Content Type | Title/Topic | Audience | Channel |
|---|---|---|---|---|
| M1 | Blog + code | "Building your first 3D world in 5 minutes" | New developers | Blog, Twitter, HN |
| M1 | Changelog | Weekly changelog launch | All developers | Blog, Discord |
| M2 | Tutorial | "Photo to explorable scene: a complete walkthrough" | Web developers | Blog, YouTube |
| M2 | Spotlight | First developer spotlight | Community | Blog, social |
| M3 | Blog | "How [company X] uses World API for robotics training" | Robotics vertical | Blog, LinkedIn |
| M3 | Hackathon | Q1 hackathon: "Generate a game level" | Gaming developers | Discord, social |
| M4 | Tutorial | "Integrating World API with Unity" | Game developers | Blog, YouTube |
| M5 | Blog | "RTFM + Marble: real-time preview to production export" | All developers | Blog, HN |
| M6 | Conference | Talk at [relevant conference] | Broad developer | Conference, YouTube |
| M6 | Hackathon | Q2 hackathon: "Robotics sim environments" | Robotics developers | Discord, social |
| M7-12 | ... | Continue pattern: blog/tutorial/spotlight/hackathon/conference per quarter | | |

Content principles:
- Every blog post ships with working code (no "announcing" without "try it")
- Changelogs are weekly and public (builds trust, shows velocity)
- Conference talks target 2-3 tier-1 events per year (GTC, GDC, SIGGRAPH, Strange Loop)
- Video content goes to YouTube (searchable, long-tail discovery)

**Output:** 12-Month Developer Content Calendar with content types, topics, audiences, and channels.

## Diagnostic Questions

1. **What is the current time from API docs page to first generated world?** If this is over 15 minutes, it is the number one thing to fix before any ecosystem investment. Measure it by actually doing it, not by asking the team.

2. **How many developers have API keys? How many made a call in the last 30 days?** The gap between these numbers is the activation rate. If fewer than 30% of key holders are active, the onboarding experience is broken.

3. **What are the top 3 questions in Discord/support channels?** These reveal the biggest DX gaps. If the same question is asked repeatedly, it belongs in the quickstart guide, not in Discord.

4. **Does `pip install worldlabs` work today?** If not, this is the first thing to ship. Developers expect a single install command.

5. **How many third-party projects are built on World API?** If the answer is under 10, the cookbook and showcase gallery are the highest-leverage investments. Developers need proof that others are building.

6. **Is the open-source renderer reducing friction for API adoption?** Track whether developers who use SparkJS to display worlds convert to API customers at a higher rate. It's ecosystem infrastructure, not a product — measure it by how well it supports the API funnel.

## Common Mistakes

1. **Building SDKs in-house when the community could contribute** — The Python SDK and TypeScript SDK should be open-source from day one. Community PRs accelerate development and create ownership. Internal-only SDKs become bottlenecks because the team cannot keep them in sync with API changes.

2. **Treating documentation as a cost center** — Docs are the primary acquisition channel for a developer product. They should be maintained with the same rigor as the API codebase: versioned, tested, reviewed, and deployed continuously. Stale docs are worse than no docs.

3. **Launching a hackathon without a showcase gallery** — Hackathon outputs need a place to live after the event. Without a gallery, the projects disappear and the community investment is wasted. Build the gallery before the first hackathon.

4. **Investing in enterprise partnerships before developer activation is working** — Enterprise buyers want to see a thriving ecosystem before committing. If the activation funnel is broken (most developers who get an API key never generate a world), no partnership will produce results.

5. **Measuring ecosystem health by API call volume alone** — Volume can come from a single large customer. Ecosystem health is measured by breadth: number of unique developers with production integrations, number of community-contributed recipes, number of third-party tools. Breadth is more defensible than depth.

6. **Ignoring the open-source renderer** — The renderer is ecosystem infrastructure that reduces friction for displaying generated worlds. Under-investing in it while pushing the paid API is counterproductive — if displaying worlds is hard, developers won't generate them.

## Context Integration

| Context Directory | Used In | Purpose |
|---|---|---|
| `context/products/world-api.md` | Step 1 (Funnel), Step 2 (SDK Audit), Step 4 (Pricing) | Current API surface, SDK status, pricing, and known DX gaps |
| `context/ecosystem/sparkjs.md` | Step 1 (Funnel), Step 4 (Flywheel) | SparkJS adoption as leading indicator of ecosystem health |
| `context/products/rtfm.md` | Step 3 (Cookbook), Step 6 (Calendar) | RTFM integration recipes and content opportunities |
| `context/verticals/` | Step 2 (SDK priorities), Step 5 (Partnerships) | Vertical-specific platform dependencies drive SDK and partnership priority |
| `context/competitive/` | Step 5 (Partnerships), Step 6 (Calendar) | Competitor ecosystem moves create urgency for specific integrations |
| `context/signals/` | Step 1 (Funnel), Step 4 (Community) | GitHub stars, HN discussions, and community sentiment as ecosystem health proxies |
| `context/company/` | Step 2 (SDK), Step 4 (Community) | Team size (~41) constrains how many SDKs and community programs can be staffed |

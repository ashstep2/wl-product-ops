---
name: spatial-ai-product-strategy
description: "Help users develop product strategy for spatial AI products — navigating the unique challenges of 3D world generation, multi-modal input pipelines, export ecosystems, and the transition from research-grade models to production developer tools."
---

# Spatial AI Product Strategy

Produces a comprehensive product strategy for a spatial AI company, covering capability mapping, platform positioning, portfolio design, input/output prioritization, ecosystem flywheel construction, and competitive framing — grounded in the reality that spatial AI is a new category requiring new strategic frameworks, not adaptations of 2D AI playbooks.

## Core Principles

1. **Spatial intelligence is a new category, not an incremental advance**
   "Yet they remain wordsmiths in the dark; eloquent but inexperienced, knowledgeable but ungrounded."
   — *Fei-Fei Li, CEO of World Labs* ([From Words to Worlds: Spatial Intelligence is AI's Next Frontier](https://drfeifei.substack.com/p/from-words-to-worlds-spatial-intelligence))

   Li's characterization of today's LLMs reveals the foundational insight for spatial AI strategy: language models lack grounding in physical reality. This means spatial AI products cannot be positioned as "better AI" — they must be positioned as a fundamentally different kind of intelligence. Strategy must account for category creation, not just category competition. Every product decision should widen the gap between "eloquent but ungrounded" and "spatially aware."

2. **The product must preserve human creative control**
   "You don't want the machine to just take the wheel and pull all that creativity away from you."
   — *Justin Johnson, Co-Founder of World Labs* ([TechCrunch, Nov 2025](https://techcrunch.com/2025/11/12/fei-fei-lis-world-labs-speeds-up-the-world-model-race-with-marble-its-first-commercial-product/))

   This principle shapes every interaction model decision. Spatial AI products that fully automate world creation will hit a ceiling — professional users (game designers, architects, filmmakers) need to steer, iterate, and refine. The product strategy must balance generation power with granular user control. Multi-modal input (text, image, multi-angle, video) is not just a feature — it is the mechanism for preserving creative agency. Each modality gives users a different lever of control.

3. **Spatial AI requires understanding, not just rendering, the physical world**
   "The ability to understand, to reason, to interact with and to navigate the real 3D, 4D physical world is the foundation."
   — *Fei-Fei Li, CEO of World Labs* ([PYMNTS Interview, Jan 2026](https://www.pymnts.com/artificial-intelligence-2/2026/fei-fei-li-says-ai-progress-now-depends-on-physical-context/))

   This separates spatial AI from traditional 3D rendering or procedural generation. The strategic implication is that product value comes from the model's understanding of spatial relationships, physics, and geometry — not just visual fidelity. Competitive moats should be built around spatial reasoning quality, not pixel count. This also means the roadmap must invest in capabilities like collision meshes and physically plausible environments, not just aesthetics.

4. **3D world generation is a brand new model category**
   "This is a brand new category of model that's generating 3D worlds."
   — *Justin Johnson, Co-Founder of World Labs* ([TechCrunch, Nov 2025](https://techcrunch.com/2025/11/12/fei-fei-lis-world-labs-speeds-up-the-world-model-race-with-marble-its-first-commercial-product/))

   When a technology creates a new category, the product strategy cannot rely on analogies from adjacent categories (image generation, video generation, game engines). New categories require educating the market, establishing evaluation criteria, and defining the competitive landscape before competitors do. The PM's job shifts from "build the best product in an existing category" to "define what good looks like and then build it."

5. **Platforms beat applications because they compound through outside developers**
   "A platform is a system that can be programmed and therefore customized by outside developers — users — and in that way, adapted to countless needs and niches that the platform's original developers could not have possibly contemplated, much less had time to accommodate."
   — *Marc Andreessen* ([The Three Kinds of Platforms You Meet on the Internet](https://pmarchive.com/three_kinds_of_platforms_you_meet_on_the_internet.html))

   For spatial AI, the platform question is existential. A company that only ships a consumer app will be constrained to use cases it imagines. A company that ships a developer API enables robotics engineers, game designers, architects, and filmmakers to build applications the platform team never envisioned. The API is not a secondary product surface — it is the mechanism for discovering use cases at scale. The strategic decision is not whether to build a platform, but when and how aggressively to shift resources from first-party applications to platform infrastructure.

6. **Come for the tool, stay for the network**
   "The idea is to initially attract users with a single-player tool and then, over time, get them to participate in a network."
   — *Chris Dixon, General Partner at Andreessen Horowitz* ([Come for the Tool, Stay for the Network](https://cdixon.org/2015/01/31/come-for-the-tool-stay-for-the-network))

   For spatial AI, the "tool" is the world generator (consumer app, Marble). The "network" is the developer ecosystem (API, export pipeline, integrations). The consumer app demonstrates what is possible and acquires users. The API and third-party integrations create the network effects. Product strategy must sequence these deliberately: the consumer app should generate demand and validate the technology, while the API captures the long tail and builds defensibility through ecosystem lock-in.

7. **Digital twins and simulation will become infrastructure**
   "Artificial intelligence will be infrastructure," like water, electricity and the internet.
   — *Jensen Huang, CEO of NVIDIA* ([3DEXPERIENCE World, Feb 2026](https://blogs.nvidia.com/blog/huang-3dexperience-2026/))

   Huang's framing positions spatial AI not as a creative tool but as foundational infrastructure for industry. This has direct implications for World Labs' product strategy: the API should be designed for infrastructure-grade reliability, predictability, and scale — not just creative experimentation. The robotics and architecture verticals are not secondary markets; they are where spatial AI becomes mission-critical infrastructure. Pricing, SLAs, and export formats must reflect infrastructure expectations, not creative-tool expectations.

8. **Content creation is the bottleneck that spatial AI must break**
   "We need to deliver higher productivity than ever before, not only for games, but also for film and other industries."
   — *Tim Sweeney, CEO of Epic Games* ([Game Developer Interview](https://www.gamedeveloper.com/design/an-interview-with-epic-games-tim-sweeney))

   The 3D content pipeline is the single biggest constraint in gaming, film, architecture, and robotics simulation. Every environment built by hand costs thousands of dollars and weeks of artist time. Spatial AI's value proposition is not "better worlds" — it is "worlds at a fraction of the time and cost." Product strategy should relentlessly focus on reducing time-to-world and cost-per-world. Every feature that does not reduce friction in the content pipeline is a distraction.

9. **Aggregators win by owning the user relationship and commoditizing supply**
   "The key characteristic of Aggregators is that they own the user relationship."
   — *Ben Thompson* ([Aggregation Theory, Stratechery](https://stratechery.com/aggregation-theory/))

   In spatial AI, the "supply" is 3D world generation capability, and the "user relationship" is owned by whoever controls the interface — the consumer app (Marble), the API, or RTFM's interactive experience. Thompson's framework clarifies the strategic risk: if World Labs only generates worlds but another company controls distribution, the generation capability gets commoditized. Owning the consumer surface (Marble), the real-time experience (RTFM), and the developer interface (API) is the mechanism for owning the user relationship and preventing commoditization.

## Instructions

### Step 1: Map the Spatial AI Capability Landscape

Assess what is technically possible today versus what is on the research frontier:

- **Generation capabilities:** Text-to-world, image-to-world, video-to-world, multi-angle-to-world. Which are production-ready? Which are experimental?
- **Real-time vs. batch generation:** RTFM generates frames in real-time (interactive exploration, implicit 3D). Marble generates persistent worlds in minutes (explicit 3D, exportable). Map where each model excels and where they overlap. See `context/products/rtfm.md`.
- **Output capabilities:** Gaussian splats (SPZ), meshes (GLB), panoramas, thumbnails. Which export formats do target verticals actually need?
- **Quality/speed trade-offs:** Draft models (fast, lower quality) vs. production models (slow, high quality). How does this map to user workflows?
- **Spatial reasoning:** Physics plausibility, collision detection, scale accuracy, lighting consistency. Where are the model's strengths and gaps?
- Check `context/products/` for current Marble capabilities and API surface
- **Output:** Capability landscape matrix (available / emerging / frontier) with quality assessments

### Step 2: Assess Product-Market Fit Across Surfaces

Evaluate PMF separately for each product surface, because a consumer app and a developer API have entirely different users and value propositions:

| Surface | Target User | Value Proposition | PMF Signal | Current State |
|---|---|---|---|---|
| Consumer App (Marble) | Creative professionals, enthusiasts | "See your idea in 3D in seconds" | Retention, sharing, repeat generation | ? |
| Developer API | Game studios, robotics teams, architecture tools | "Programmable world generation at scale" | API call volume, integration depth, willingness to pay | ? |
| Enterprise | VFX studios, simulation companies | "Custom pipeline integration" | Contract value, renewal rate | ? |

For each surface, document evidence of product-market fit or lack thereof. Use Sean Ellis's test: what percentage of users would be "very disappointed" if this product disappeared?
- Check `context/verticals/` for demand signals from gaming, robotics, and architecture
- **Output:** PMF assessment table with evidence and gaps

### Step 3: Define the Platform Strategy

The central strategic question: when does World Labs transition from building applications to building a platform?

Analyze the platform readiness indicators:
- **API stability:** Is the API surface stable enough for third parties to build on?
- **Developer demand:** Are developers asking for capabilities not yet exposed?
- **Use case diversity:** Are API users building things the World Labs team did not anticipate?
- **Ecosystem infrastructure:** Are there SDKs, documentation, community resources sufficient for self-service adoption?

Define the platform strategy along a spectrum:
1. **Tool phase** (current?) — First-party app drives all usage, API is secondary
2. **Platform-curious** — API usage growing, but first-party app still dominant
3. **Platform-first** — API ecosystem generates more value than first-party app
4. **Platform-only** — First-party app becomes a reference implementation, all innovation from ecosystem

For each phase, specify: resource allocation, API investment level, developer relations posture, pricing strategy.
- Check `context/company/` for team size and whether platform investment is feasible at current scale
- **Output:** Platform maturity assessment and phase transition plan

### Step 4: Design the Product Portfolio

Define the role of each product surface in the portfolio:

| Surface | Portfolio Job | Horizon | Resource Allocation |
|---|---|---|---|
| Consumer App (Marble) | Acquisition engine + technology showcase | H1 | ?% |
| Developer API | Monetization engine + use case discovery | H1/H2 | ?% |
| RTFM (Real-Time Frame Model) | Interactive exploration + preview mode + real-time experiences | H1/H2 | ?% |
| Enterprise Offering | Revenue engine + vertical depth | H3 | ?% |

For each surface, apply the framework from Principle 6 (come for the tool, stay for the network):
- How does this surface attract users initially (tool value)?
- How does this surface create network effects over time (network value)?
- What feedback loops connect this surface to other surfaces?

Map the cross-surface flywheel:
```
Consumer App (demand generation)
  --> API (programmatic access)
    --> Developer ecosystem (new use cases, integrations)
      --> More demand for Consumer App + API
```
- Check `context/founders/` for founder vision on portfolio priorities
- **Output:** Portfolio strategy with job assignments, horizon classification, and flywheel map

### Step 5: Build the Input-Output Strategy

Spatial AI's competitive differentiation comes from the breadth and quality of its input-output pipeline. Prioritize modalities based on vertical demand:

**Input prioritization matrix:**

| Input Modality | Gaming Demand | Robotics Demand | Architecture Demand | Film/VFX Demand | Priority |
|---|---|---|---|---|---|
| Text-to-world | High | Medium | Medium | Medium | ? |
| Image-to-world | High | Low | High | High | ? |
| Video-to-world | Medium | High | Low | High | ? |
| Multi-angle-to-world | Low | Low | High | Medium | ? |
| Pano-to-world | Medium | Low | Medium | Medium | ? |

**Output prioritization matrix:**

| Output Format | Gaming Need | Robotics Need | Architecture Need | Integration Difficulty |
|---|---|---|---|---|
| SPZ (Gaussian splats) | Medium | Low | Low | New format, needs renderer |
| GLB (mesh) | High | High | High | Industry standard |
| USD (Universal Scene Description) | High | High | Medium | NVIDIA ecosystem |
| USDZ (Apple) | Medium | Low | High | Apple ecosystem |
| Collider mesh | Low | High | Low | Physics simulation |

Recommendation: Prioritize output formats that unlock the highest-value verticals. GLB mesh export is table stakes. USD export is the bridge to game engines and NVIDIA's robotics simulation ecosystem. Collider meshes unlock the robotics vertical.
- Check `context/verticals/` for specific customer requests by format
- **Output:** Prioritized input-output roadmap with vertical justification

### Step 6: Develop the Ecosystem Flywheel

Design the specific mechanisms that create compounding value:

1. **Developer tools and SDKs**
   - Python SDK, JavaScript SDK, Unity plugin, Unreal plugin
   - Each SDK targets a specific vertical and reduces integration time
   - Track: SDK downloads, time-to-first-world for new developers

2. **Content marketplace (future)**
   - User-generated worlds as a shared asset library
   - Network effects: more worlds make the platform more valuable for all users
   - Gating question: Is generation quality consistent enough for shared assets?

3. **Integration partnerships**
   - NVIDIA Isaac Sim (robotics), Unity/Unreal (gaming), Figma/Rhino (architecture)
   - Each integration creates a new on-ramp to the World Labs API
   - Track: API calls originating from each integration partner

- Check `context/competitive/` for competitor ecosystem moves that create urgency
- **Output:** Ecosystem flywheel diagram with investment priorities, metrics, and sequencing

### Step 7: Create the Competitive Positioning Framework

Position World Labs on the two axes that matter most in spatial AI:

**Axis 1: Infrastructure vs. Entertainment**
- Infrastructure (World Labs): Persistent, exportable, programmable worlds. Value proposition is "build on us."
- Entertainment (Google Genie 3): Ephemeral, non-exportable, consumer experiences. Value proposition is "play with us."

**Axis 2: Real-time vs. Batch**
- Real-time (RTFM, Genie 3): Interactive framerates, exploration, immediate feedback
- Batch (Marble, traditional 3D generation): Minutes per world, high fidelity, exportable

World Labs is now the only company spanning both axes: real-time exploration (RTFM) AND persistent exportable infrastructure (Marble). Update the positioning to reflect this "both/and" advantage. See `context/products/rtfm.md` and consider running `real-time-persistent-convergence` for the full analysis.

**Axis 3: Developer-first vs. Consumer-first**
- Developer-first (World Labs API): Programmable, composable, integrates into existing pipelines
- Consumer-first (Google Genie 3): End-user experience, no API, no developer access

Draft positioning statements for each audience:
- **For developers:** "World Labs is the programmable infrastructure for 3D world generation — persistent, exportable, and designed to integrate into your existing pipeline."
- **For enterprises:** "Generate diverse, physically plausible 3D environments at scale — for robotics training, architectural visualization, and game development."
- **For creatives:** "Turn any idea into an explorable 3D world in seconds — from a text description, a sketch, a photo, or a video."

Competitive response triggers — define what competitor moves require a response:

| Competitor Move | Response Type | Urgency |
|---|---|---|
| Genie 3 launches a public API | Offensive — accelerate API feature development | High |
| NVIDIA ships native world generation in Omniverse | Defensive — deepen Isaac Sim integration | High |
| Open-source model matches Marble quality | Positioning — emphasize managed service value | Medium |
| Game engine ships built-in generation | Partnership — integrate rather than compete | Medium |

- Check `context/competitive/` for current competitor status and recent moves
- **Output:** 2x2 positioning map, audience-specific positioning statements, and competitive response playbook

## Diagnostic Questions

1. **Can you explain why spatial AI is a new category, not an extension of 2D image or video generation?**
   If the team cannot articulate the category difference, the product will be positioned incorrectly and evaluated against the wrong competitors. The answer should reference 3D understanding, persistence, exportability, and spatial reasoning — not just visual quality.

2. **What is the ratio of API-originated worlds to consumer-app-originated worlds?**
   This reveals where value is actually being created. If the API is generating more worlds, the platform transition is underway. If the consumer app dominates, the company is still in tool phase. This ratio should be tracked weekly and informs resource allocation.

3. **Which export format generates the most downstream integrations?**
   Export formats are not commodities — they are strategic choices. If SPZ is widely used, the ecosystem is building around Gaussian splats (World Labs' advantage). If developers are converting to GLB before using the output, mesh quality is the bottleneck.

4. **What percentage of API users are building applications the World Labs team did not anticipate?**
   This is the platform signal. If >30% of API usage is for unanticipated use cases, the platform is working. If API usage mirrors the consumer app's use cases, the API is just an alternative interface, not a platform.

5. **How long does it take a new developer to generate their first world via the API?**
   Time-to-first-world is the developer experience north star. If it takes more than 30 minutes from API key to generated world, the DX is a growth bottleneck. Every minute of friction here costs potential ecosystem participants.

6. **What would happen if Google Genie 3 launched a public API tomorrow?**
   This forces the team to articulate their defensible advantages: persistence, export pipeline, multi-modal input, quality, developer ecosystem. If the answer is "we'd be in trouble," the strategy lacks a moat. If the answer references ecosystem lock-in and format advantages, the platform strategy is working.

## Common Mistakes

1. **Treating spatial AI as "3D image generation"** — Spatial AI generates persistent, explorable, physically structured 3D environments. Positioning it as "Midjourney but 3D" attracts the wrong users, invites the wrong comparisons, and misses the infrastructure opportunity. The value is in spatial understanding and exportable assets, not prettier pictures.

2. **Building API and consumer app as separate products** — The API and consumer app must share a model, a pipeline, and a product strategy. When they diverge, the company ends up maintaining two products with different quality bars, different release cycles, and different user expectations. The consumer app should be the best API client, not a separate codebase.

3. **Ignoring export format strategy** — Export formats determine which ecosystems the product integrates with. SPZ is a newer format that requires compatible renderers. GLB opens the door to Unity, Unreal, Blender, and the entire 3D industry. USD opens the door to NVIDIA Omniverse and professional pipelines. Treating export as an afterthought cedes the integration layer to competitors.

4. **Over-investing in generation quality at the expense of developer experience** — A model that generates stunning worlds but requires 47 API calls and manual polling to use will lose to a model that generates good worlds with a single function call. Developer experience is as important as generation quality for platform adoption. The best model in the world loses if no one can integrate it.

5. **Chasing the consumer entertainment use case instead of building infrastructure** — Consumer entertainment (Genie 3's approach) is high-visibility but low-defensibility. Infrastructure (API + export pipeline) is low-visibility but high-defensibility. The temptation is to build viral consumer features. The strategy should be to build the infrastructure that makes those consumer features possible for everyone.

## Context Integration

How this skill uses the `context/` directory when available:

| Context Directory | Used In | Purpose |
|---|---|---|
| `context/founders/` | Step 4 (Portfolio Design), Principles | Founder vision shapes platform vs. application balance and category creation strategy |
| `context/products/` | Step 1 (Capability Mapping), Step 2 (PMF Assessment) | Current Marble capabilities and API surface inform gap analysis |
| `context/verticals/` | Step 2 (PMF), Step 5 (Input-Output Strategy) | Gaming, robotics, and architecture demand signals drive modality and export priorities |
| `context/competitive/` | Step 6 (Ecosystem Flywheel), Step 7 (Positioning) | Competitor moves (especially Genie 3, NVIDIA Cosmos) inform positioning urgency and response triggers |
| `context/company/` | Step 3 (Platform Strategy), Step 4 (Portfolio Design) | Team size (~41 people) and funding ($250M+) constrain how many product surfaces can be staffed |
| `context/signals/` | Step 2 (PMF), Step 6 (Ecosystem), Step 7 (Positioning) | Auto-collected signals from GitHub, HN, Reddit, news. [SIGNAL] tagged. GitHub ecosystem data informs developer adoption velocity. Community discussions reveal PMF signals across surfaces. Competitor mentions from `_synthesis.md` drive positioning urgency. Check freshness before citing. |

If no `context/` directory is available, the skill uses web search to gather current data on World Labs' products, competitors, and market dynamics. Results will be less precise but still structurally sound.

# Product Vision & Roadmap: World Labs

> Applied output from `product-portfolio-strategy` + `spatial-ai-product-strategy` skills
> Author: Ashka Stephen | [PUBLIC]. All data from publicly available sources.

---

## Vision Statement

World Labs is building the infrastructure layer for spatial intelligence: making 3D world generation as programmable and accessible as text generation became with LLMs. The end state is a new computational primitive (beyond a better rendering tool) where any developer, designer, or creator can turn any signal (a sentence, a photo, a video) into a persistent, exportable, physically structured 3D environment. Within two years, "generate a world" should feel as natural as "generate an image" does today.

---

## Product Portfolio Overview

World Labs ships three product surfaces that serve distinct but reinforcing roles:

| Product | Role | User | Business Function |
|---|---|---|---|
| **Marble App** | Consumer front door | Creators, enthusiasts, professionals exploring ideas | Acquisition + technology validation |
| **World API** | Developer backbone | Game studios, robotics teams, architecture tools, indie devs | Monetization + ecosystem expansion |
| **RTFM** | Real-time exploration layer | Interactive experiences, previews, real-time use cases | Speed + interactivity (bridges consumer and developer) |

**The flywheel:** Marble demonstrates what is possible and generates viral content. RTFM lets users explore interactively in real-time. Both drive developers to the API. Developers build applications and integrations. New use cases emerge. Usage data improves the models. Better models make Marble and RTFM more compelling. Repeat.

```
Marble App (demand + validation)
  --> RTFM (real-time exploration, preview)
    --> Developers discover the API (conversion)
      --> New use cases emerge (ecosystem)
        --> Usage data improves the model (R&D)
          --> Better Marble + RTFM experience (retention + virality)
```

The critical insight: World Labs is now the only company offering both real-time interactive generation (RTFM) and persistent exportable 3D (Marble). This combination is the platform moat; competitors offer one or the other, rarely both.

---

## Strategic Themes

Four themes guide every roadmap decision for the next 18 months:

### 1. From Generation to Creation
Generation alone is one-shot: input goes in, a world comes out. Deepening editing (object manipulation, lighting adjustments, material swaps, and broader programmatic control via the API) is what raises retention (consumers) and integration depth (developers). Pushing editing from the app surface into the API is the single highest-leverage capability gap.

### 2. From Manual to Programmatic
The API requires polling, has no batch endpoint, no webhooks, and a minimal Python SDK with no TypeScript SDK. Every missing developer primitive is friction that prevents adoption. The goal: a developer should go from API key to first generated world in under 10 minutes, with a single function call, in their language of choice.

### 3. From Single-User to Social
Marble worlds are islands. There is no gallery, no community discovery, no shared exploration, no remixing. Social features turn a generation tool into a content platform, and content platforms gain network effects that pure tools lack. The sequencing matters: community gallery first (low lift, high signal), collaborative exploration later (high lift, high payoff).

### 4. From General to Vertical-Specific
Gaming studios need USD/FBX export and engine plugins. Robotics teams need batch generation and physics-ready collider meshes. Architects need multi-angle input fidelity and measurement accuracy. Horizontal capability is necessary but not sufficient. Vertical depth is what converts pilots to contracts.

---

## Roadmap

### Now through Q2 2026: Foundation

**World API**
- Ship official TypeScript/Node SDK (largest web developer population, no official SDK exists)
- Add webhook callbacks for world generation completion (eliminate polling)
- Launch batch generation endpoint (submit N prompts, get N worlds, single API call)
- Publish comprehensive API reference with runnable examples for all 4 input modalities

**Marble App**
- Launch community gallery with public world browsing and search
- Add world sharing improvements: embeddable viewer, social preview cards, short URL sharing
- Begin editing prototype: start with lighting/time-of-day control as lowest-risk editing surface
- Introduce vertical-specific prompt presets (architecture interiors, game environments, product scenes)

**RTFM**
- Publish research findings and gather developer feedback on productization priorities
- Prototype RTFM-to-Marble pipeline: explore in real-time, then "render" the best view into a persistent Marble world
- Evaluate API endpoint design for real-time generation

**Platform**
- Developer documentation overhaul: quickstart guides per language, interactive API explorer
- Onboarding flow optimization: reduce time-to-first-world below 10 minutes
- Credit usage dashboard with per-operation cost visibility

### Q3 through Q4 2026: Growth

**World API**
- Launch Editing API v1: modify lighting, swap materials, adjust camera paths on existing worlds
- Ship enterprise tier: SLA guarantees (99.9% uptime), SSO, volume pricing, dedicated support
- Add real-time generation status streaming (Server-Sent Events) as alternative to polling
- Introduce model fine-tuning API for enterprise customers (style-consistent generation)

**Marble App**
- Collaborative world exploration: invite links, shared camera views, voice chat overlay
- Template library: curated starting points for common use cases (product photography, game levels, architectural walkthroughs)
- Remixing: generate variations of existing public worlds with one click

**RTFM**
- Ship RTFM API endpoint with real-time streaming
- RTFM + Marble convergence: unified workflow from real-time preview to production export
- VR/WebXR real-time exploration mode

**Platform**
- Community marketplace for templates and world presets
- Vertical-specific SDK packages: `@worldlabs/robotics` (Isaac Sim helpers, batch environment generation), `@worldlabs/creative` (style presets, camera tools)
- Launch partner program with co-marketing for top integrations

### 2027+: Vision

**World API**
- Scene composition: combine multiple generated worlds or insert generated objects into existing environments
- Persistent world hosting: serve generated worlds as always-on URLs with CDN-backed rendering
- Multi-modal editing: modify worlds via text instructions ("add a lamp in the corner," "make it sunset")

**Marble App**
- Full creative suite: object placement, material editing, scene merging, export to any format
- Multiplayer persistent worlds: shared spaces that multiple users can inhabit and modify simultaneously
- AI co-creation: conversational world editing ("move the table closer to the window")

**Integrations**
- Native Unity and Unreal Engine plugins (generate environments inside the editor, not via external API)
- Deeper NVIDIA Isaac Sim integration: one-click world-to-simulation pipeline with physics baked in
- Figma/design tool plugins for architectural visualization workflows

**Model**
- Next-generation model with sub-10-second draft generation
- Real-time refinement: generate a coarse world instantly, progressively enhance as user explores
- Video-to-persistent-world at production quality (capture a real space, generate a navigable digital twin)

---

## Success Metrics

| Metric | Current (Feb 2026 est.) | Q2 2026 Target | Q4 2026 Target |
|---|---|---|---|
| **Registered API developers** | ~500 | 3,000 | 10,000 |
| **Worlds generated / day (API)** | ~200 | 1,500 | 5,000 |
| **Developer activation rate** (first world within 7 days of key creation) | ~25% | 50% | 65% |
| **Marble App MAU** | ~50,000 | 200,000 | 500,000 |
| **Enterprise contracts signed** | 3-5 (pilot stage) | 10 | 25 |
| **RTFM weekly sessions** | Research preview | 5,000 | 25,000 |

---

## Key Bets & Risks

| Bet | Rationale | Risk If Wrong |
|---|---|---|
| **Editing API is the #1 unlock for retention** | One-shot generation is a novelty; editing makes it a tool. Every creative professional needs iteration. Without editing, users generate once and leave. | If editing is too hard technically (model limitations) or users don't actually iterate, we've invested 2-3 eng quarters in a feature that doesn't move retention. Mitigation: prototype with lighting-only edits first, measure before going deeper. |
| **TypeScript SDK matters more than Python SDK improvements** | Web developers outnumber Python developers in the creative tools and gaming verticals. The existing Python client covers basic needs; TypeScript has zero official coverage. | If the high-value developers turn out to be Python-first (robotics, ML engineers), we under-serve the revenue-generating segment. Mitigation: ship both, but TS first. |
| **Community gallery drives consumer retention, not better generation** | Generation quality is already impressive. The gap is that users have nowhere to go after generating: no discovery, no audience, no feedback loop. Gallery creates the content network. | If users don't engage with others' worlds (3D browsing is niche), the gallery becomes a dead feature. Mitigation: curate aggressively at launch, feature staff picks, seed with partner content. |
| **Vertical SDKs beat horizontal features for enterprise conversion** | Enterprise buyers don't want a general API; they want a solution shaped to their workflow. `@worldlabs/robotics` with Isaac Sim helpers closes faster than generic API improvements. | If verticals fragment the engineering team and none reaches depth, we spread thin across use cases without winning any. Mitigation: pick robotics first (warmest partnership, clearest ROI), prove the model, then expand. |

---

## What We Are NOT Building (and Why)

| Not Building | Why Not |
|---|---|
| **Competing with game engines on editing** | Unity and Unreal have 20+ years of editing toolchain investment. World Labs should focus on generation and export, not try to replicate full scene authoring. The editing API should enable lightweight modifications, not replace DCC tools. |
| **A game engine** | Unity and Unreal have 20+ years of ecosystem investment. World Labs should integrate into engines, not replace them. The correct surface is a plugin that generates environments inside existing editors, meeting developers where they already work. Building an engine would consume the entire company. |
| **A Blender/Maya replacement** | Professional 3D artists are not the primary user. They have mature tools and deep muscle memory. World Labs should export formats that import cleanly into existing DCC tools, not try to replicate their editing UI. The editing API should enable lightweight modifications, not full scene authoring. |

---

*This roadmap assumes a team of roughly 50-60 employees and total funding of about $1.23B (the $230M Series A plus the $1B round that closed 2026-02-18, with investors including Autodesk, Andreessen Horowitz, NVIDIA, and AMD). Hiring a PM, scaling engineering, and securing enterprise partnerships will determine execution velocity. The themes are sequenced to deliver compounding value: each phase builds infrastructure that makes the next phase cheaper and faster to execute.*

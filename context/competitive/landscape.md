# Competitive Landscape — Spatial AI & World Models

## Market Map

The spatial AI / world model space has players across several categories:

### Category 1: World Model Companies (Direct Competitors)

| Company | Product | Model | Key Differentiator | Threat Level |
|---|---|---|---|---|
| **World Labs** | Marble App + World API | Large World Model | Persistent, exportable, developer API | — (us) |
| **Google DeepMind** | Genie 3 | Autoregressive world model | Real-time generation (20-24fps), consumer-only. Now also powering Waymo World Model for AV simulation. | High |
| **Waymo** (Alphabet) | Waymo World Model | Genie 3 + AV post-training | AV-specific sim with camera + lidar output. Not a product for sale. Announced 2026-02-06. | Medium (indirect) |
| **Runway** | GWM-1 | Video-first world model | Video generation expertise, creative tools brand | Medium |
| **Odyssey** | Explorer | Causal world model | Storytelling-focused, narrative generation | Medium |
| **Decart** | Oasis/Lucy 2.0 | Real-time video transformation | Gaming-focused, real-time | Medium |

### Category 2: 3D Generation (Adjacent)

| Company | Product | Approach | Overlap with World Labs |
|---|---|---|---|
| **NVIDIA** | Cosmos | Open-source robotics/AV platform | Overlaps in robotics simulation vertical |
| **Luma AI** | Dream Machine / Genie | NeRF-based 3D generation | Object-level generation, not full worlds |
| **Meshy** | Text-to-3D | Mesh generation pipeline | Single objects, not environments |
| **Kaedim** | AI 3D modeling | Production 3D assets | Asset-level, not world-level |

### Category 3: Game Engine AI (Platform Competitors)

| Company | Product | Approach | Overlap with World Labs |
|---|---|---|---|
| **Unity** | Muse / AI tools | AI-assisted content creation in-engine | Could build generation into the engine |
| **Epic Games** | Unreal + AI | AI tools for Unreal Engine | Deepest creative tool ecosystem |
| **Roblox** | AI generation tools | AI for user-generated content | Massive creator ecosystem |

### Category 4: Pre-Product Research

| Lab | Focus | Status |
|---|---|---|
| **AMI Labs** (Yann LeCun) | JEPA architecture, world models | Pre-product, theoretical |
| **Various academic groups** | World model research | Papers, not products |

## World Labs' Positioning

World Labs occupies a unique position: **the only company offering persistent, exportable 3D worlds through a developer API.** Every competitor is missing at least one of these properties.

## Strategic Implications

1. **Google is the biggest competitive threat, and Genie 3 is becoming infrastructure** — Waymo's use of Genie 3 (Project Genie, Feb 2026) shows Google's world model is being embedded in vertical products across Alphabet. If this pattern repeats, Genie 3 becomes a foundation model that powers vertical-specific simulators, not just a consumer demo. World Labs' moat is the API + export pipeline. However, the narrative threat is key.
2. **Runway is the brand threat** — Runway has strong brand recognition among creatives. If they ship a world generation API, they'll capture the creative tools market.
3. **NVIDIA is the partnership opportunity** — Cosmos is open-source for robotics. World Labs + NVIDIA Isaac Sim integration is already happening. But NVIDIA also has deep ties to Waymo, so the partnership landscape is complex.
4. **The window is open but narrowing** — No competitor has a world generation API with export. But Genie 3's spread into Waymo signals that Google's ecosystem is expanding fast. World Labs needs to lock in mindshare and adoption before Genie 3 gets an API.
5. **RTFM changes World Labs' competitive position** — With RTFM, World Labs has both real-time generation (matching Genie 3's core strength) and persistent exportable worlds (which no one else offers). This is the strongest positioning World Labs has had.

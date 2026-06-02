# RTFM — Real-Time Frame Model

**Blog:** [worldlabs.ai/blog/rtfm](https://www.worldlabs.ai/blog/rtfm)
**Demo:** [rtfm.worldlabs.ai](https://rtfm.worldlabs.ai)

## Overview

RTFM (Real-Time Frame Model) is World Labs' second world model — a generative model that produces video in real-time during user interaction. It generates new viewpoints on the fly from input images, without constructing explicit 3D geometry. Released as a research preview in late 2025.

## How It Works

- **Architecture:** Autoregressive diffusion transformer operating on sequences of frames, trained end-to-end on large-scale video data
- **Input mechanism:** Converts input frames into neural network activations (KV cache) that implicitly represent the world
- **Generation:** Network reads from this implicit representation via attention mechanisms to create new viewpoints consistent with input images
- **Spatial memory:** Each generated frame is assigned a pose (3D position and orientation). "Posed frames as spatial memory" enables unbounded persistence.
- **Context juggling:** Retrieves spatially nearby frames when generating new ones — avoids ever-expanding context, keeps compute cost per frame constant regardless of exploration duration

## Performance

- Runs on a single H100 GPU
- Designed to scale with increased compute and data

## Capabilities

- Complex visual effects: reflections, glossy surfaces, shadows, lens flare
- Works from single images to generate explorable 3D scenes
- Bridges reconstruction (interpolating between views) and generation (extrapolating beyond input views)
- Processes real-world video footage for scene rendering

## How It Differs from Marble

| Dimension | RTFM | Marble |
|---|---|---|
| **3D representation** | Implicit (neural activations, KV cache) | Explicit (Gaussian splats, meshes) |
| **Persistence** | Spatial memory (implicit) | Full persistent 3D world (explicit) |
| **Editability** | Not editable | Editable (Chisel + Marble Studio, "Create & edit" in the omnibox) |
| **API access** | Research preview only | Publicly Available |
| **Use case** | Exploration, preview, interactive experiences | Production assets, downstream pipelines, integration |

## Strategic Significance

- World Labs now has two world models with complementary strengths
- RTFM positions WL to compete directly with Google Genie 3 on real-time interactive generation
- Combined with Marble, WL can offer both speed (RTFM) and fidelity/export (Marble)
- The blog states RTFM "combines with Marble to create 3D worlds from single images," suggesting an intended integration path

## Limitations / Gaps

- Research preview — no API, no programmatic access
- User interaction capabilities noted as future pathway

## Key Questions for PM

1. Does RTFM become a "preview mode" in Marble? (Fast exploration before committing to full generation). Can RTFM output seed a Marble generation? (Website alludes to it, but unclear to me. Use RTFM to explore, then "render" the best view with Marble)
2. Which verticals care most about real-time? (Gaming, VR, robotics simulation)
3. What's the path from research preview to production?

# Waymo World Model

**Blog:** [waymo.com/blog/2026/02/the-waymo-world-model](https://waymo.com/blog/2026/02/the-waymo-world-model-a-new-frontier-for-autonomous-driving-simulation/)
**Related:** [Introducing EMMA](https://waymo.com/blog/2024/10/introducing-emma) | [Demonstrably Safe AI](https://waymo.com/blog/2025/12/demonstrably-safe-ai-for-autonomous-driving)

## What It Is

A generative AI system for creating hyper-realistic simulated driving environments, announced 2026-02-06. Built on Google DeepMind's Genie 3, adapted for autonomous driving through specialized post-training.

Waymo's framing: "Blended the smarts of Genie 3 with our unique experience in autonomous driving to build an end-to-end driving simulator which understands the world and renders it in a photorealistic way."

## How It Works 

- **Foundation:** Google DeepMind's Genie 3 (same underlying world model technology)
- **Enhancement:** Specialized post-training on Waymo's driving data (nearly 200 million fully autonomous miles)
- **Output:** High-fidelity, multi-sensor simulation including both camera AND lidar data
- **Explicit contrast with 3DGS:** Blog states that unlike "reconstructive methods (3D Gaussian Splats)," the learned World Model "maintains good realism and consistency" even when simulated routes differ significantly from original recordings

## Key Capabilities

Three control mechanisms:

| Control Type | What It Does | Example |
|---|---|---|
| **Driving action control** | Simulates counterfactual "what if" scenarios | "What happens if the car turns left here instead?" |
| **Scene layout control** | Customizes road layouts, traffic signals, pedestrian behavior | Rearrange intersection geometry, add vehicles |
| **Language control** | Text prompts adjust weather, time of day, or generate synthetic scenes | "Snow on the Golden Gate Bridge" |

Rare event simulation: tornadoes, floods, wrong-way drivers, elephants on the road. Events that are nearly impossible to capture at scale in real driving data.

## Performance

- Supports 4x playback speed while maintaining "high realism and fidelity"
- Extended rollouts with reduced compute
- Multi-sensor output (camera + lidar), not just visual frames

## Strategic Significance for World Labs

### 1. Genie 3 is becoming infrastructure, not just a product

This is the first case of Google's world model technology being embedded in a vertical-specific product by a major company. Waymo did not build their own world model from scratch. They took Genie 3 and fine-tuned it. If this pattern repeats (other Google/Alphabet companies or partners doing the same), Genie 3 becomes a foundation model that powers vertical products, not just a standalone demo. Key risk

### 2. Direct shot at Gaussian splatting

The blog explicitly contrasts their approach with "3D Gaussian Splats". Waymo is arguing that learned world models (implicit 3D) are better than reconstruction-based methods (explicit 3D) for simulation, because they generalize to new viewpoints and scenarios that were never recorded. This is the same argument RTFM somewhat makes.

### 3. Autonomous driving simulation is a massive vertical

Waymo has 200M autonomous miles of data. Their simulator needs to generate millions of diverse scenarios. This is the kind of high-volume, mission-critical use case that World Labs has been targeting with the robotics vertical. Waymo building their own (on Genie 3) instead of using World Labs' API is a key signal (though it makes sense due to the Google affiliation); What we DON'T want is this to signify market leadership in the autonomous driving space such that other companies follow Waymo's  route.

### 4. Multi-sensor output raises the bar

Waymo's model outputs camera AND lidar data. World Labs' current export pipeline (SPZ, GLB) does not include seem to include synthetic sensor data.

## Relationship to Broader Waymo AI Stack

Waymo's "Demonstrably Safe AI" blog (Dec 2025) describes a full stack:

- **Waymo Foundation Model:** A world model serving as the cornerstone, combining learned embeddings with structured representations
- **EMMA** (2025 updated): End-to-End Multimodal Model for driving, built on Gemini. Processes raw camera inputs to generate trajectories, object detection, road graphs. https://waymo.com/research/emma/
- **Learning flywheels:** Inner loop + outer loop.

The World Model is one piece of an integrated autonomous driving AI stack. It is not yet a general-purpose product - it's the composable building block.

## Threat Assessment

| Dimension | Threat Level | Rationale |
|---|---|---|
| **Direct competition with WL products** | Low | Waymo is not selling world generation as a product. Internal tool for AV simulation. |
| **Narrative/positioning threat** | High | "Genie 3 powers Waymo" validates Google's world model as production-ready. Makes WL positioning harder. |
| **Vertical market threat (robotics/AV)** | High | If AV companies build on Genie 3 instead of buying from WL, the robotics vertical closes. |
| **Technical benchmark threat** | Medium | Multi-sensor output (camera + lidar) sets a new bar WL does not currently meet. |
| **Talent competition** | Medium | Google DeepMind + Waymo can attract world model researchers with AV-scale data and compute. |

## Key Questions for PM

1. Is Waymo's use of Genie 3 a one-off or the start of a pattern? Will other Google/Alphabet companies do the same? Other autonomous driving companies?
2. Should World Labs pursue autonomous driving simulation as a vertical, or concede it?
3. Does WL need to add synthetic sensor data (lidar, radar) to the export pipeline to compete?
4. How does this change the NVIDIA partnership, if at all? NVIDIA has relationships with both Waymo and World Labs.

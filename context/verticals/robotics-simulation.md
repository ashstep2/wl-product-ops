# Robotics & Simulation Vertical

> All information sourced from publicly available data. Tagged [PUBLIC].

## Overview

Generate diverse 3D environments at scale for robotics training, simulation testing, and synthetic data generation. This is the most technical vertical with the clearest enterprise value proposition.

## Key Partners & Integrations

| Partner | Use Case | Source |
|---|---|---|
| **NVIDIA Isaac Sim** | Integration for robotic simulation environments | [NVIDIA Developer Blog](https://developer.nvidia.com/blog/simulate-robotic-environments-faster-with-nvidia-isaac-sim-and-world-labs-marble) |
| **Lightwheel** | Evaluation across many diverse environments | [World Labs case studies](https://www.worldlabs.ai/case-studies/2-lightwheel) |
| **MuJoCo / RoboSuite** | Physics simulation frameworks | [World Labs blog](https://www.worldlabs.ai/blog/announcing-the-world-api) |

## Use Cases

1. **Training environment diversity:** Generate thousands of unique environments for robot training (warehouses, kitchens, offices, hospitals)
2. **Sim-to-real transfer:** More diverse training environments → better real-world generalization
3. **Evaluation at scale:** Test robot policies across many environment variations
4. **Synthetic data generation:** Generate labeled 3D scenes for perception training
5. **Digital twin creation:** Generate 3D models of real-world spaces from photos/video

## Why It Matters for World Labs

- **Highest enterprise value:** Robotics companies will pay significant amounts for environment generation at scale
- **Batch API demand:** Robotics users need to generate 100s or 1000s of environments, not one at a time
- **Mesh export is critical:** Robotics needs collider meshes (GLB) for physics simulation — this is a Marble 0.1-plus differentiator
- **NVIDIA partnership signal:** Integration with Isaac Sim suggests a strong enterprise channel
- **Fei-Fei Li's vision alignment:** "From seeing to doing" (NeurIPS 2024) directly maps to robotics

## Adoption Barriers

- **Physics accuracy:** Robotics needs physically accurate environments, not just visually plausible ones
- **Mesh quality:** Collider meshes need to be precise for simulation; generated meshes may have artifacts
- **Reproducibility:** Research requires reproducible environment generation — how deterministic is the API?
- **Scale economics:** At 1,500 credits/world (plus model), generating 1,000 environments costs ~$1,200. Needs volume pricing.

## Market Size [ILLUSTRATIVE]

- Robot simulation market: Growing rapidly with autonomous vehicle, warehouse automation, and household robotics
- Key companies: NVIDIA (Isaac), Google DeepMind, Tesla (Optimus), Amazon (warehouse robots), Agility Robotics
- Synthetic data for perception: $1-2B market growing 30%+ annually

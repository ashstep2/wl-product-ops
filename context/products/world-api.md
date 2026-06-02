# World API — Developer Product

**Docs:** [docs.worldlabs.ai/api](https://docs.worldlabs.ai/api)
**Platform:** [platform.worldlabs.ai](https://platform.worldlabs.ai)

## Overview

The World API is World Labs' developer-facing product — an API for programmatic 3D world generation. Developers can generate worlds from text, images, videos, and multi-angle images, then export.

## Pricing

- $1.00 USD per 1,250 credits
- Minimum purchase: 6,250 credits ($5.00)
- World generation costs vary by model:
  - **Marble 1.1** (default): ~1,500 credits/world base
  - **Marble 1.1 Plus**: variable pricing per auto-expanded world (automatic spatial expansion for larger, more complex worlds)
- Text/image → world may incur TWO events (pano generation + world generation)

## Keys Endpoints

| Endpoint | Function |
|---|---|
| `POST /worlds:generate` | Generate a world from text, image, multi-image, or video |
| `GET /operations/{id}` | Poll generation status |
| `GET /worlds/{id}` | Get world details and asset URLs |
| `POST /worlds:list` | List all generated worlds |
| `POST /media-assets:prepare_upload` | Upload custom images/videos |

## Input Types

- **Text:** Prompt → world
- **Image:** Single image → world (supports panoramas)
- **Multi-image:** Multiple angles with azimuth → world
- **Video:** Video clip → world

## Export Formats

- **Gaussian splats (SPZ):** 100k, 500k, full resolution
- **Collider mesh (GLB):** Marble 1.1 Plus only
- **Panorama image:** 2D panoramic view
- **Thumbnail:** Preview image

## Developer Ecosystem

| Resource | Stars | Description |
|---|---|---|
| [worldlabs-api-examples](https://github.com/worldlabsai/worldlabs-api-examples) | 13 | 4 CLI scripts + 1 web app. Minimal. |
| [worldlabs-api-python](https://github.com/worldlabsai/worldlabs-api-python) | 7 | Python client + splat utilities |

## Strengths

- **Full pipeline:** Generate + export + render — complete workflow
- **Multiple input modalities:** Text, image, video, multi-angle
- **Exportable assets:** Unlike competitors, you can download and use the 3D assets
- **SPZ format at multiple resolutions:** Quality vs performance tradeoffs 

## Weaknesses / Gaps

- **Thin SDK:** Official Python client is minimal. No official TypeScript/Node SDK.
- **No batch API:** Can't submit multiple worlds in one request
- **Limited examples:** Official repo has 4 scripts covering 2 of 4 input types
- **No streaming:** World generation is synchronous (poll until done)
- **No editing API:** Can't modify a generated world programmatically
- **Pricing transparency:** Credit costs per operation aren't fully documented upfront

## Strategic Role in Portfolio

- **Monetization engine:** Credits-based pricing generates revenue
- **Ecosystem builder:** Developers build apps and integrations on top
- **Platform play:** Third-party apps increase the value of the World Labs ecosystem
- **Enterprise gateway:** API usage patterns identify enterprise prospects

## Key Questions for PM

1. What's the developer activation metric? (First world generated via API? First app deployed?)
2. What's the retention curve for API developers? Do they keep generating or churn?
3. Which input modality drives the most value for developers?
4. Is batch generation a top request?
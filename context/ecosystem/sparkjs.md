# SparkJS — Open-Source Renderer

**URL:** [sparkjs.dev](https://sparkjs.dev/)

## Overview

SparkJS is World Labs' open-source 3D Gaussian splatting renderer, built on Three.js with Rust + WebAssembly for performance. It allows anyone to render World Labs-generated worlds (and other 3DGS content) in a web browser.

## Technical Details

- **Built on:** Three.js
- **Supported formats:** SPZ, PLY, SOGS, KSPLAT, SPLAT
- **Platforms:** Desktop and mobile browsers

## Key Features

- High-performance Gaussian splatting rendering
- THREE.js mesh integration (mix splats with traditional 3D content)
- Dynamic and procedural splat effects
- Quality selectors (100k / 500k / full resolution)
- Mobile-optimized rendering

## Strategic Role in Portfolio

SparkJS is a **open-source play** — it follows the "open the renderer, monetize the generation" pattern:

1. **Removes friction:** Anyone can view World Labs-generated worlds for free → increases the value of generated worlds
2. **Ecosystem lock-in:** Developers build rendering into their apps using SparkJS → creates dependency on World Labs' format
3. **Standard-setting:** If SparkJS becomes the default 3DGS renderer, World Labs defines the rendering standard
4. **Developer onramp:** Using SparkJS → using World API

## Competitive Context

Other 3DGS renderers exist, but SparkJS benefits from:
- Official backing by the leading world model company
- Active development driven by World Labs' product needs

## Key Questions for PM

1. What's SparkJS adoption? (npm downloads, GitHub stars, sites using it)
2. Are developers using SparkJS without the World API? (rendering other 3DGS content)
3. Does SparkJS need a plugin ecosystem? (effects, post-processing, VR support)

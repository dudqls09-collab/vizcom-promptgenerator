# Interior Scene Prompt Builder v1.5 — System Overview

## Purpose
- Build repeatable, high-quality prompts for generating interior scenes similar to user living environments.
- Separate internal **Spec** authoring from generated **Surface Prompt** output.
- Keep brand mood consistent through reusable **Scene DNA** presets.
- Prioritize compositing-ready background scenes with object-ready staging surfaces.

## Non-Goals
- This system does not guarantee pixel-perfect geometry.
- This system does not place products in SCENE_ONLY mode.
- This system does not rely on free-form negative text inside the main prompt body.
- This system does not use direct product keywords in Surface Prompt output.

## Core Terms
- **Spec**: Structured internal data model used as single source of truth for generation.
- **Surface Prompt**: Comma-separated, slot-based model input string compiled from Spec.
- **Compiler**: Deterministic mapping layer from Spec → Surface Prompt.
- **Lexicon**: Controlled dictionaries (room placement, scale buckets, Scene DNA) used by UI/compiler.
- **Gate**: Measurable pass/fail validation rule for consistency and safety.
- **Scene DNA**: Brand mood preset that fixes palette/material/light/grading/decor/photo tone.

## Modes
1. **SCENE_ONLY**
   - Generate an interior scene only.
   - Product slots are disabled.

2. **PRODUCT_IN_SCENE**
   - Use additional structural fields for staging-surface planning.
   - Output phrasing remains background-first and compositing-ready.

## Scene DNA Definition
Scene DNA is a reusable preset spec that locks interior mood through fixed slots:
- palette
- materials
- lighting
- grading
- decor_density
- photography_vibe

Scene DNA ensures consistency across iterations and can be further reinforced with a Vizcom Custom Palette in future workflows.

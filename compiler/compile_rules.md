# Compile Rules (Spec → Surface Prompt) v1.4

## Deterministic Mapping
- Generate always compiles from the latest in-memory Spec.
- Compiler never mutates Spec values.
- Compiler writes comma-separated slot strings only.

## Fixed Slot Order
1. Room + Mood + Time
2. Architecture/Layout cue
3. Scene DNA bundle
   - scene palette: `{scene_dna.palette}`
   - scene materials: `{scene_dna.materials}`
   - scene lighting: `{scene_dna.lighting}`
   - scene tone: `{scene_dna.grading}`
   - decor: `{scene_dna.decor_density}`
   - photography: `{scene_dna.photography_vibe}`
4. Anchor zone rule
5. Camera intent
6. Framing spec (master ratio + crop-safe derivatives)
7. Optional PRODUCT_IN_SCENE slots
   - product subject clause
   - placement clause (+ keep-out)
   - scale bucket surface phrase
   - brand moment sentence

## Mode Behavior
- `SCENE_ONLY`
  - Product fields are ignored and must not be rendered into output prompt.
- `PRODUCT_IN_SCENE`
  - Product fields are required and rendered after framing section.

## Lexicon Binding
- `room_type` × `placement` must resolve from `lexicon/room_placement_map.yml` allowlist unless placement is custom-added by user for the same room.
- `scale_bucket_cm` must resolve through `lexicon/scale_buckets.yml` and insert the bucket's `surface_prompt` text.
- `scene_dna_preset` must resolve to one preset in `lexicon/scene_dna.yml` and populate the six Scene DNA slots.

# Gates v1.4 (Pass Conditions)

- Gate: `output.master_ratio` is exactly one of `{1:1, 3:2}`.
- Gate: `scene.room_type` has a valid placement in room allowlist (`room_placement_map`) or a custom placement registered for that room.
- Gate: Generate recompiles Surface Prompt from current Spec on every run (no stale cache output).
- Gate: `SCENE_ONLY` mode does not emit product slots in Surface Prompt.
- Gate: `PRODUCT_IN_SCENE` mode emits product placement, scale bucket phrase, and brand moment slots.
- Gate: `scene.scene_dna_preset` resolves to one of five presets and all six Scene DNA slots are present in output.

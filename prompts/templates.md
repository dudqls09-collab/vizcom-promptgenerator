# Surface Prompt Templates v1.5

All templates are comma-separated slot strings. Slot order is fixed for consistency.

## Slot Order Standard
1. Room + Mood + Time
2. Architecture/Layout cue
3. Scene DNA bundle (palette/materials/lighting/grading/decor_density/photography_vibe)
4. Anchor zone rule
5. Camera intent
6. Framing spec (master ratio + crop-safe derivatives)
7. Staging surface directives (PRODUCT_IN_SCENE only)

## SCENE_ONLY
"{room_type} interior, {time_of_day} light, {mood},
{architecture_layout},
scene palette: {scene_dna.palette},
scene materials: {scene_dna.materials},
scene lighting: {scene_dna.lighting},
scene tone: {scene_dna.grading},
decor: {scene_dna.decor_density},
photography: {scene_dna.photography_vibe},
anchor zone: {anchor_rule},
camera: three-quarter interior viewpoint, pitch {pitch}°, yaw {yaw_dir} {yaw}°, {distance}, {lens_mm_equiv}mm,
framing: master {master_ratio}, crop-safe for {derivatives}"

## PRODUCT_IN_SCENE
"{room_type} interior, {time_of_day} light, {mood},
{architecture_layout},
scene palette: {scene_dna.palette},
scene materials: {scene_dna.materials},
scene lighting: {scene_dna.lighting},
scene tone: {scene_dna.grading},
decor: {scene_dna.decor_density},
photography: {scene_dna.photography_vibe},
anchor zone: {anchor_rule},
camera: three-quarter view, pitch {pitch}°, yaw {yaw_dir} {yaw}°, {distance}, {lens_mm_equiv}mm,
framing: master {master_ratio}, crop-safe for {derivatives},
staging surface: {placement_clause},
clearance: {keepout_clause},
support scale: {scale_bucket_surface_phrase},
scene intent: composition prepared for later object compositing"

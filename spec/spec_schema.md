# Spec Schema v1.4

## Root
- `mode` (required): `SCENE_ONLY | PRODUCT_IN_SCENE`
- `scene` (required)
- `camera` (required)
- `composition` (required)
- `output` (required)
- `product` (optional; valid only when `mode=PRODUCT_IN_SCENE`)

## scene
- `room_type` (required)
- `time_of_day` (required)
- `mood` (required)
- `scene_dna_preset` (required)

## camera
- `pitch` (required, number)
- `yaw` (required, number)
- `distance` (required, string)
- `lens_mm_equiv` (required, number)

## composition
- `decor_density` (required, string)
- `anchor_zone` (required, string)
- `crop_safe` (required, string)

## output
- `master_ratio` (required): `1:1 | 3:2`
- `derivatives` (required array): values from `16:9 | 1:1 | 4:5`

## product (mode-gated)
Only valid for `PRODUCT_IN_SCENE`.
- `placement` (required)
- `scale_bucket_cm` (required)

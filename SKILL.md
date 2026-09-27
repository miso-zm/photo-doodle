---
name: photo-doodle
description: Transform a real-life photo, primarily portraits, outfits, full-body poses, or people with pets, into a sparse hand-drawn daily line illustration. Preserve the photographed person's identity cues, hairstyle, expression, clothing, pose, and relationships. Also supports scenes and still life when requested; do not substitute a fixed IP character or apply a photo filter.
---

# Photo to Daily Line Illustration

Reconstruct the photograph as an illustration, primarily for photos of people. Preserve the photographed reality, but edit the visual information aggressively.

This is an independent visual language. Do not invoke Miso, Oro, or any fixed character system. Do not borrow their proportions, palettes, expressions, or assets.

## Required workflow

1. Inspect the uploaded photo and identify:
   - the real subjects and their identity cues;
   - the action, gaze, gesture, contact, and relationship;
   - distinctive hair, hair color/highlights, clothing silhouette, pet markings, and important objects;
   - one to three spatial anchors that make the scene legible.
2. Read [references/style-system.md](references/style-system.md).
3. Read the applicable section of [references/photo-types.md](references/photo-types.md).
4. Use the image-generation tool in reference/edit mode. Treat the photo as the content source and the relevant files in `assets/` as style references with explicit roles.
5. Generate one finished illustration. Do not trace every contour and do not apply a filter.
6. Check it against [references/quality-gate.md](references/quality-gate.md). If it fails, make one targeted correction; do not change unrelated approved features.

## Non-negotiable visual rules

- Preserve the actual person, pet, object, clothing, pose, action, and relationship. Never substitute a stock figure or fixed IP.
- Use abundant white or near-white negative space. Delete background texture, clutter, tiny architecture, surface detail, and photographic lighting.
- Keep only the subject, action, spatial anchor, and a few necessary props.
- Draw with medium-light black lines: visible but not heavy, organically wobbly, mildly pressure-varied, and slightly blunt at the ends. Long contours may bow or kink gently. Never use vector-smooth lines, uniform jitter, repeated sketch strokes, or hairline-thin outlines.
- Simplify faces strongly. Use short incomplete brows; an upper-eye curve plus a small pupil; a minimal nose hook or cue; and a short mouth with an optional tiny lower-lip cue. No lower lids, enclosed eyes, eyelashes, realistic irises, blush, oversized eyes, or baby-face proportions.
- Treat hair as a clear mass. Dark hair may use a solid black shape with a few bold, irregular white strand channels. Preserve the original hair base color, dyed color, and highlight placement; reduce complex hair to the base plus at most one or two highlight colors.
- Keep black fills solid and opaque. Never put white bubbles, marker gaps, grain, or mottling inside black.
- Use colored areas as clean, coherent flat fills. Keep the interior calm and even; allow only a very slight hand-shaped edge. Do not add marker bands, watercolor blooms, colored-pencil texture, cloudy shading, grain, hatching, or decorative holes.
- Derive color from the photo. Prefer black, white, and gray with one or two restrained accent colors. Preserve a distinctive clothing or hair color when it is part of recognition.
- Let the hand-drawn feeling come mainly from line rhythm, joins, contour decisions, and hair channels—not from noisy surface texture.

## Style anchors

Use these assets by role; do not copy their subject matter:

- `assets/primary-style-anchor.png`: primary overall anchor for contrast, wobble, black mass, accent color, and hair-channel handling.
- `assets/full-body-color-anchor.png`: approved full-body proportions, white space, blue/black/gray-blue balance, and clean flat-color treatment.
- `assets/line-weight-anchor.png`: approved medium-light line weight.
- `assets/style-baseline-card.png`: compact face, line, and fill reference; use its face examples when a portrait needs extra guidance.

For everyday objects, follow the simplification rules in `references/photo-types.md`; no separate object image is required.

When anchors disagree, follow `primary-style-anchor.png` for overall feeling and `full-body-color-anchor.png` for large colored areas.

## Prompt skeleton

Give the image tool a short structured brief:

```text
Input photo: content and identity source.
Style references: [name each relevant anchor and its role].
Preserve: real subjects, identity cues, pose/action, relationship, distinctive hair/clothing/pet markings, and essential props.
Reconstruct: simplify anatomy and objects into sparse daily line illustration; remove most background detail; retain only 1–3 spatial anchors.
Line: medium-light black, organically wobbly, mild pressure variation, blunt ends, imperfect joins; no vector smoothness or uniform jitter.
Face: sparse adult face marks; upper-eye curve + small pupil; minimal nose and mouth; no realism or chibi exaggeration.
Fill: solid black masses; calm clean flat accent colors with only slightly hand-shaped edges; no marker texture, cloudiness, grain, or shading.
Canvas: white/near-white, generous negative space.
```

## Output

Return the completed illustration and a concise note naming the preserved subjects/relationship and the deleted background information. Do not present multiple variants unless the user asks for comparison.

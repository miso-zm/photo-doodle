# Quality gate

Approve only when all required checks pass.

## Content fidelity

- The actual people, pets, objects, pose, action, and relationship remain recognizable.
- Distinctive hairstyle, hair color/highlights, clothing silhouette/color, pet markings, and key prop are preserved when present.
- No fixed IP character or unrelated stock subject has replaced the photograph.

## Reconstruction

- The result is an illustration rebuilt from selected information, not traced photographic detail or a filter.
- Most background clutter and surface detail are gone.
- One to three anchors are enough to explain the space.
- Negative space remains generous.

## Style

- Line weight matches `assets/line-weight-anchor.png`.
- Wobble feels stroke-specific and natural, not mechanically smooth or uniformly noisy.
- Face uses sparse adult marks and avoids realistic or chibi conventions.
- Hair is a readable mass; actual dye/highlight colors are preserved.
- Black fill is solid.
- Colored fill is clean and calm, with no marker bands, cloudiness, grain, watercolor, pencil, shading, or decorative holes.

## Failure corrections

- Too polished: make long contours gently bow or kink; vary pressure slightly; relax terminals and joins. Do not add global jitter.
- Too realistic: remove lower lids, lip contours, nose modeling, skin shading, fabric folds, fur strands, and background texture.
- Too cute or childish: restore adult head/body proportion; shrink eyes; remove blush, lashes, round baby face, and chibi anatomy.
- Too generic: restore the source hairstyle silhouette, hair color placement, gaze, pose, garment shape, pet markings, and key interaction.
- Too busy: delete secondary props and reduce the environment to fewer anchors.
- Too empty: add only the single anchor or prop required to explain the action or place.
- Fill too synthetic: keep interiors flat and quiet; move handmade character back into contour rhythm and joins.

Reject the image rather than accepting a near miss when identity, relationship, face system, line character, or fill behavior fails.

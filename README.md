# VOXIS P002-WXR-001 — Dual Folio First Contact

A self-contained, no-framework WebXR proof of concept for **Meeting Without Merging**.

## Implemented

- Real 2r and 2v folio images as two independent VR objects.
- Quest controller trigger grab/release; controller movement and orientation move/rotate the grabbed folio.
- Floating controls: Scale −, Scale +, Opacity, Depth −, Depth +, Reset.
- Visible `2r.root` and `2v.central_y` anchor markers.
- Hard reset to a known starting state.

## Not implemented yet

- Alignment claims or residual scoring.
- Snapshot persistence / export.
- Two-hand scale.
- Pivot-locked rotation.
- Hand-tracking manipulation.

Those are intentionally deferred until this smaller instrument passes on the real Quest 3.

## Run on Quest 3

**WebXR immersive VR requires a secure HTTPS origin.** Put this entire folder on a static HTTPS host such as GitHub Pages, Netlify, or Cloudflare Pages, then open its HTTPS URL in Meta Quest Browser.

1. Open the hosted URL in Quest Browser.
2. Press **Enter VR**.
3. Aim at 2r or 2v and hold trigger to grab it.
4. Move/rotate the controller; release trigger to leave the folio in place.
5. Aim at the floating control dock and trigger a control.
6. Press **Reset** to restore the canonical starting configuration.

## First validation record

Mark each item PASS / FAIL / OBSERVATION:

- Both folios visible and stable in depth.
- 2r and 2v can be selected independently.
- Grab/release preserves the intended position.
- Controller orientation produces intuitive folio rotation.
- Scale control is useful and predictable.
- Opacity cycling helps comparison.
- Depth control materially changes how the relationship can be inspected.
- Anchor markers stay attached to the correct folio.
- Reset returns both folios to the known starting state.
- Frame rate and comfort are acceptable.

## Research boundary

**Geometry first. Measurement second. Meaning last.**

Geometric fit is a research aid, not proof of manuscript correspondence. A visually interesting configuration remains a configuration until separately measured and evaluated.

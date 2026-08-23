# P002-WXR-001 QA Report

## Verification status

### Static/code checks — PASS
- Embedded JavaScript parsed successfully with `node --check`.
- `index.html`, 2r, and 2v served successfully from a local HTTP server (HTTP 200).
- SHA-256 hashes recorded in `SHA256SUMS.txt`.
- No external JavaScript framework or CDN dependency is required.

### Browser surface — PASS with environment limitation
A Playwright-controlled system Chromium browser was used for the desktop surface at 1440×900. Direct navigation to localhost/file URLs is blocked by the execution environment administrator, so Playwright `set_content` was used with the exact HTML/CSS and inlined copies of the two PNG assets. The rendered browser surface was captured as `qa_desktop.png`.

The full runtime script was also loaded with Playwright. In this headless environment WebGL2 is unavailable, so the app correctly remained in desktop-preview mode with **no console/page errors**. This environment cannot validate immersive WebXR.

### Quest/WebXR interaction — PENDING REAL HARDWARE
Must be verified on the user's Quest 3:
- `immersive-vr` session entry.
- Controller target-ray selection.
- Trigger grab/release.
- Controller-pose movement/rotation.
- Scale, opacity, depth, and reset controls.
- Comfort and frame rate.

## Visual fidelity ledger
The generated design board is a direction/reference board rather than a user-approved production screenshot. The implemented primary surface preserves its central app language while intentionally omitting explanatory infographic panels from the live instrument.

1. **Core composition:** two independent folios, left/right, separated in depth — matched.
2. **Palette:** near-black research-space background, gold headings, cyan interaction accents — matched.
3. **Control model:** scale, opacity, depth, reset presented as a compact floating dock — matched; implementation adds explicit depth controls.
4. **Anchors:** distinct visual markers on 2r and 2v — matched; implementation uses cyan for `2r.root` and magenta for `2v.central_y` for stronger discrimination.
5. **Hierarchy:** experiment ID/title + short “Two folios. Two anchors. No merging.” framing — matched and simplified for readability.
6. **Live instrument vs. infographic:** side explanation panels and roadmap content from the concept are intentionally excluded from the live VR surface so they do not occlude research objects.

## Epistemic QA
- Raw folio assets remain separate objects.
- No alignment claim is generated.
- Reset establishes a known starting state.
- Provenance file retains folio/image IDs and named anchors.
- Snapshot persistence and residual measurement are intentionally deferred.

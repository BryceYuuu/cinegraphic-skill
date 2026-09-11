# Cinegraphic Skill

## Purpose
Transform a user-provided image into a cinematic graphic poster with mid-century modern composition, editorial illustration, geometric character rendering, oversized typography, limited color palettes, and analog print texture.

## Trigger
Use this skill when the user asks to:
- transform a photo into a vintage editorial poster
- create a cinematic graphic poster from a reference image
- use the Cinegraphic / 电影图形主义 style
- convert an image into a geometric, screen-printed, mid-century poster

## Workflow
1. Analyze the source image for subject count, pose, emotional relationship, camera angle, hierarchy, dominant colors, and negative space.
2. Choose the prompt mode:
   - Local/Open Model: maximum reference fidelity.
   - Hosted/Guardrail-Friendly: original reinterpretation from high-level visual structure.
3. Preserve the source's strongest visual hierarchy, not every detail.
4. Compress the palette to 3–5 colors.
5. Rebuild people and objects using geometric planes, angular shadows, strong silhouettes, and large flat color fields.
6. Introduce oversized typography as a structural graphic element.
7. Simplify secondary architecture and background clutter.
8. Add paper grain, screen-print or Risograph texture, uneven ink density, and slight registration offset.
9. Keep the final result cinematic, editorial, tactile, minimal, and deliberately designed.

## Prompt files
- `prompts/local-reference-faithful.md`
- `prompts/hosted-original-reinterpretation.md`

## Default visual constraints
- No glossy 3D rendering.
- No plastic skin.
- No random decorative clutter.
- No unnecessary gradients.
- No generic AI illustration look.
- Typography must participate in the composition rather than float on top.

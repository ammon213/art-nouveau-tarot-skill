---
name: artifact-template-art-nouveau-tarot
description: "Generate personal, original-character and anime tarot cards with delicate anime drawing, luminous ivory palettes and dense Art Nouveau botanical ornament. Use this reference-backed template when explicitly invoked or when this saved decorative card style is requested; not for divination or unrelated tarot styles."
---

# Art Nouveau Tarot

Generate one illustrated card using the retained visual reference. Read `artifact-template.json` and resolve all paths relative to this skill directory. Keep retained files unchanged and create new output files.

Read [references/style-guide.md](references/style-guide.md), [references/reference-index.md](references/reference-index.md) and [references/prompt-template.md](references/prompt-template.md) before generation.

## Reference and identity priorities

1. The user's explicit visual choice and requested deviations take priority. If the user selects an accessible generated illustration as a style target, use that exact image as the primary style reference rather than substituting a generic Art Nouveau interpretation. Inspect it first. Do not assume AI-generated franchise characters are original characters or legally cleared.
2. Otherwise, `assets/reference.png` (THE STARKEEPER) is the canonical style anchor. Supply its resolved path to the built-in image generation tool. A style description alone is not a substitute for actually passing the image.
3. A style reference controls drawing medium, line weight, face treatment, palette luminosity, detail density and decorative integration. The requested subject controls identity, proportions, costume and signature props. A new character does not require changing the drawing style.
4. Distinguish style, identity and edit-target roles in the tool prompt. A new subject needs a new face, gesture, scene and motif arrangement; do not transplant the reference person's identity or entire composition.
5. Use one anchor by default. Add the listed companion only if it addresses a concrete pose or palette need. Do not attach unrelated older experiments merely because they are present on disk.

## Simple input

A theme or one sentence is sufficient. Infer reversible design choices; clarify only materially missing identity or content.
- Personal theme: choose one main action and up to two symbols from supplied information. Without a portrait, use a fictional avatar; do not invent private traits or promise a likeness.
- Original character: create a new face, costume, pose, scene and symbolic arrangement.
- Known fictional character: preserve recognizable hair, facial cues, source proportions, costume colors and signature accessories. Do not automatically replace the costume with Victorian tailoring. Do not imply official status or ownership of the character.
- Real person: add the supplied portrait as an identity reference, with the style reference separately labeled.
- Prompt-only: provide a reusable prompt with one editable input line. For explicit text-only generation, omit all image-reference inputs and describe the output as a more approximate match.

## Generate and inspect

1. Inspect the chosen reference with `view_image` if unseen. Build the request with the prompt template, exact requested title, one action and a restrained theme palette.
2. Invoke the available built-in `image_gen` tool under the imagegen skill and its current schema. Use accessible reference paths where supported, or the appropriate recent-image mechanism, never both. If the reference is inaccessible, report the concrete limit instead of pretending it was passed; do not silently substitute another model or API.
3. Default to one complete roughly 5:9 portrait card, full body and both feet, with an integrated ornate border and small bottom title. Respect deliberate user-requested crops or layout changes.
4. Visually compare the actual output with the anchor. Check anime facial drawing, light color areas, fine lines, floral density, layered ivory architecture, scroll framing and readable silhouette. A dark sepia or naturalistic portrait is a material style mismatch even if it contains flowers and arches.
5. Repair observed mismatches with a focused edit using the actual result as target and the selected image as style support. Preserve identity and unaffected elements. Normally allow at most two repair attempts unless further optimization was requested.
6. Save final PNGs non-destructively in the workspace. Save prompts when sharing or reproducibility is requested. Report material limitations; do not claim exact repeatability from a prompt. Generate requested cards separately, not as a collage.

## Acceptance checks

- Complete edges and feet, exact readable title, no watermark, numbering, unrelated text or tabletop.
- Delicate anime face, graceful proportions, continuous fine charcoal/taupe lines and tiny interior detail. No realistic painted face, hard face shadows, glossy doll skin or thick comic outlines.
- Luminous ivory base, clean muted blue/green/lilac accents, gentle local shading and extremely faint print surface. No dark sepia cast, dirty parchment or heavy distress.
- Dense ordered plants and layered shallow architecture joined to carved-leaf scrolls and hanging fine ornaments. No sparse broad wall, square-badge/large-diamond-chain substitute or deep scenic panorama.
- Face, hands and main symbols readable; plausible contact between fingers and props; frame and figure use the same drawing medium.
- New content preserves reference-level craft without cloning the reference person, full pose/scene or exact border contours.
- New fictional subjects and image generation do not establish worldwide uniqueness or legal clearance.

## Provenance

The current two sample subjects are newly designed fictional archetypes. THE STARKEEPER was generated using a user-selected earlier AI illustration as a style input; THE GARDENER used THE STARKEEPER. The earlier input contains a known fictional character and is not bundled. These are image-backed generations, not text-only outputs. See the repository's COPYRIGHT.md for the source and rights boundaries.


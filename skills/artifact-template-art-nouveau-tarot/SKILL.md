---
name: artifact-template-art-nouveau-tarot
description: "Generate personal, original-character, and anime character tarot cards using this Art Nouveau Tarot public template and bundled text-generated references. Use for this saved decorative style or explicit template invocation; not for divination or unrelated tarot deck styles."
---

# Art Nouveau Tarot — public edition

Generate one illustrated card using the bundled visual system. Read `artifact-template.json` and resolve its reference and preview paths relative to this skill directory. Keep retained images unchanged; create new output files.

Read [references/style-guide.md](references/style-guide.md) and [references/reference-index.md](references/reference-index.md) when generating. Assemble the request using [references/prompt-template.md](references/prompt-template.md). All paths are relative to this skill, not the original author's computer.

## Input and identity

A one-sentence theme or a character name with its work is enough for a first result. Infer routine reversible design choices. Ask only when missing identity, form, or content materially changes the result.
- Personal theme: select one clear action and at most two primary symbols from the supplied information. Without an appearance reference, use a fictional avatar and do not claim an accurate likeness or invent private biography.
- Original character: design a new face, costume, scene, prop relationship and motif arrangement; do not reproduce a bundled reference person as the user's subject.
- Named fictional character: preserve recognizable hair, body proportions, age, costume colors and signature props. Character identity overrides the sample's Victorian clothing. Do not imply the character or its rights belong to this project, or that the result is official.
- Real person: use a user-supplied portrait as an identity reference in addition to the style reference. Do not quietly substitute a fictional avatar while promising likeness.
- Prompt-only or text-only: return a reusable prompt with one editable final input line. For an explicit no-reference generation, omit all image-reference inputs and explain that matching may be more approximate.

## Generation

1. Use `assets/reference.png` as the style anchor. Add at most one relevant companion from the reference index when it solves a concrete pose, age or palette need. Inspect local images with `view_image` when needed; label style and identity roles explicitly.
2. Invoke the available built-in `image_gen` tool, following its current schema and the imagegen skill. Default to a single approximately 5:9 vertical card, with complete edges, full body, integrated border, modest title plaque, one action and two primary symbols. Supply resolved local reference paths when supported; do not combine path references with recent-image inclusion. Use neither mechanism for an explicit text-only mode.
3. Treat a new subject as new image generation. For an actual edit, clearly identify the edit target and the elements that must stay unchanged.
4. Inspect the actual image against the selected style reference. Fix a clear observed defect with a focused edit and preserve the best version; for routine requests, stop after at most two repair attempts unless further optimization was requested.
5. Save final images non-destructively to the current workspace. Save the final prompt when sharing or reproducibility is requested. Report the result and material mismatches. Generate requested cards separately rather than replacing them with a collage.

## Checks

- Complete border and feet, readable exact title, no watermark, unrelated text or photographed tabletop.
- Fine ink contours, restrained shading, ivory architectural panels, botanical integration and the public edition's square-rosette/diamond-chain border.
- Readable face, hands and principal symbols; plausible contact between fingers, tools and objects.
- Preserve requested identity and source-specific costume; do not replace it with a generic sample person.
- Do not claim perfect fidelity, worldwide uniqueness, legal clearance or ownership of existing fictional characters.
- If references cannot be accessed, report that limit rather than pretending referenced generation occurred. Do not silently switch to an API/CLI or install software.

## Public provenance

The four distinct bundled cards were generated from written briefs without input images. They portray invented archetypes rather than existing franchise characters. The artwork and prompts for this public edition were newly prepared; prior private references and character demonstrations are not included. See the repository's COPYRIGHT.md for rights and review boundaries.


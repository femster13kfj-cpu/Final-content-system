# Kyndle Cover Design System v2 (Editorial Surrealism)

Evidence base: five adarshxdesign covers (Montserrat, Pinterest, Carousels, Colors, Master Covers), the creator's highest-engagement covers and Karoni's picks. v1 extracted one cover's look; v2 extracts the system underneath all five. Consistency comes from the invariants; diversity comes from the variables.

## The invariants (every cover, non-negotiable)

1. **Vast natural world + one small figure.** Scale contrast is the signature: a lone figure dwarfed by meadow, hills, sky, sunset field, or mountains. Figure is faceless or back-turned so the viewer projects themselves. Nature is ALWAYS the world; interfaces appear only as floating props, never as the environment.
2. **A dedicated type zone.** One low-clutter region (dark sky, bright sky, misty valley) is engineered to carry the typography.
3. **The keyword-scaled headline.** Setup words small; ONE power word detonated at 2-4x their size (pinterest, CAROUSELS, colors, covers). Every cover hook must contain a single word able to carry the frame alone.
4. **Metadata strip:** [DATE] left, [HANDLE] center, [CATEGORY] right, small all-caps. CATEGORY is the magazine-section label of the post's topic (AI MARKETING, LOCAL SEO, META ADS, SOCIAL MEDIA), rotating per post.
5. **Topical UI props.** One or two flat interface elements from the topic float in-scene: font toolbar, engagement-stat pills, color pickers, mini cover cards, AI prompt bar. The prop is the topic's fingerprint.
6. **The hand-drawn squiggle arrow** with a 2-3 word accent tag, pointing into the scene.
7. **Museum-label caption** near the bottom, 2-3 short lines, exactly one phrase highlighted in the accent color.
8. **Editorial poster feel:** photoreal scene + flat graphic overlay, generous margins, no logos, no clutter.

## The variables (rotate per cover)

1. **Setting library** (extend freely, keep it nature): starry night meadow, rolling grass hills, sky-as-curtain reveal, sunset flower field, misty mountain valley.
2. **The luminance rule.** Type color derives from the type zone's brightness: DARK zone = white setup + Kyndle green keyword (display tint #2BD99F). LIGHT zone = black type, with green demoted to micro-accents (a swatch, one caption phrase, one sub-line word). This rule, not a fixed dark background, is what allows palette diversity.
3. **Palette derives from the scene**; the constant thread is Kyndle green #1D9E75 appearing somewhere in the graphic layer on every cover, and navy #1A1A2E grading the dark zones.
4. **Figure matches topic** when possible: samurai for mastery, walker on a path for choices, robot for AI, business owner for founder topics. The Concept Engine's literalization moves choose the figure and scene.
5. **Occlusion depth (optional):** the figure or UI prop may overlap the headline's SETUP words for depth, never the keyword. The keyword stays fully legible at all times (set 5 observation, slide-system.md Part 6).

## Type system

- **Balboa** for the headline stack, sub-line rows, and metadata strip. Keyword at 2-4x setup size, tight leading.
- **Shadows Into Light** for the caption paragraph and accent tags.
- Optional sub-line row under the headline: small caps fragments with ONE word in green ("FOR EVERYTHING  INSTEAD  TRY THESE WEBSITES").
- Luminance rule governs all type colors. Generated text approximates fonts; brand-exact type = hybrid path.

## UI prop library (topic > prop)

fonts > font-selector toolbar | engagement/strategy > like/comment/share stat pills | color > color-picker panel | covers/design > mini cover cards | AI > prompt input bar | local SEO > map pin + review stars bar | ads > metrics card | websites > browser address bar | leads > DM/notification pop

## Generation recipe (unchanged from v1, condensed)

1. Two-layer prompting: describe the photographic layer fully, then the flat graphic overlay element by element, exact strings in double quotes.
2. Accent color lives ONLY in the graphic layer, never as light inside the photo.
3. Text is the failure point: short strings, proofread every character, one typo = regenerate.
3b. Cover gate: the Cover Design Checklist and 3-Second Test (formats/carousel.md and written/carousel-hooks.md). 5/5 or don't post.
4. Three concepts per cover via the Concept Engine, grade, pick.
5. Consistency levers: this spec verbatim + an approved cover saved as a Higgsfield reference element + same model (Nano Banana Pro, 4:5, 2k).
6. Hybrid fallback: scene-only generation + type applied in template whenever brand-exact Balboa/Shadows Into Light is required or text misrenders twice.

## Master prompt template

"[SCENE: vast natural setting from the library, one small back-turned figure matched to the topic, shallow depth of field, cinematic]. [TYPE ZONE: which region is kept clean and whether it is dark or light]. Overlaid flat graphic design elements on top of the photograph: a soft emerald green (#1D9E75) gradient bar bleeding off the top edge; a small all-caps metadata strip reading "[DATE]" left, "[HANDLE]" center, "[CATEGORY]" right; a headline in bold condensed display sans-serif: small setup line "[SETUP WORDS]", then the single word "[KEYWORD]" at three times the size in [white/green per dark zone | black per light zone]; [optional small caps sub-line row with one green word]; a small flat [UI PROP] floating in the frame; a two-word accent tag "[TAG]" with a thin hand-drawn squiggle arrow pointing at the figure; a small centered caption in a delicate handwritten font reading "[CAPTION]" with the phrase "[HIGHLIGHT]" in emerald green. Editorial magazine poster, photorealistic scene with flat vector overlay. The green appears only in the graphic elements. No text other than the quoted strings. No watermark."

## Kyndle brand adaptation (locked; the default profile's values)

These are `clients/kyndle.md`'s values, shown as the worked example. A client cover swaps in that client's profile values; the system's invariants and the luminance rule stay identical.

- Navy #1A1A2E | Green #1D9E75 | Display tint #2BD99F (large green headline text on dark zones only)
- Balboa (headlines/titles) + Shadows Into Light (captions/subtitles/tags)
- Alignment note (RESOLVED, Aug 2026): the lead-magnet PDF runs Path B because no Balboa desktop file exists to embed. PDF spec: Anton for the title band (closest free Balboa stand-in at display scale), Oswald for checklist item titles, Shadows Into Light for the subtitle and footer sign-off (brand-exact, Google Fonts), Archivo for body. Carousels remain real Balboa via the design template; the PDF is the only surface on the stand-in.

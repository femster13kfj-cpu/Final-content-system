# Blog Module

The repo side of blog content. The `kyndle-blog-skill` already exists as a complete pipeline for kyndleaisystems.com (SERP research, answer-first structure, GEO checklists, infographics, WordPress draft push, GBP/Slack delivery, daily keyword-queue automation) and it stays THE authority for Kyndle's own blog end to end. This module never overrides it. This module owns the three things the skill doesn't: client blogs, the hook-grade pass on titles, and the repo integrations (profiles, performance loop, atomization).

## Division of authority

| Concern | Owner |
|---|---|
| Kyndle blog: keywords, research, structure, HTML, images, WordPress push, GBP updates | kyndle-blog-skill, unchanged |
| Client blogs: same intelligence, client brand values, client publishing stack | This module |
| Title and meta grading (rubric pass) | This module, both cases |
| Performance logging and promotion | This module via `/performance/` |
| Blog-to-social atomization | This module via `/hooks/` |

## The shared ladder (one taxonomy everywhere)

The skill's funnel stages and the ads module's awareness map are the same Eugene Schwartz ladder wearing different labels. Use them interchangeably; never invent a third scale:

| Blog stage | Awareness stage | Ads equivalent | Hook families |
|---|---|---|---|
| TOF | Problem aware | Cold | Educational + Fear & Mistakes |
| MOF | Solution aware | Warm | Authority + Proof & Numbers |
| BOF | Most aware | Retargeting/hot | Offer, guarantee, match + differentiate |

## Titles are written hooks wearing a keyword

A blog title serves two masters: the query (keyword must appear, 55-65 characters, question format) and the click (it competes on a SERP against nine other results). The skill's format rules stand; this module adds the grade:

1. Generate 5 title options inside the skill's constraints, pulling from the written patterns of the row's hook families above.
2. Grade with `hooks/grading/rubric.md`. The claim-not-topic rule applies inside the question format: "What Should a Fence Cost in Dallas?" describes; "What Should a Fence Cost in Dallas? (Most Quotes Hide This)" provokes and still carries the keyword.
3. BOF titles follow the Google ads logic (match + differentiate): mirror the query, then add the one differentiator competitors' titles lack.
4. Meta descriptions get the same pass: 150-160 characters, keyword present, graded as a written hook because on the SERP that's exactly what it is.

## Client blog workflow

**Step 0.** Active profile from `/clients/`. Palette and type govern the images, the receipt inventory supplies the human-layer element every post needs, the no-go list gates claims, and city/service area come from the profile, not from Kyndle's.

**Step 1.** Stage and keyword per the shared ladder; batch as TOF/MOF/BOF clusters with link equity flowing to the client's money page, same authority flow the skill uses.

**Step 2.** Research per the skill's framework (SERP format scan, AI Overview check, PAA harvest, competitor gap, length calibration) plus the repo's Step 1.5 rules: named sources, no invented stats, the gap is where the post lives. Cannibalization check runs against the CLIENT's domain.

**Step 3.** Structure per the skill's answer-first rules, compressed here for sessions where the skill isn't loaded: first paragraph answers the title's question in 40-60 standalone words (snippet bait), H2s are real PAA questions each answered answer-first, one comparison table, FAQ block of 3-5 pairs, Article + FAQ schema, city in the first 100 words, minimum two internal links and one external authority link. When the skill IS available, its references are the deep source; this paragraph never overrides them.

**Step 4.** Images via the visual layer in the client's brand system. The featured image is a graphic-format piece (hooks/formats/graphic.md) on the client's palette; interior infographics follow the one-glance bar from the slide system.

**Step 5.** Grade (titles, meta, and the post against both of the skill's checklists), then package: markdown or HTML + images + metadata in a build doc. Publishing runs on the client's stack; WordPress clients can reuse the skill's REST payload shape pointed at their domain, others get the package for their platform. The draft-only rule is inherited absolutely: nothing auto-publishes on a client site, ever.

## Atomization (the multiplier)

Every published blog is pre-researched source material for the organic formats, and the research is already paid for:

- The snippet-bait paragraph is a written post opener one edit away.
- A listicle post's H2s are a carousel's slides; the FAQ block is the receipt slide.
- The post's strongest stat is a stat-slide graphic.
- The flow also runs backward: an organic winner in the performance log is validated demand, and its topic goes to the front of the blog keyword queue.

One rule: atomized pieces re-run the hook workflow for their format. A blog title that grades A as a title is usually a C as a cover; formats keep their own gates.

## Performance: the slow clock

Blogs enter `performance/log.md` like everything else but on their own cadence, because organic search compounds instead of spiking: log at publish, numbers at 30 days and 90 days (rankings for the primary keyword, organic entrances, leads attributed). Goal metric by stage: BOF = leads, MOF/TOF = rankings and entrances plus internal-link clickthrough toward BOF. Winners promote their TITLE pattern to the written examples file; a post that ranks is a written hook that beat the SERP.

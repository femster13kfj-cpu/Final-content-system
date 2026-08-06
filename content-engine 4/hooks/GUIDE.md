# Hooks Module

This module creates hooks for any piece of content. A hook is the first thing a person sees, hears, or reads. Its only job is to stop the scroll and earn the next three seconds.

## The three hook layers

Every hook belongs to one of three layers. Most content formats stack more than one layer at the same time.

| Layer | What it is | Folder |
|---|---|---|
| Verbal | The first words spoken out loud in a video | `/hooks/verbal/` |
| Written | The first line someone reads: a post opener, caption first line, headline, or cover text | `/hooks/written/` |
| Visual | What the eye lands on first: the opening frame, cover slide, thumbnail, or graphic design choice | `/hooks/visual/` |

## Which layers each format needs

This is the most important table in this module. Load it before generating anything.

| Format | Layers required | Format file |
|---|---|---|
| Video (short or long form) | Verbal + Visual + Written | `formats/video.md` |
| Carousel | Visual + Written | `formats/carousel.md` |
| Written post (LinkedIn, Facebook, X, any platform) | Written | `formats/written-post.md` |
| Graphic image | Visual + Written | `formats/graphic.md` |

A short video is really three hooks firing at once: what they hear, what they see, and the caption line under it. Treat each layer as its own deliverable.

## Workflow

Follow these steps in order every time.

**Step 0. Identify the brand.**
Which profile in `/clients/` is this content for? Load it before anything else. No client named = `clients/kyndle.md`. All brand values, receipts, and ramps below come from the active profile; a gap in the profile gets flagged, never guessed at, and never filled from another brand's profile.

**Step 1. Identify the format AND the goal.**
Format: video, carousel, written post, or graphic. The format decides which layers you build.
Goal: capturing leads, authority, virality, connection, or educational. One goal per piece of content. The goal decides which pattern section you pull from in every layer.
If either is unclear, ask. Do not guess.

**The stacking rule:** when a format needs multiple hook layers, every layer pulls patterns from the SAME goal section in its folder. A lead-capture caption under a virality cover slide works against itself. All pattern files in verbal/, written/, and visual/ are organized by the same five goals for exactly this reason.

**Step 1.5. Research the substance (automatic, every piece).**
Research runs for EVERY topic, no exceptions; automation never waits on the user.
- **The one context ask.** At the start of creation, ask ONCE: "Any context, results, or observations you want in this one?" Accept "no" instantly and proceed. When Karoni does contribute (a client result, an audit finding), his firsthand material is the strongest receipt available and leads the content.
- **The mandatory research pass**, scaled to the topic, gathers:
  1. Current facts and platform changes (anything that could have shifted recently gets verified, never assumed)
  2. Industry data from named, credible, checkable sources; original sources over aggregators
  3. A competitor gap scan: what the most visible content on this topic already says, and what it MISSES. The gap is where the post lives.
  4. The unique angle: synthesize the research with the repo's verified dataset and Kyndle's own receipts so the piece says something the top content doesn't
- Every stat ships with its source named. Deep or multi-source needs route to the Kyndle research skills.
- Hard floor unchanged: if a claim can't be sourced at any level, do NOT invent support. Reframe to what's backable, mark it as opinion, or flag it. Invented stats and fake cases are automatic rubric fails.
- Research output feeds the hooks: findings, the chosen angle, and the receipt list get decided BEFORE any hook is written, so hooks are built on substance instead of decoration.

**Step 2. Load the format file.**
Read the matching file in `formats/`. It contains platform-specific rules, length limits, and placement notes for that format.

**Step 3. Load the pattern files for each required layer.**
For each layer the format needs, read that layer's `patterns.md` and work only within the section matching the content's goal (plus patterns tagged "Also serves" that goal). Only pull `templates.md` if the user wants fill-in-the-blank structures, and only pull `examples.md` if the user asks for inspiration or you need proof a pattern works.

**Step 4. Generate.**
Produce 5 hook options per required layer unless told otherwise. For multi-layer formats, present the options grouped by layer, then recommend one combined set (one verbal + one visual + one written) that works together as a unit.

**Step 5. Grade.**
Read `grading/rubric.md` and grade every option A through F. Show the grade next to each option with a one-line reason.

**Step 6. Revise.**
Any option graded C or below gets rewritten using `grading/revision-playbook.md` before it is shown, or is cut entirely. Never present a C or lower to the user.

**Step 7. Run the ramp check.**
Before the content ships, name its off-ramp in one line (lead magnet, offer, or conversation) and confirm it aligns with the topic, per `conversion/funnel.md`. A missing ramp is flagged like a C-grade hook: allowed only as a deliberate decision, never as an oversight.

**Step 8. Capture winners.**
If the user says a hook performed well in the real world, offer to add it to `swipe-file/inbox.md` with the format, platform, and result noted.

## Folder contents

```
hooks/
├── GUIDE.md              You are here
├── conversion/
│   └── funnel.md         Signal x Trust x Ramp x Offer; the ramp check; receipt tiers
├── verbal/
│   ├── patterns.md       Named verbal hook patterns by goal, with when-to-use notes
│   ├── structure.md      The Continuous Hook System: re-hooks, timing, pacing
│   ├── templates.md      Fill-in-the-blank spoken openers
│   └── examples.md       Real spoken hooks that performed, with context
├── written/
│   ├── patterns.md       Named written hook patterns by goal, with when-to-use notes
│   ├── templates.md      Fill-in-the-blank first lines and headlines
│   ├── examples.md       Real written hooks that performed, with numbers and ADAPT IT lines
│   └── archive/          Full source libraries kept for variety mining
├── visual/
│   ├── patterns.md       The eight visual hook families + goal sections (build pending)
│   ├── templates.md      Repeatable visual hook setups
│   └── examples.md       Descriptions of real visual hooks that performed
├── formats/
│   ├── video.md          Rules for video hooks, short and long form
│   ├── carousel.md       Rules for carousel cover hooks
│   ├── written-post.md   Rules for post openers by platform
│   └── graphic.md        Rules for single-image graphic hooks
├── grading/
│   ├── rubric.md         The A through F grading criteria with receipt tiers
│   └── revision-playbook.md   How to fix each common hook failure
└── swipe-file/
    └── inbox.md          Raw dump of winning hooks, sorted later
```

## File conventions

- Every pattern in a `patterns.md` gets a name, a one-line description, when to use it, and one short example.
- Every entry in `examples.md` includes the platform, the format, and why it worked or what it did numbers-wise.
- Keep each file focused. If a file grows past roughly 300 lines, split it and update this GUIDE.

# Content Engine

This repository is a content creation system designed to be plugged into Claude. It is organized into modules. Each module is a top-level folder with its own GUIDE.md that contains the full workflow for that module.

## How to use this repo

1. Identify what the user is trying to create.
2. Open the matching module folder below.
3. Read that module's GUIDE.md first. It tells you exactly which files to load and in what order.
4. Never load an entire module into context at once. Load only the files the GUIDE.md tells you to load for the task at hand. This keeps sessions fast and token-efficient.

## Brand profiles (load first)

`/clients/` holds one profile per brand: palette, type, voice, ICP, receipts, ramps. Before any content work, load the ACTIVE PROFILE: the client the user names, or `clients/kyndle.md` by default. Every brand value referenced in the modules (colors, tints, fonts, handles, receipts, guarantees) resolves to the active profile; Kyndle's values appear inline in module files as the worked example. Receipts never cross profiles. See `clients/README.md`.

## Modules

| Module | Folder | Use when the user wants |
|---|---|---|
| Hooks | `/hooks/` | Any hook: verbal, visual, or written. For videos, carousels, written posts, or graphics. |
| Performance | `/performance/` | Logging a published piece, entering its numbers, writing a verdict, promoting winners, diagnosing flops. |
| Ads | `/ads/` | Any paid ad: Meta or Google. Ad copy, headlines, ad creative, compliance and message-match checks. |
| Blog | `/blog/` | Blog posts. Client blogs, title/meta hook grading, blog-to-social atomization. Kyndle's own blog pipeline stays with the kyndle-blog-skill. |

More modules will be added over time. When a new folder appears at the root, check for its GUIDE.md and add it to this table.

## Rules that apply across every module

- Always generate multiple options, never a single answer. Default to 5 unless the user asks for a different number.
- Always grade your own output against the module's rubric before presenting it. Show the grade.
- Match the user's platform and audience. Ask which platform if it is not stated and it changes the output.
- Write in a natural, human, conversational tone. No em dashes, no corporate filler, no AI-sounding phrasing.
- When something performs well in the real world, it belongs in that module's swipe file. Offer to save winners.

## What this repo is not

This is not a general knowledge base. Every file exists to be pulled into a working session and used. If a file would never be loaded during a real task, it does not belong here.

# Content Engine

A modular content creation system built to be plugged into Claude.

## What this is

This repo holds the ideas, examples, templates, and rules that power content creation sessions with Claude. Instead of pasting context into every chat, Claude reads what it needs directly from this repo.

## Current modules

- **Brand profiles** (`/clients/`): one file per brand the engine serves. Loaded first in every session; Kyndle is the default. See `clients/README.md`.
- **Hooks**: verbal, visual, and written hooks for videos, carousels, written posts, and graphic images. See `/hooks/GUIDE.md`.
- **Performance**: the loop that makes the repo learn from our own results. Log published pieces, promote winners, diagnose flops. See `/performance/GUIDE.md`.
- **Ads**: paid versions of the hook system for Meta and Google, with compliance and message-match gates. See `/ads/GUIDE.md`.
- **Blog**: client blogs, title grading, and blog-to-social atomization; reconciled with the kyndle-blog-skill, which keeps owning the Kyndle site pipeline. See `/blog/GUIDE.md`.

## How to plug it into Claude

- **Claude Code / Cowork**: open this repo as the working directory. Claude reads `CLAUDE.md` automatically and routes from there.
- **Claude chat**: share the raw GitHub link to `CLAUDE.md` at the start of a session, or paste the relevant module's GUIDE.md.

## How it grows

New capabilities get added as new top-level folders, each with its own GUIDE.md. The root `CLAUDE.md` keeps the master list.

## Maintenance

- Winning hooks from the real world go into `hooks/swipe-file/inbox.md` as they happen.
- Sort the inbox into the right patterns and examples files monthly.
- Review the rubric quarterly and update it based on what actually performed.

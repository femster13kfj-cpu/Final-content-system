# Brand Profiles

One file per brand the engine creates content for. This folder is what turns the repo from a Kyndle tool into agency infrastructure: every module reads its colors, type, voice, receipts, and ramps from the ACTIVE PROFILE instead of hardcoding them.

## How the active profile works

1. At the start of any content session, identify which brand the content is for. If the user names a client, load that client's file. If no brand is named, the default is `kyndle.md`.
2. Load the active profile BEFORE loading any module files. Every "Kyndle mapping" in the style files is really a profile mapping; Kyndle's values stay inline in those files as the worked example.
3. Wherever a module references brand values (palette, display tint, type pair, handle, category labels, receipts, ramps, guarantee), substitute the active profile's values.
4. Receipts only ever come from the active profile or fresh research. NEVER use one brand's receipts, case numbers, or results in another brand's content. This is the hard wall between profiles.
5. If the active profile has a gap the task needs (no display tint defined, no receipts at the needed tier), flag the gap and ask; never borrow from another profile to fill it.

## Files

- `_template.md`: the blank profile. Copy it to start a new client.
- `kyndle.md`: the house brand and the default active profile.
- One file per client after that, named with the client slug.

## Maintenance

- New client results get added to that client's receipt inventory with a funnel tier number (hooks/conversion/funnel.md) as they happen. Client wins are also Kyndle receipts (a named pattern of client results is tier 4 for Kyndle); log them in both files, worded for each.
- When the performance loop promotes a winner, note which profile it ran under; a hook that wins for a roofer may need regrading for a med spa.
- Review each profile at the monthly swipe-file sort: stale offers, dead keywords, and outdated receipts come out.

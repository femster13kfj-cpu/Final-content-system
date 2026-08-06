# Ads Module

Paid versions of everything the hooks module already knows. Meta and Google ads are Kyndle's core service, and an ad is a hook with money behind it: the same layers (written, visual), the same conversion math, but hard character limits, platform policy walls, and a landing page instead of a comment keyword. This module adapts; it does not duplicate. Pattern files, the Concept Engine, the rubric, and the funnel all still live in `/hooks/` and get loaded from there.

## The two big shifts from organic

1. **The goal is fixed.** Organic content picks one of five goals. Paid traffic exists to capture leads or sales; the ramp and offer are built into the ad unit itself. So in ads, the AWARENESS STAGE of the audience replaces the goal as the pattern selector: it decides which pattern families carry the hook, while the conversion machinery stays constant.
2. **Compliance is a gate, not a suggestion.** Hooks that win organic can be policy violations paid. Every ad passes the platform's compliance gate before it ships, full stop.

## The awareness map (the pattern selector)

| Audience stage | Who they are | Pull hook patterns from | The job |
|---|---|---|---|
| Unaware / problem-aware (cold) | Feel the pain, haven't named it | Educational + Fear & Mistakes families | Name the problem sharper than they can; brand arrives late |
| Solution-aware (warm) | Know solutions exist, comparing | Authority + Proof & Numbers families | Differentiate with receipts; why this one |
| Product-aware (retargeting) | Know the brand, haven't acted | Offer-led: guarantee, risk reversal, urgency | Remove the last risk |
| Most-aware (hot retargeting) | Ready, need a nudge | Straight offer, deadline, simplest path | Make acting easier than not acting |

The funnel's multiplication rule maps onto the ad unit cleanly: the creative and opening line are SIGNAL, the receipts in the copy are TRUST, the click is the RAMP, the landing page is the OFFER. When an ad gets clicks but no leads, the zero is usually on the page, not in the ad.

## Workflow

**Step 0. Brand profile.** Load the active profile from `/clients/`. Ads consume more profile fields than anything else: the offer, the guarantee wording, the receipt inventory, and the no-go list are the raw material. Receipts never cross profiles, and in paid this is also a legal line: results claims in ads need real substantiation, and testimonials need permission. An empty receipt tier means the ad angle changes, never that a receipt gets invented.

**Step 1. Platform, objective, awareness stage.** Which platform file to load, what the campaign optimizes for, and who is seeing it. If the stage is unclear, ask; cold copy shown to a retargeting audience wastes money in both directions.

**Step 2. Research (Step 1.5 rules apply, plus two ad-only sources).**
- The **Meta Ad Library** scan: what competitors are actively running, how long their ads have survived (longevity is the closest public signal to "this ad works"), and what angle NONE of them use. The gap rule from organic research applies verbatim.
- The **landing page read**: the ad must match the page it sends to. Pull the page's headline and offer before writing a word; message match is graded later.
- A **policy check** when any doubt exists: ad policies shift and get enforced unevenly, so verify the current rule for the vertical at build time instead of trusting memory. This module's compliance notes are the known walls, not a substitute for checking.

**Step 3. Load the platform file.** `meta.md` or `google.md`. They carry structure, character limits, placement specs, and the platform's compliance walls.

**Step 4. Generate.** Five options per slot, per the repo's global rule. Meta: primary text variants, headlines, and creative concepts via the Concept Engine. Google: the headline set and descriptions. Creative pulls the visual layer with the ad-specific constraints in the platform file.

**Step 5. Grade, with two extra gates.** The rubric grades every hook as usual, then:
- **Compliance gate:** any option that fails the platform's policy walls is cut, not revised into ambiguity. If the strongest angle is a policy risk, find the compliant reframe (the platform files show the standard moves).
- **Message-match gate:** the ad's promise and the landing page's headline must agree the way a keyword and its deliverable agree in organic. A mismatch is a zero factor; flag it even when the ad itself grades A.

**Step 6. Log it.** Ads enter `performance/log.md` like everything else. The goal metric for paid is leads and cost per lead; CTR and CPM are context. The 48h/7d cadence still applies, and losers get the same one-line zero-factor diagnosis, which for ads very often reads "the page, not the ad."

## Creative: two modes, chosen deliberately

1. **Branded editorial:** the cover system (minus the metadata strip) at ad sizes. Signals quality; fits solution-aware and retargeting audiences who are evaluating the brand.
2. **Native feel:** deliberately un-designed, reads like a person's post or a phone photo. Often outperforms polish on cold audiences because it doesn't pattern-match to "ad." Still passes the 3-Second Test; native is a style, not an excuse for a weak hook.

Both modes run 4:5 for feeds (the carousel sizing already in the system) and 9:16 for stories/reels placements. Safe zones per the platform files.

## Folder contents

```
ads/
├── GUIDE.md     You are here
├── meta.md      Meta: structure, limits, placements, compliance walls, Special Ad Category triggers
└── google.md    Google: RSA structure, character limits, search-intent hook logic, policy walls
```

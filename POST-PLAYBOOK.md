# POST-PLAYBOOK.md — How FFG posts get made (skill-in-progress)
# ─────────────────────────────────────────────────────────────────────────────
# STATUS: in-flux. PULL WHEN: writing any FFG post / building the post-writing skill.
# Purpose: capture the REPEATABLE process for writing a Festival Field Guide post on
# WordPress, so it can be codified into a Claude skill. Derived from post #10
# (electrolytes) + validated/expanded on post #2 (earplugs). n=2 before we lock a skill.
# NOTE: BLOG-SPEC.md describes a DIFFERENT platform (Next.js/MDX for flowstateslc.live).
# FFG is WordPress — only the *concepts* (experience-interview anti-slop, AI-does-plumbing)
# transfer; the mechanics below are FFG/WordPress-specific.
# ─────────────────────────────────────────────────────────────────────────────

## THE PHASES (the emerging template)

### PHASE 1 — RESEARCH (AI, parallel)
Four streams (from post #10):
- MONEY — which products have affiliate programs, networks, rates, cookie length.
- SCIENCE / TRUST — the E-E-A-T angle competitors miss (electrolytes: hyponatremia).
- SPECS — real per-product spec table (verified vs current labels, not stale plan data).
- SERP — what ranks now, difficulty, what the top posts miss (the gap to exploit).
Output: a research brief + a synthesis of the ANGLE (the honest tension = the hook).
[earplugs log: TBD]

### PHASE 2 — EXPERIENCE INTERVIEW (Nick, 5-10 min) — the anti-slop core
Targeted questions extract Nick's REAL first-hand experience. Never fabricate.
Reserve "we use this" for products actually used; others get confident spec verdicts.
[earplugs question set + Nick's answers: TBD]

### PHASE 3 — DRAFT IN VOICE (AI)
Draft in RAVE DADDY voice (REFERENCE FFG VOICE) from research + experience blocks.
Proven post skeleton (post #10 + #2): short-version/picks → why it matters → E-E-A-T/safety
angle → "won't this ruin X?" reassurance → verdict cards (picks) → comparison table →
"how Rave Daddy runs it" method → FAQ → bottom line, signed Rave Daddy. ~1,500-1,900 words.
- LINKING (Nick, post #2): link every AFFILIATE product at EVERY decision point — short
  version, verdict card CTA, table pick row, closing. Not just the CTA button. ~4-5 links
  per product is healthy. AFFILIATE PRODUCTS ONLY (no-program picks stay unlinked per the
  PLAIN-LINK RULE). Short version especially MUST have links (scanners decide there).
- Persona/byline = RAVE DADDY. "we"/crew voice, "I" for personal anecdotes.
- Anti-slop = Nick's real interview answers woven in (his scare, his exact phrasing).
[earplugs (#2) draft: post 54, draft, ~1500 words, Eargasm/Loop/Alpine picks. Done.]

### PHASE 4 — SPEC VERIFY + SKU TAGS (AI)
Verify every spec against current product pages/labels (agent). Add SKU tags.
[earplugs: TBD]

### PHASE 5 — SEO (Rank Math) — MUST use the Gutenberg editor (NOT REST)
Rank Math meta is NOT REST-writable (rank_math_* not exposed). Steps (browser):
1. Open post in editor → click Rank Math score button (top bar).
2. Focus Keyword = the target (e.g. "best earplugs for festivals").
3. Edit Snippet → custom SEO TITLE (<60 chars, keyword FIRST) + meta DESCRIPTION
   (~150 chars, MUST contain keyword). Don't leave the %title% template (too long).
4. Put the EXACT keyword phrase in the BODY opening (first ~100 words) so "keyword in
   content / at beginning" checks pass. Edit body via REST, but FIRST navigate the editor
   tab AWAY so its autosave doesn't clobber the REST change.
5. Save. Purge LiteSpeed. Target 60+ (post #2 hit ~63+, post #10 = 61).
GOTCHA (confirmed post #3-5): Rank Math meta CANNOT be set via REST (403) OR via the
wp.data `rank-math` store + programmatic savePost() (updateAppData sets the store but does
NOT persist to postmeta — a fresh load shows the default %title% template). MUST use the
real UI: click Rank Math score button → type in Focus Keyword field → Edit Snippet → clear
+ type custom Title + Description → close modal → click the Save BUTTON. Verify persistence
by reloading and reading wp.data.select('rank-math').getTitle(). Tip: keyword usually already
in title/URL/body (we write the intro note with it), so the only failing check is meta
description — fixing that + a <60char title gets to green.
[earplugs (#2): title "Best Earplugs for Festivals (2026): Honest Hi-Fi Picks", kw in
title/desc/url/body. DONE.]

### PHASE 6 — FEATURED IMAGE
Dispatch an agent to source ONE Unsplash-licensed (free commercial) landscape photo,
download to scratchpad. Then: upload to /media, set alt_text + caption (photographer
credit), set featured_media on the post, add a small "Photo: X via Unsplash" credit line
at the post foot. [earplugs (#2): crowd shot, Aditya Chinchure. DONE.]

### PHASE 7 — PUBLISH-PREP CHECKLIST
- [ ] Em dashes removed (Nick rule) — convert to commas/periods
- [ ] Branded components used in body (.ffg-verdict / .ffg-note / comparison table) — post #10 UNDER-used these; DO BETTER
- [ ] Category assigned (not Uncategorized)
- [ ] No Amazon links (hard rule)
- [ ] Internal links to/from hub + sibling posts
- [ ] Disclosure present/linked (site-wide footer — already done)
- [ ] Author byline = brand name, not personal email  ← still an open bug

### PHASE 8 — PUBLISH
WP REST publish (status=publish). Verify 200. Purge LiteSpeed cache.

### PHASE 9 — AFFILIATE LINKS (when approved)
Impact `transformLinks` may auto-convert approved-merchant links (no manual cloaking).
Otherwise Pretty Links `/go/` cloaking. LMNT-type (no program) stays plain honest link.

## OPEN QUESTIONS FOR THE SKILL (resolve by end of post #2)
- Which phases can AI do fully solo vs need Nick? (research=solo, interview=Nick)
- Templatize the experience-interview question set BY product category?
- Lock the post skeleton as a reusable outline?
- Build a components-usage rule (when to wrap in .ffg-verdict vs plain)?
- Standing publish-checklist as the skill's final gate.

## POST LOG
| # | topic | date | words | SEO | notes |
|---|-------|------|-------|-----|-------|
| 10 | electrolytes | 2026-07-13/14 | 1873 | 61 | LIVE. Voice interview + 4-stream research. Components under-used. |
| 2 | earplugs | 2026-07-14 | ~1600 | 63+ | LIVE /best-earplugs-for-festivals/. Rave Daddy byline. 4-stream research + interview. Affiliate-only picks (Loop/Eargasm/Alpine), unlinked table rows for no-program. Links at every decision point. Science cited (WHO/CDC/NIDCD). Needs affiliate-link swap on approval. |
| 115 | RV camping | 2026-07-15 | 1888 | 68 | DRAFT /renting-rv-for-festival/ (Camping cat 15). Decision/logistics post, not a product roundup — "verdict cards" = rental platforms (Outdoorsy earned pick + RVshare honest-alt). Honest thesis: costs MORE, sells what the extra buys. Interview-driven (Nick RVs every festival). SEO done. PARKED before featured-image + publish (needs app pw). Sibling TENT post still to write. |

### GOTCHAS (session 2026-07-15, camping build)
- **Create a post via REST WITHOUT the app password** using the logged-in session nonce
  (`window.wpApiSettings.nonce`): base64 the HTML in Bash → inject the b64 string into
  `javascript_tool` → decode with
  `new TextDecoder('utf-8').decode(Uint8Array.from(atob(b64),c=>c.charCodeAt(0)))` (UTF-8 decode
  needed for the `·` middot in verdict bands). `POST /wp-json/wp/v2/posts` with `X-WP-Nonce` header,
  `author:1`. Set category + status the same way (or in-editor). Cleaner than curl when browser-only.
- **Featured-image upload is the ONE step that resists browser-only.** base64-inject blows context
  (base64 tokenizes ~6.5 tok/char through Read — a 152KB b64 file = 144k+ tokens; do NOT Read it),
  and `mcp__claude-in-chrome__file_upload` NO LONGER accepts host/scratchpad paths. → Do the media
  upload with the **app password + curl** `POST /media` (Content-Disposition filename + --data-binary),
  or have Nick drag the file into the Media Library. Compress first (sips -Z 1100 + q52 ≈ 114KB).
- **Rank Math persistence reconfirmed** (n=3): editor UI only. After Save, verify with
  `wp.data.select('rank-math').getTitle()`. Category is safe to set in the editor Categories panel.
- **Editor-open vs REST clobber:** navigate the post's editor tab AWAY (to a clean page) before any
  REST edit to that post; only navigate after the editor is SAVED (clean) or a beforeunload dialog
  blocks the extension.

## SKILL-READINESS (n=2 reached 2026-07-14)
We now have TWO fully-worked posts (electrolytes #10, earplugs #2) run through the same
phases. Enough to draft the skill. What proved REPEATABLE across both:
- 4-stream parallel research (money/science/specs/SERP) → then interview → draft.
- Interview works BEST conversational, ONE question at a time (not a wall of 8).
- Skeleton is stable: note-hook → short-version(with links) → why-it-matters(science) →
  "won't this ruin X?" reassurance → verdict cards → honest table → "how Rave Daddy runs
  it" → FAQ → bottom line, signed Rave Daddy.
- Fixed gates every time: no em dashes, no Amazon, affiliate-only picks + links at every
  decision point, branded components (.ffg-verdict/.ffg-note/table), category, featured
  image + credit, Rank Math via editor, purge cache.
Still one-off / needs a 3rd post to confirm: exact interview question set per category;
how much science depth; whether transformLinks removes the need for /go cloaking.

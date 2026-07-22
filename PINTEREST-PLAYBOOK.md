# PINTEREST-PLAYBOOK.md — Operating Manual (real-data, 2026)
# ─────────────────────────────────────────────────────────────────────────────
# STATUS: locked. PULL WHEN: building/running the Pinterest side of the business.
# Sourced from primary docs (Pinterest Engineering + Help + policy, FTC code,
# Amazon agreement, SEC filings, Tailwind's 1.2M-pin study). Guru myths flagged.
# ─────────────────────────────────────────────────────────────────────────────

## HOW RANKING WORKS (2026)
- Two-stage recommender: retrieval -> transformer RANKING (TransAct V2, real,
  arxiv Jun 2025). NOT "16,000 signals" (garbled), NOT the legacy "four factors,"
  NOT any guru "algorithm override system."
- Distribution signals: ENGAGEMENT (saves > outbound clicks > pin-clicks >
  impressions), text relevance (title/description/board/linked domain), board
  relevance (tight niche board beats generic), FRESHNESS, image quality.
- SAVES = top value signal (design to be saved). OUTBOUND CLICKS = the money
  metric (design to be clicked out).
- Traffic decline since ~Feb 2025 is REAL but UNQUANTIFIED (no verified %). It's
  Pinterest deliberately keeping users on-platform for shopping — MAU still GROWING
  (553M->570M). Not a penalty. -> DIVERSIFY off Pinterest.

## NEW-ACCOUNT RAMP (plan for the lag)
- Wks 1-4 ~zero. Pins sit 45-60 days before visibility. Meaningful traffic
  60-90 days. Traction 3-6 mo. Compounding 6mo+. REAL MONEY = year 2.
- Safe cadence new account: 3-5 FRESH pins/day. Judge over 2-3 weeks, not days.
- Throttles a new account: mass-follow bursts, rapid mass-repinning, duplicate/
  near-dup images, low-effort AI-spun bulk, aggressive link-posting before trust.

## FRESH PINS (the #1 lever)
- "Fresh" = a NEW IMAGE + text for a URL (spectrum). New image on a REPEAT URL =
  ~64-77% of a brand-new pin's reach. You do NOT need new blog posts constantly.
- One blog post -> 5-15 fresh pins over WEEKS (new design/angle/title each),
  spaced 3-7 days between pins hitting the same URL, each on its most-relevant board.
- Repin value COLLAPSED. Group boards + Tailwind Tribes = DEAD. Don't build on them.

## PIN SPECS + DESIGN
- Idea vs Standard pin = OBSOLETE (merged May 2023; all pins link now). Ignore any
  "Idea pins can't have links" advice.
- Static 2:3 image pin, 1000x1500, = the CLICK ENGINE. Video (vertical 2:3-9:16,
  6-15s) = a reach/discovery layer, not the traffic driver.
- Design that converts (Tailwind 1.2M-pin study): HIGH CONTRAST + light/near-white
  backgrounds win (87/100 top colors were light; only 4% of viral pins used the
  brand's own palette). Raw lifestyle photos win fashion/beauty; designed text-
  overlay wins quotes/decor. Amateur photos are fine (0% used pro tools).
- Text overlay: 3-7 words, sans-serif, high contrast, hook formulas (numbers /
  time / results / problem). One pin = one message = one CTA. Keep safe zones
  (bottom ~790px is Pinterest UI — no CTA there).
- ALT TEXT: add it every pin (accessibility + keywords). The "+123% clicks" stat
  is vendor-sourced — do it, don't believe the number.

## PINTEREST SEO / KEYWORDS
- Free research: search AUTOCOMPLETE, GUIDED-SEARCH tiles, Pinterest TRENDS
  (trends.pinterest.com, 12-mo volume, compare 4 terms).
- Put keywords in (priority): pin TITLE (front-load), DESCRIPTION (natural, no
  stuffing), BOARD title + description (name boards EXACT keyword phrases, not
  cute/branded), alt text.
- DEAD: hashtags (no ranking value), first-comment keyword stuffing (myth).

## RICH PINS + SITE CLAIMING
- Claim your domain (business account, meta tag / file / DNS) -> attribution +
  DOMAIN ANALYTICS. Rich Pins (Article type) render automatically via Open Graph/
  Schema, no application/validator.
- HONEST: neither is a documented SEARCH-RANKING boost (Pinterest's own docs make
  no such claim — "rich pins boost SEO" is a myth). Only the Verified Merchant
  Program / shopping surfaces have a documented distribution benefit. Set up
  claiming + rich pins for attribution/analytics, not as a ranking lever.

## AFFILIATE MECHANICS (pin -> blog -> link)
- Direct affiliate links ARE allowed (Pinterest reversed the ban in 2016) — but
  "in moderation," disclosed, NO cloaking/deceptive redirects, NO bulk/repetitive
  affiliate pinning, NO fake-saving your own links.
- AMAZON: no Pinterest ban, but you must REGISTER your Pinterest profile in
  Associates, use NO masked links, and add Amazon's required disclosure. Verify in
  your live Associates settings.
- Other networks (Impact/CJ/ShareASale/Refersion): check EACH MERCHANT's terms —
  some ban social/coupon traffic.
- PREFERRED = BRIDGE: pin -> your full blog POST (affiliate links in the content).
  Wins: email capture, disclosure you control, retargeting pixel, multiple
  programs, you own the destination, sidesteps merchant social bans. The "bridge
  converts +30%" stat is funnel-seller myth — keep the rationale, ignore the number.
- WARNING: the bridge must be a FULL value-added post, NOT a thin one-CTA "doorway"
  page — Google penalizes thin-affiliate + doorway pages (spam policy). Direct
  linking is fine for low-ticket impulse; bridge for the winners.

## FTC DISCLOSURE (2023 guides — has teeth: fake-review rule, $50k/violation)
- Standard: "clear & conspicuous" = UNAVOIDABLE, BEFORE-the-click, plain language.
- BLOG: near the link / at the TOP before content or first affiliate link. NOT
  footer-only, NOT a separate disclosure page, NOT behind "more."
- PIN: disclosure in the VISIBLE pin DESCRIPTION before the click — not only on the
  destination page.
- Use "#ad" or a full sentence ("I earn commissions from links in this post").
  "#aff", "#sp", "collab", "#partner" alone are INADEQUATE. Amazon needs its exact
  line. Pinterest's paid-partnership label alone may be insufficient — add text.

## ACCOUNT SAFETY (domain blocks are the real killer)
- Bannable: cloaking/redirects to evade filters, pin-image-vs-destination mismatch,
  bulk identical affiliate pins, fake-save/engagement pods, buying followers/
  engagement, unapproved bots, mass inauthentic accounts.
- Link shorteners: use the NATIVE/direct URL even if long. "bit.ly = instant ban"
  is overstated; the real risk is unsupported/masking shorteners.
- Rate-limit blocks are real, NO published number; vary actions, most lift in 24h.
  Any guru quoting an exact daily pin cap is guessing.
- Tailwind is an OFFICIAL Pinterest partner (approved API) — schedulers don't ban
  you; unapproved browser bots do.
- DOMAIN BLOCKS = the catastrophic risk; appeals are slow/unreliable ("we won't
  unblock this site"). Protect it: ONE clean domain, native links, no cloaking,
  no thin/spam pages. You may not get it back.

## METRICS THAT MATTER
- OUTBOUND CLICKS (user LEAVES Pinterest for your URL) = the only metric that maps
  to revenue. Track it + outbound CTR. Pinterest Analytics separates: impressions
  / saves / pin-clicks (stay on-platform, semi-vanity) / OUTBOUND clicks / follows.
- Ignore monthly views + raw impressions as a scoreboard. 8k views + 400 outbound
  clicks beats 50k views + 200. Impressions measure appearances, not action.

## THE OPERATING STACK
- Blog: self-hosted WordPress.org + managed host (only thing that runs real ad
  networks + affiliate plugins + owns the SEO asset). Not Wix/Squarespace/Medium.
- Affiliate links: Pretty Links (~$99/yr, cheap start) -> Lasso (~$29/mo) once
  affiliate revenue justifies it.
- Email: MailerLite (start, free/cheap) -> Kit once automation/segmentation matter.
- Pinterest scheduling: Tailwind (~$18/mo, SmartSchedule + bulk pin creation) or
  free native scheduler.
- Analytics: GA4 + Google Search Console (free, mandatory) + Pinterest Analytics.
- Ads ladder: AdSense (day 1, tiny) -> Journey by Mediavine (1,000 sessions/mo =
  first real money) -> Raptive (25,000 pageviews/mo) -> Mediavine (25k sessions or
  $5k/yr). RPM $20-40 at the premium tiers; model conservatively.

## CONTENT SYSTEM (lean solo)
- Batch by FUNCTION (research / write / design pins / schedule), not by post.
- ~1 buyer-intent blog post/week (~40-50/yr). Templates: roundup, "best X", "X vs
  Y", review, tutorial, PACKING LIST/gift guide. One post -> many fresh pins.
- Content that CONVERTS: "best X" roundups, "X vs Y" comparisons, reviews, and
  PACKING LISTS/gift guides (Pinterest-native AND affiliate-carrying). Written for
  GOOGLE buyer-intent first, PINNED second (85% of affiliate clicks come from
  organic search, not Pinterest directly). -> This is exactly the "Survival Kit"
  pillar. Validated.
  ⚠ **CORRECTED 2026-07-15 — this line is GENERIC CATEGORY WISDOM, not niche-validated.**
  It was true for travel/food, where packing-list volume is enormous. TWO live probes on
  Nick's own account contradict it for THIS niche:
    · 07-03: "festival packing list exists but TINY vs outfits — NOT a Pinterest traffic driver."
    · 07-15: alive but its #1 result is a SELF-CONTAINED checklist infographic = the 0.1%-CTR trap.
  **LIVE NICHE DATA BEATS CATEGORY WISDOM. Do NOT "lead with" the packing list on Pinterest
  on the strength of this line.** See CONTENT-PLAN.md "LIVE PINTEREST PROBE #2" for the real map.
  ALSO CORRECTED: "'best X' roundups + 'X vs Y' comparisons are Pinterest-native" holds only for
  VISIBLE/WEARABLE gear (hydration packs → Backpack/Vest tiles). For INVISIBLE gear it is FALSE:
  "festival earplugs" returns ZERO guided tiles + a Shop module; "festival electrolytes" returns
  ZERO tiles + DIY drink recipes. Pin comparisons of things people can SEE.
  The 85%-from-organic-search line is the one to actually govern by: Pinterest is a SUPPLEMENT to
  Google here, never the affiliate engine.
- AI = scaffolding ONLY (outlines, keyword clusters, pin copy, research). NOT the
  ranking words. Google's HCU hammered scaled-AI affiliate content (71% of
  affiliate sites hit). You write the experience/opinion/review layer.

## THE 3-CHANNEL COMBO (the #1 winner-vs-loser differentiator)
- PINTEREST = ignition (fast traffic months 1-12 while Google ignores you).
- GOOGLE SEO = the compounding flywheel (slow, ~5.7% of pages reach top-10 in a
  year, but pays for years).
- EMAIL = the owned insurance policy (an algorithm can't delete your list). Capture
  it from DAY ONE (lead magnet on every high-traffic post).
- Single-channel dependence is what kills the 95%. Both Pinterest (Aug 2024 /
  Feb 2025) and Google (2024-25 core updates + AI Overviews) individually wiped
  out single-source operators.

## FAILURE MODES + CADENCE
- ~80% quit by month 18 — most "three months before the curve bends." Plan for a
  year-2 payoff, not year-1.
- Kills: quitting the dead window, thin/AI content hit by Google, single-channel,
  NO email list, chasing vanity metrics, buying the "how I make $10k on Pinterest"
  course (usually the course IS the income).
- Realistic solo cadence: 8-15 hrs/week. ~1 post/week. 2-5 fresh pins/day batched.
  Seasonal content pinned 45-60 days ahead. Months 1-3 near-zero (NORMAL), 4-8
  acceleration + first commissions + Journey at 1k sessions, 9-12 Google starts.

## FLOW-STATE-SPECIFIC NOTES
- BRAND-vs-DATA TENSION: Pinterest data rewards light/high-contrast pins; Flow
  State's aesthetic is dark/underground. Resolve by giving PINS a brighter, high-
  contrast treatment (test) while keeping the blog/brand core dark. Reach depends
  on it — don't force the dark aesthetic onto the pins untested.
- ⚠ **SUPERSEDED 2026-07-15.** (Was: "The 'Rave Survival Kit / what's in my fanny pack'
  packing-list = the exact highest-converting, Pinterest-native, Google-buyer-intent format.
  Lead with it.") Two live probes say otherwise for THIS niche — packing list is tiny vs outfits
  and its top pin is a self-contained infographic. The REAL Pinterest × money overlap is
  **FESTIVAL CAMPING** (5/8 probes route there; richest tile set; Pinterest curating boards;
  advertisers buying) — which is also the highest-AOV affiliate lane (Outdoorsy $60-110/booking).
  Lead with CAMPING on Pinterest, not the survival kit. See CONTENT-PLAN.md PROBE #2.
- DIVERSIFY from day one: Pinterest (new, ignition) + Google SEO + email + the
  existing TikTok 10k/IG 5k. Don't bet the business on Pinterest alone.

# ACTIVE.md — Working State
# ─────────────────────────────────────────────────────────────────────────────
# Only file that changes every session. Update at session end — never skip.
# ─────────────────────────────────────────────────────────────────────────────

## OPEN LOOPS

### BUILD — FESTIVAL FIELD GUIDE (Track A: standalone affiliate blog) ★ ACTIVE FOCUS
- **STATUS:** LIVE + PUBLISHING. **5-post hub-and-spoke cluster all LIVE + cross-linked**
  (electrolytes, earplugs, packing HUB, water packs, insoles), fully branded + DEFAULT DARK,
  legal pages live, RAVE DADDY persona, Impact tracking in. Post process codified in
  POST-PLAYBOOK.md (n=5) + **2 FFG skills built**. Now = affiliate approvals + more spokes.
- **LAST (2026-07-15 affiliate):** OPENED THE MONEY GATE. Built **AFFILIATE-TRACKER.md** (indexed)
  — every program's network / rate / cookie / apply URL / status, in network-first apply order.
  3 research agents verified ~20 brands current (2026): rate corrections (Alpine 12.5% not 15,
  Cure 20% flat not 25); NOTHING is Amazon-only. Key leverage: **AvantLink = 7 brands on one
  account** (Superfeet, Tread Labs, Salomon, Klean Kanteen, Helly Hansen, Outdoorsy, Hipcamp);
  Impact = 4 (Loop, Cure, CamelBak, Anker); Rakuten = Key Nutrients + Supergoop; Awin = Alpine;
  CJ = RVshare; self-serve = Nuun/Vibedration/iEDM/Eargasm. **iHeartRaves confirmed CLOSED** →
  swapped the hydration Best-Budget pick to **iEDM** (Refersion 10%/15d; live, links to their
  collection until stock+approval; zero iHeartRaves refs left). Nick STARTED applying (Awin account
  made + 254-char description written). Claude can't submit apps (needs Nick's tax/payment/ID).
  NEXT PREREQ for traffic (neither built): email capture (MailerLite + lead magnet) + reach post #1
  (50 Festival Outfit Ideas = the Pinterest traffic monster). Rec order: email capture → reach post.
- **LAST (2026-07-15 camping spoke):** WROTE THE FESTIVAL CAMPING SPOKE via ffg-write-post +
  ffg-publish skills. Nick's call: SPLIT into TWO posts (tent camping / RV camping) so honesty holds
  — Nick has NEVER tent-camped a festival (always RV, always Outdoorsy), so a "how I pitch a tent"
  post would be fabricated. Wrote the RV post FIRST (first-hand + highest-AOV lane). **Post #115
  DRAFT, slug `renting-rv-for-festival`, title "Renting an RV for a Festival (2026): Is It Worth It?
  The Honest Math", 1,888 words, Rave Daddy, 0 em dashes.** HONEST THESIS (Nick's correction, key):
  the RV does NOT pay for itself — it ALWAYS costs more than tenting; the post sells what the extra
  BUYS, not a fake break-even. $1,200 rig / split 6 = $200pp; food $20-30/meal; RV camping pass
  always costs MORE (the number rental blogs hide). Two insights no RV blog writes: (1) confirm the
  Outdoorsy owner ALLOWS FESTIVALS before booking (many prohibit it → lost rig/deposit); (2) fridge
  vs cooler = FOOD SAFETY (cooler can't hold safe temp 3-4 days in desert heat → forced $25 meals;
  fridge only comes with the RV). AC framed as heat-safety (tent-oven + alcohol false-coolness),
  cross-links electrolytes. Who it's NOT for: small crews (split 2 = $600 each), money-tight.
  Outdoorsy = earned first-person pick (pays $60-110/booking, MORE than RVshare's ~$45-66, so honest
  = profitable here); RVshare = honest "haven't used it" alternative card. WALMART pickup tip stays
  a PLAIN link — research confirmed Walmart pays $0 on grocery/pickup orders ("you don't get paid for
  grocery pickups"), so it's the LMNT case (best advice, no payout). RESEARCH (4 agents): money (camping
  affiliate table — Outdoorsy/RVshare/Shiftpod 365d-cookie/Jackery+GoalZero $400-2000 AOV), science
  (CO poisoning CDC-verified; ⚠ agent MISAPPLIED a mine-refuge-chamber study as "tent temps" — I cut
  it), SERP (primary kw "renting an RV for a festival"/first-time long-tail; head terms REI-walled).
  DONE in publish: Rank Math SEO (title 52/60, desc 142/160, kw "renting an RV for a festival", score
  68, persisted via UI), created + assigned CAMPING category (id 15), featured image sourced (RV
  trailer, Lance Anderson via Unsplash, /scratchpad/rv-up.jpg).
  ⚠ NEW GOTCHA (featured-image upload is HARD browser-only): base64-inject blows context (base64
  tokenizes ~6.5 tok/char via Read — a 152KB b64 = 144k+ tokens), `file_upload` NO LONGER accepts
  host/scratchpad paths, and curl needs the app password. → Featured-image upload = an APP-PASSWORD
  step, not a browser step. Nick chose browser-only this session so it's PARKED.
  NEW TECHNIQUE (worked): create a post via REST from the logged-in session nonce (no app password) —
  base64 the HTML in Bash, inject the b64 STRING into `javascript_tool`, decode with
  `new TextDecoder('utf-8').decode(Uint8Array.from(atob(b64),c=>c.charCodeAt(0)))` (handles the · middot
  in verdict bands). Author = user id 1 (Rave Daddy).
- **LAST (2026-07-15 pinterest probe):** ★ LIVE FESTIVAL-BROAD PINTEREST PROBE (8 terms, Nick's
  acct, guided-search tiles). Nick's framing: blog = bottom of funnel, build the funnel ABOVE it,
  work BACKWARDS from posts → keywords. FULL MAP + method + caveats → **CONTENT-PLAN.md "LIVE
  PINTEREST PROBE #2"**. Probe #1 (07-03) was rave-narrow; the festival cluster had NEVER been probed.
  THREE findings:
  1. ★ **CAMPING = the Pinterest × money jackpot, and the post DOESN'T EXIST.** 5/8 probes route to
     camping (packing list → Camping tile; coachella → camping tiles ONLY; hacks → Camping + Car
     camping; camping = richest set + Pinterest-CURATED boards + Amazon sponsored pins). It's also
     the highest-AOV affiliate in the plan (Outdoorsy $60-110/booking). Currently queued BEHIND
     cooling + sunscreen. **JUMP THE QUEUE — write camping next.**
  2. **THE VISIBLE/INVISIBLE LAW.** Pinterest carries festival gear that is VISIBLE/WEARABLE/SCENE-
     shaped; it does NOT carry invisible gear. hydration pack → Backpack/Vest/"Outfit with" tiles
     (ALIVE). earplugs → ZERO tiles + a "Shop" module. electrolytes → ZERO tiles + DIY drink recipes
     (intent = "make your own" = ANTI-affiliate). So of the 5 live posts only 2 are pinnable (hub +
     hydration pack); insoles PREDICTED dead (invisible) but UNTESTED. This corrects my own advice
     from earlier the same session ("pin the gear posts") — wrong for the invisible half.
  3. **"DOWNLOAD" = how to beat a self-contained incumbent.** Pinterest's guided tile AND Google's
     autocomplete independently surface download/template for "festival packing list". The #1 pin
     for the term is a complete screenshottable checklist (the 0.1% trap winning). You can't
     out-checklist it — a better image still gets saved, not clicked. The FILE is the one thing the
     image can't hold → the pin promises the PRINTABLE, never the list. This makes the prep-checklist
     magnet the pin's REASON TO EXIST, not a bolt-on, and it's a MATCHED magnet (5-15% vs 2-5%).
  FUNNEL: pin ("the printable festival packing list") → HUB → checklist magnet → email → gear posts.
  Gear posts fed by EMAIL + GOOGLE, never by Pinterest directly.
  ALSO FIXED: the PINTEREST-PLAYBOOK ↔ CONTENT-PLAN contradiction (both files edited). Playbook's
  "packing lists are Pinterest-native… lead with it" = generic category wisdom (true for travel),
  now marked CORRECTED/SUPERSEDED; live niche data wins. Its "85% of affiliate clicks come from
  organic search, not Pinterest" is the line to actually govern by.
  METHOD CAVEAT: guided tiles = content-ecosystem DEPTH, not search VOLUME. 8 terms, 1 acct, 1 day.
  Directional. Pinterest's typeahead API 403s (CSRF-gated) — read tiles off the search UI instead.
- **LAST (2026-07-15 strategy):** GATE 2 (email) opened → KANDI MAGNET KILLED + hub retargeted
  FESTIVAL-BROAD (live). Nick proposed a kandi-PDF landing page as the day-1 email play. 4 adversarial
  agents (traffic / SEO / audience-bridge / economics) → CONVERGENT KILL on all 4 axes:
  (1) TRAFFIC — Pinterest shipped TransActV2 (Feb 2025, Pinterest Engineering blog) optimizing for
  in-app engagement over outbound clicks; independently corroborates the vault's Feb-2025 outbound
  collapse. Kandi patterns are SELF-CONTAINED (~0.1% CTR vs ~5% recipes) — screenshot the pin, never
  click. The proposed fix (hide pattern, promise a 50-set PDF) is UNTESTED, no public data either way.
  (2) SEO — "how to make X" is the query class AI Overviews answer inline; 2-wk-old domain can't rank
  a head term; possible TOPICAL DILUTION (craft content on a gear domain may drag the 5 money posts).
  (3) AUDIENCE — Taylor Swift Eras Tour (2023) mass-popularized friendship bracelets → the volume is
  either polluted with Swifties/kids/hobbyists OR (if pure "kandi" jargon) far smaller than claimed.
  Fork kills it either way. Kandi's 10-mo dormancy also POISONS deliverability (ISP penalties ~3mo
  inactivity, spam traps ~12mo) — a liability against the later checklist list on the same domain.
  (4) ECONOMICS — sequencing inverted; approvals + checklist beat it on cost AND relevance.
  ⚠ THREE agents independently FAILED TO VERIFY the 748k-Pinterest / 33k-Google kandi numbers. Those
  are load-bearing in KEYWORD-MAP + this file and DO NOT hold up. Verify before betting on any of them.
  ⚠ METHOD NOTE: agents briefed to KILL return prosecution briefs, not verdicts. This batch inflated
  arithmetic (an itemized 14-20 hrs totalled as "98-104"), priced its preferred alternative
  credulously (camping spoke "$120-330/mo starting month 1-2" on a 2-wk-old domain = fantasy), and
  buried its own best counter-evidence (a real case: new blog → 60 daily visits after 3 wks pinning).
  Audit selection bias, not just arithmetic.
  CORRECTION TO MY OWN CLAIM: "Pinterest can't work here" was TOO STRONG. The intersection of
  {what Pinterest distributes} ∩ {what clicks} is THIN, not empty — "rave earplugs" is the #1 "rave"
  autocomplete = real gear demand, and a "Loop vs Eargasm" comparison is NOT self-contained. Nobody
  has measured Nick's account; the honest move is a ~4hr/$0 test, not more theory.
  SHIPPED LIVE (browser, Nick's logged-in Chrome): hub /rave-packing-list/ → /festival-packing-list/
  ("The Festival Packing List (2026)"), Rank Math SEO title + meta + focus keyword → "festival packing
  list" (score 67→71); all 4 spokes repointed (0 stale refs); earplugs title/meta widened → "Festivals
  & Concerts" (59/60). All 5 URLs 200, old slug 301s, hub-and-spoke intact. Rave Daddy + body copy
  untouched (persona locked; rave = feeder silo under a festival-broad scope).
  GOTCHAS: WP CORE does old-slug 301s natively (wp_old_slug_redirect) — Rank Math Redirections module
  NOT needed (was OFF; I wasted turns trying to enable it; its Modules grid also resists automation).
  Rank Math's FOCUS KEYWORD is NOT a ranking signal (plugin-internal score only) — the real dials are
  <title>/H1/slug/content. Rank Math stores a CUSTOM SEO title that OVERRIDES the post title, so
  changing the post title alone leaves <title> stale (confirmed live). Must-use-UI gotcha reconfirmed.
  FREE FIND: Rank Math's keyword autocomplete surfaced "festival packing list TEMPLATE / DOWNLOAD /
  2026 / camping / for girls / with kids / women" — template+download are LEAD-MAGNET-SHAPED queries.
  Google's own autocomplete says the prep-checklist magnet and the hub share intent = the MATCHED
  magnet case (5-15% conv vs 2-5% unrelated). Strongest evidence yet for checklist-first.
  ⚠ VAULT CONTRADICTION (unreconciled): PINTEREST-PLAYBOOK says packing lists are "Pinterest-native
  AND affiliate-carrying… Lead with it"; CONTENT-PLAN's LIVE probe says "festival packing list… tiny
  vs outfits, NOT a Pinterest traffic driver." Both dated 07-03, both marked authoritative. Resolution:
  playbook = generic category wisdom (true for travel), content-plan = live niche probe → live data
  wins. NEEDS AN ACTUAL FIX IN THE FILES.
  KEYWORD COVERAGE AUDIT: the 5 posts target ~1,500-2,500 combined searches/mo — the SMALLEST terms in
  KEYWORD-MAP. Its top-10 build list is ~unbuilt. Insoles + hydration-pack were written with NO keyword
  target at all (insoles appears nowhere in the map; map says "water bottle ~300", not hydration packs).
- **LAST (2026-07-15 audit):** FULL 5-POST REVIEW + FIX PASS (closed the REVIEW loop). Ran a
  multi-agent audit (voice, SEO/cannibalization, links/FTC, structure/brand) + a live mobile
  render pass. Fixed all P0/P1: above-fold FTC disclosure added to 4 posts (only electrolytes had
  one); hub-and-spoke made whole (earplugs+electrolytes had NO internal FFG links); cut a PHANTOM
  product ("Rave Runner 3L Dual") from the hydration table; electrolytes given Rave Daddy persona
  beat + signoff (predated the persona lock); CamelBak 404 repointed; hydration+insoles verdicts
  prose→bulleted picks. Then all 8 P2s: table template normalized (`Product` first-col + `Best for`
  on electrolytes); **site-wide MOBILE bug fixed** (posts scrolled sideways — `.content-area` was a
  fixed 848px flex item that wouldn't shrink; fix = wrap tables in overflow-x:auto scroll-boxes via
  REST + Customizer CSS `@media(max-width:880px){.content-area{width:100%!important}}`); insoles
  honest "skip" item; earplugs dB standards/NRR note; **FAQPage JSON-LD schema on all 5 posts**
  (injected in post content via REST — admin unfiltered_html keeps the <script>; Rank Math schema
  untouched, no dup FAQPage); earplugs retitled (was H1-dup "Honest Picks…" → "Save Your Hearing
  Without Killing the Music"). No-change-by-design: camping/Outdoorsy deferred to its future spoke;
  LMNT stays a deliberate non-affiliate link (honest #1 pick, DanceSafe pattern). All verified live.
  GOTCHA CONFIRMED: custom_css still 403 via REST → edited via logged-in Customizer wp.customize
  set()+previewer.save() in Nick's Chrome. NEW TECHNIQUE: FAQPage schema via content-injected
  JSON-LD (bypasses fragile Rank Math UI). Homepage "blank card" scare = Playwright lazy-load
  artifact, not a real bug (all 5 card imgs are valid 200s).
- **LAST (2026-07-15):** CLUSTER COMPLETE + SKILLS BUILT. Wrote & published 3 more posts →
  the 5-post cluster is all live + cross-linked: packing HUB (/rave-packing-list/), water packs
  (/best-hydration-pack-festivals/), insoles (/best-insoles-for-festivals/). Each: 4-stream
  research, conversational interview, Rave Daddy voice, licensed featured image (all different),
  Rank Math SEO. KEY GOTCHA: Rank Math SEO does NOT persist via REST or the wp.data store —
  MUST use the editor UI (cost a redo; now documented). New REFERENCE rule: MONETIZATION DENSITY
  (fill posts with money products; junk items = honest no-link advice). Hub trimmed to on-body
  (camping + cooling punted to future spokes). THEN built 2 skills in .claude/skills/:
  ffg-write-post (research→interview→draft→review) + ffg-publish (WP mechanics + gotchas), both
  referencing REFERENCE.md + POST-PLAYBOOK.md as source of truth. INDEX updated.
- **LAST (2026-07-14 eve):** Big session. PUBLISHED both posts: electrolytes #10 (was draft)
  + WROTE & PUBLISHED earplugs #2 (/best-earplugs-for-festivals/, ~1600w, Rank Math ~63,
  4-stream research + conversational interview). LOCKED "RAVE DADDY" persona: every post
  bylined + voiced by Rave Daddy (his crew's real name for him — packs extras, checks
  everyone's earplugs before the gates); WP display name set (fixes the email byline).
  Published the 4 legal pages (clean slugs; trashed default WP privacy squatter), stripped
  em dashes, comments OFF site-wide. Built FOOTER legal menu; header nav stripped to
  logo+name (GP ignored nav-none → CSS kill); transparent dark-mode logo (PIL-drawn,
  light-pine). Installed IMPACT tracking tag in <head> via WPCode Lite (verifies +
  transformLinks). Applied to Impact. NEW RULES locked in REFERENCE: no-Amazon-ever,
  plain-link=last-resort (affiliate picks only; no-program products = unlinked table rows),
  Rave-Daddy persona. Created POST-PLAYBOOK.md tracking the whole post-writing process →
  n=2, ready to build a /write-ffg-post skill. Cloudflare Email Routing set up but hello@
  still bouncing (Activity Log empty = sender-side DNS cache; retest later).
- **LAST (2026-07-14 pm):** STYLING PASS on live post pages — made them match the brand
  board. Diagnosed the mismatch: GeneratePress was painting its own container palette
  (white `--base-3`) over the brand, and the post sat in a flat, left-shoved right-sidebar
  layout. Fixes (all via Customizer Additional CSS `custom_css[generatepress]`, edited
  through `wp.customize().set()` + `previewer.save()` JS-inject in the logged-in customizer
  — NOT REST; the `custom_css` post type returns 403 in REST): (1) overrode GP vars
  (`--base`/`--base-3`/`--contrast`/`--accent`) to the brand palette; (2) restored field-
  manual DEPTH — paper ground → raised lighter plate w/ border+shadow → mid-tone inset
  cards, plus a CSS-only SVG topographic-contour texture on the ground; (3) DEFAULT DARK —
  ported the board's dark palette and applied it UNCONDITIONALLY (dark for ALL readers, not
  `@media`-gated); (4) CENTERED the reading column — hid the empty `#right-sidebar`,
  constrained `.content-area` to 848px margin-auto so topo ground gutters show both sides.
  Comparison table = pixel-match to board. Verified live via screenshots.
- **LAST (2026-07-14):** Polished post #10 (removed em dashes per Nick, verified all sodium
  specs vs 2026 labels via agent, added SKU tags, set Rank Math SEO title/meta/focus-keyword
  = 61/100, added licensed Unsplash featured image + credit + alt). Then BRANDING: locked
  direction FIELD-GUIDE EDITORIAL (brand board artifact + Nick "love this, sick"), built
  emblem logo (sun-over-contours) + full site CSS (Fraunces+Inter, pine/coral/marigold/paper
  palette, branded verdict/table/spec components). APPLIED LIVE via API + Customizer JS-inject:
  logo+favicon set, site title="Festival Field Guide", Additional CSS live (custom_css[generatepress]),
  Rank Math reset (deactivate/reactivate fixed its locked state — Nick completed the wizard).
  Site now fully on-brand: Fraunces headers w/ pine underlines, Inter body, branded comparison
  table (pine mono head + zebra + serif names), palette-matched hero image.
- **LAST (2026-07-13):** Massive build session. RESEARCH first: 3 agents (SERP + scope
  economics + domains) → pivoted plan to v2 — FESTIVAL-BROAD (not rave-narrow; RPM + AOV
  trap), electrolytes-first (earplugs SERP too hard), brand = FESTIVAL FIELD GUIDE.
  STOOD UP THE SITE: domain festivalfieldguide.com (Cloudflare registrar) → Hostinger
  Unlimited 12-mo → WordPress live, SSL working (Cloudflare A-record + proxy, NOT
  nameservers — Cloudflare Registrar forces its own NS). GeneratePress theme + Rank Math
  active. Permalinks=post name. Generated WP Application Password → REST API publishing
  CONFIRMED (Claude publishes via curl/python; creds in session scratchpad, not git).
  Drafted 4 legal pages (Disclosure/Privacy/About/Contact, IDs 6-9). Then 4-stream research
  on electrolytes (money/science/specs/SERP) → drafted first post "Best Electrolytes for
  Festivals" (ID 10, ~1,900 words) in Nick's voice via experience interview → pushed as draft.
- **KEY FINDINGS:** Money≠truth tension = the brand's edge (LMNT best by sodium but $0
  commission → feature it honestly; Key Nutrients best commission but token sodium →
  honest caveat). Cure downgraded to 4-6% (plan's 20-25% was stale). Hyponatremia/
  overhydration = the E-E-A-T angle competitors miss. Never route to Amazon (health=1%).
- **NEXT:**
  0. ⚠️ **IMPACT DENIED (account-level, 2026-07-15) → REAPPLY AT MILESTONE 3.** Not an Impact problem,
     a NEW-SITE problem (every network gates on traffic). Full milestone ladder + ungated reroutes in
     **AFFILIATE-TRACKER.md**. Denial costs $0 now (no traffic = link earns same as placeholder).
     ★★ HIGHEST-PRIORITY TASKS (the reapply ladder — do in this order):
       P1. ✅ DONE 2026-07-15 — Site Kit by Google installed + activated; Nick did the Google OAuth.
           GA4 property created (measurement ID **G-3063ZES3G7**, tag VERIFIED firing live) + Search
           Console CONNECTED + PageSpeed Insights. All 3 green in Site Kit → Settings. GA4 is now the
           traffic proof to screenshot at Milestone 3. (Data starts accumulating from today.)
       P2. 🔄 IN PROGRESS — grab JOINABLE-NOW affiliate links, then swap onto posts. Full per-brand
           routes + swap map + apply URLs in AFFILIATE-TRACKER.md (+ .csv for Sheets). Corrections
           this session: Cure = Impact-BLOCKED (declined, not ungated); Eargasm = Refersion (not
           in-house). ✅ RAKUTEN APPROVED (SID 4726466) → apply to Anker + Key Nutrients via Find
           Advertisers. Still to sign up (Nick's accts): Eargasm/Vibedration/iEDM (Refersion each),
           Nuun (UpPromote), Shiftpod (in-house, needs tent post). RAKUTEN SWEEP DONE = covers ~none
           of our categories (only Anker + Key Nutrients); don't re-sweep. Live-links-now set covers
           earplugs/electrolytes/hydration-budget/hub; insoles + premium-hydration = M3. As each
           approves → tell Claude the brand + link → Claude swaps + re-verifies (map prebuilt).
       P3. Finish publishing RV post #115 (featured image + publish + hub link + purge — needs app pw).
       P4. Write TENT post → then cooling/sunscreen/per-festival guide = reach 8-10 posts (Milestone 1).
       P5. Pinterest business acct + claim domain + pin the PINNABLE posts (hub/hydration/camping);
           run the ~4hr/$0 outbound-click test. Grow GA4 toward ~500 sessions/mo (Milestone 2).
       P6. At 8-10 posts + ~500 sessions/mo + verified social → REAPPLY Impact + AvantLink (Milestone 3).
           Reopens Loop (earplug pick) + Outdoorsy (RV money).
  2. TEST the ffg-write-post skill on the next SPOKE (cooling or sunscreen) — refine from use.
  3. hello@ email: ✅ WORKING (2026-07-15) — was sender-side DNS cache, cleared on its own.
     (Optional later: Gmail "Send mail as" if you want to reply FROM hello@.)
  4. **PINTEREST TEST (~4hr, $0).** NOT a build — an EXPERIMENT. Business acct + claim domain +
     pin + 2-4wks → read OUTBOUND CLICKS in Pinterest Analytics. Replaces theory + the vault's
     unsourced "1 click/day" with Nick's OWN number on his OWN account.
     ⚠ REVISED by the 07-15 probe — pin only what Pinterest actually carries:
     · PIN: the HUB (as "the PRINTABLE packing list", never the checklist image) + the hydration
       pack post (Backpack/Vest tiles = alive) + camping angles once that spoke exists.
     · DON'T PIN FOR REACH: earplugs + electrolytes (ZERO tiles; Pinterest reroutes to Shop / DIY
       recipes), insoles (predicted dead, untested). Outfits/makeup/kandi = the 0.1% self-contained
       trap — do NOT build a reach layer.
  5. **EMAIL = KIT, not MailerLite** (MailerLite BANS affiliate marketing verbatim — see plan §8).
     Magnet #1 = FESTIVAL PREP CHECKLIST (matched magnet, compiles from the 5 live posts in an
     evening, 5-15% conv vs 2-5% unrelated; Google autocomplete confirms "festival packing list
     template/download" = real demand). KANDI PDF = KILLED (see LAST 2026-07-15 strategy).
     Gate: email needs a traffic source — do it WITH the Pinterest test, not before.
  6. ★★ **FINISH PUBLISHING THE RV POST (#115, draft)** — 3 steps left, all need the APP PASSWORD
     (or a browser workaround): (a) upload featured image /scratchpad/rv-up.jpg + set featured_media
     + append photo-credit line ("Photo: Lance Anderson via Unsplash"); (b) status→publish; (c) add
     the HUB inbound link: in post 61, link the text "RV rentals" → /renting-rv-for-festival/ (exact
     hub sentence: "...its own (tent, sleeping setup, RV rentals, camp kitchen), so we're giving it a
     dedicated guide..." — this post IS that dedicated guide); (d) purge LiteSpeed; verify 200 + live
     <title>. NOTE: featured-image upload can't be done via browser base64 (blows context) — use the
     app password + curl POST /media, OR Nick drags the file into Media Library.
  7. ★ **WRITE THE TENT-CAMPING POST** (the sibling). Nick: "the most important post is for the tent
     people." Observed-not-lived vantage (Rave Daddy is the RV guy watching the tent city) — honest
     framing, never faked first-hand. Primary kw "first time festival camping" / "festival camping
     mistakes" (both LOW comp, winnable; head terms REI-walled). Science: CO poisoning (CDC-verified),
     tent-oven heat (state plainly, NO fake citation — the mine-study was cut), noise (cross-link
     earplugs). Cross-link to the RV post + hub. Money: Shiftpod (365d cookie), power stations, sleep
     gear — but most is Google-side (invisible gear per the Pinterest rule); camping-scene pins are
     the Pinterest play.
  8. AFFILIATE-TRACKER: add camping brands — Outdoorsy (AvantLink, $60-110/booking), RVshare, Shiftpod
     (365d cookie), Jackery/Goal Zero ($400-2000 AOV), + FLAG CamelBak's 7-day cookie (live on the
     hydration post, fights save-then-buy). Walmart = confirmed $0 on grocery/pickup, keep PLAIN.
     Other spokes after tent: cooling, sunscreen, portable charger.
     ★ ALSO: PER-FESTIVAL PACKING LISTS (coachella ~4k→15k Mar-Apr, edc ~3k) = the vault's own #1
     whitespace (per-festival logistics; travel incumbents ignore it), perfect intent adjacency to
     all 5 money posts, NOT self-contained. For GOOGLE these need PAGES (a pin never ranks); for
     PINTEREST one evergreen hub + per-festival SECTIONS/anchors + many pins avoids annual rewrite
     debt in the Feb-Mar window that collides with event busy season. Decide per channel.
  7. FIX THE VAULT CONTRADICTION: PINTEREST-PLAYBOOK ("packing lists = Pinterest-native, lead with
     it") vs CONTENT-PLAN (live probe: "festival packing list… NOT a Pinterest traffic driver").
     Live niche data should win; the playbook line is generic category wisdom. Not yet edited.
  8. Optional 1-word fix: hub intro still reads "The short version on a rave packing list" — the last
     stale string; changing it satisfies Rank Math's keyword-at-start check. Left per Nick's
     body-copy-untouched rule.
- **DONE (2026-07-15):** 5-post cluster fully LIVE + cross-linked (wrote+published+SEO'd+imaged
  3 new posts this session: hub, water packs, insoles). MONETIZATION DENSITY rule locked in
  REFERENCE. Built 2 FFG skills (ffg-write-post + ffg-publish) in .claude/skills/. POST-PLAYBOOK
  → n=5 (+ Rank Math must-use-UI gotcha documented). INDEX updated.
- **DONE (2026-07-14):** 2 posts published, Rave Daddy persona + byline, 4 legal pages live +
  footer menu, Impact tracking (WPCode), comments off, transparent logo, 3 REFERENCE rules
  (no-Amazon, plain-link, persona), POST-PLAYBOOK created. hello@ troubleshot (bouncing).
- **STACK/CREDS:** WP REST API base https://festivalfieldguide.com/wp-json/wp/v2/ ;
  user rabownick123@gmail.com + app password "Claude API" (scratchpad wp-creds.txt).
  Research artifacts + post HTML in session scratchpad.
- **VOICE:** locked in REFERENCE.md (FFG section) — "we"/crew, honest-but-clean, communal,
  confident-not-hedgy, honesty hook (feature best even if $0), NEVER fabricate testing.

### BUILD — Flow State Online (RESHAPED post-stress-test 2026-07-03)
- **STATUS:** cluster locked; BLOG ARCHITECTURE decided + self-contained build brief ready
- **LAST (2026-07-08):** Decided the blog architecture — build NATIVELY in the EXISTING
  flowstateslc.live app (custom Next.js on Vercel) at the /blog SUBDIRECTORY (NOT WordPress,
  NOT a new domain — best SEO + one codebase + AI-authorable). Posts = MDX content-as-code
  (AI writes file -> commit -> Vercel deploys). Anti-slop solved via "EXPERIENCE SKILLS" —
  exercises that extract Nick's real first-hand experience + real event photos, woven into
  each post. Wrote BLOG-SPEC.md (the system) + BUILD-BRIEF-blog.md (self-contained handoff
  for a fresh Claude Code session running INSIDE the flowstateslc.live repo).
- **PRIOR (2026-07-03):** Fixed vault to the reshape. Reconciled the Pinterest+blog role
  (top-of-funnel + affiliate audition, NOT the income engine). Ran LIVE Pinterest vertical
  validation on Nick's account -> locked the first 6-post cluster in CONTENT-PLAN.md.
  Findings: Pinterest discovery = OUTFITS + MAKEUP + KANDI only; sober/wellness = ZERO
  Pinterest demand (off-platform play); earplugs/gear = shopping/Google term, not Pinterest reach.
- **MODEL (reshaped):** NOT an affiliate/ads blog to replace income — 4 kill-tests
  killed that (a $50-500/mo hobby, wrong tribe, tiny/walled keywords, decaying
  channel). INSTEAD: Flow State = conscious/wellness/flow-state rave AUDIENCE +
  brand -> monetize via BRAND DEALS + EVENTS + OWN PRODUCTS + affiliate/ads FLOOR.
  Event company = the moat. AFFILIATE = the AUDITION (prove you drive sales ->
  convert to flat brand deals), NOT the income engine. Full verdict in REFERENCE.md
  (STRESS TEST section).
- **CHANNELS:** short-form video (TikTok/Reels — Nick has 10k) + EMAIL primary;
  Pinterest + blog = evergreen SEO/discovery + affiliate-audition layer (crucial as
  top-of-funnel + owned home, NOT the income engine). Cadence ~8-10 hrs/wk; content
  is marketing FOR the events (hours double-count).
- **NEXT (two parallel tracks):**
  A. BUILD THE MACHINE — hand BUILD-BRIEF-blog.md to a Claude Code session running INSIDE
     the flowstateslc.live repo -> it scaffolds /blog (MDX pipeline, component kit,
     products.ts, /go redirect, sample earplugs post). Then swap in real affiliate URLs
     + hero images (in ONE place), and wire <EmailOptin> to the ESP.
  B. WRITE POST #1 — run the EXPERIENCE SKILLS (BLOG-SPEC.md Part B). IMMEDIATE NEXT
     ACTION: the FIELD-TEST + HOT-TAKE interview on rave EARPLUGS -> real-experience
     blocks -> AI drafts the earplugs-review MDX. (Not started.)
  Then (post-blog): apply to first affiliates (Loop/Eargasm/Alpine/Cure/Today Glitter/
  Rave Doctor/TestKitPlus); pick + set up email ESP (MailerLite/Kit) + the two lead magnets
  (kandi pattern PDF + festival-prep/harm-reduction checklist); set up Pinterest business
  account + claim flowstateslc.live; batch fresh pins for the 3 REACH posts (outfits/makeup/
  kandi); verify non-alc beverage programs; build the outreach tracker + first pitches
  (Rave Doctor + local harm-reduction booth); lock the online brand identity.
- **CONTEXT:** $0, solo, US. Harm-reduction + sober-curious/wellness = richest, most
  on-brand lanes (+ Utah SB86 = local drug-checking legal edge). Affiliate converts
  on GEAR (earplugs/hydration), not outfits. Keep the events as the hard revenue layer.

### BRAND-PARTNER PIPELINE — Flow State
- **STATUS:** list built (ALIGNED-BRANDS.md); outreach not started
- **LAST:** Enumerated aligned partners across 7 lanes (earplugs, recovery, hydration,
  harm-reduction + local orgs, sober-curious/wellness, sustainable wear, non-alc
  beverage). Top 10 ranked. Event-activation pitch validated (brands pay for festival
  sampling: Liquid I.V. 1.7M units, Alpine/Eargasm booths, Cymbiotika local events).
- **NEXT:** verify non-alc programs -> outreach tracker -> draft + send first pitches.
  Pitch = affiliate audition + on-site event activation (the thing no pure creator offers).

---

# ─────────────────────────────────────────────────────────────────────────────
## SESSION LOG
# Append-only. One row per session.
# ─────────────────────────────────────────────────────────────────────────────

| DATE       | SUMMARY                                                       | LOOP CHANGES              |
|------------|---------------------------------------------------------------|---------------------------|
| 2026-06-30 | Set up vault. Captured business model + constraints. Drafted  | Opened: Niche + program   |
|            | Pinterest gap-research plan.                                  | research                  |
| 2026-06-30 | Ran Round 0 model validation (3 agents). Verdict = ADJUST     | Progressed: model         |
|            | (Pinterest<->SaaS intent mismatch). Awaiting A/B/C re-wire.   | validation; opened Round 1|
| 2026-06-30 | Round 0.5 live Pinterest probe. Demand CONFIRMED real;        | Progressed: model         |
|            | intent=templates, audience=young women. Favors Option B/C.   | validation                |
| 2026-06-30 | Round 0.5b: Pinterest stress-test biz terms + Impact map.     | Progressed: model         |
|            | POD/Shopify/Airtable dead; make-money wins; Squarespace=best. | validation                |
| 2026-06-30 | Round 1 content-gap sweep (3 agents + live Pinterest).        | Closed: Round 1 sweep;    |
|            | Anchor=profession-segmented templates (sell own + Envato).    | opened: launch decision   |
| 2026-06-30 | Chose Etsy + photographer silos. Two-layer model. Then deep   | Progressed then           |
|            | Etsy buyer dive -> Notion->Sheets pivot -> reframed to "Own   | challenged: brand thesis  |
|            | Your Business" media brand.                                   |                           |
| 2026-06-30 | 3 adversarial kill-tests INVALIDATED Etsy thesis (affiliate   | Closed/parked: Etsy       |
|            | dead, saturated, no migration, Pinterest=beginners). Closed   | thesis; opened:           |
|            | out. Nick pivoting to PHOTOGRAPHER space.                     | photographer space        |
| 2026-07-01 | Photographer space validated + KILLED (same wall). Meta-      | Closed: photographer;     |
|            | finding: Pinterest=beginners not operators (vehicle problem). | opened: strategic pivot   |
|            | Nick's EVENT COMPANY (Flow State) surfaced = the edge.        |                           |
| 2026-07-02 | Committed FLOW STATE. Full research: scene, affiliate         | Closed: direction +       |
|            | foundation, Pinterest playbook, keyword map. Consolidated to  | research; opened: BUILD    |
|            | FLOW-STATE-MASTER-PLAN.md. Pushed vault to private git.       |                           |
| 2026-07-03 | 4 adversarial kill-tests -> plan RESHAPED (not an affiliate   | Reshaped: BUILD loop;      |
|            | blog; audience/brand -> brand deals+events+products, affiliate| opened: brand-partner     |
|            | = audition). Built aligned-brand pipeline (ALIGNED-BRANDS.md).| pipeline                  |
| 2026-07-03 | Fixed vault to reshape. Reconciled Pinterest+blog role. LIVE  | Progressed: BUILD         |
|            | Pinterest vertical validation -> locked first content cluster | (cluster locked)          |
|            | (CONTENT-PLAN.md). Discovery = outfits/makeup/kandi only.     |                           |
| 2026-07-08 | Blog architecture: native Next.js /blog on flowstateslc.live  | Progressed: BUILD         |
|            | (NOT WordPress). MDX content-as-code + experience-skills anti- | (blog spec + handoff      |
|            | slop system. Wrote BLOG-SPEC.md + BUILD-BRIEF-blog.md handoff. | ready)                    |
| 2026-07-13 | Track A GO. Research → plan v2 (festival-broad, electrolytes-  | Opened: FESTIVAL FIELD    |
|            | first, brand=Festival Field Guide). Stood up full site: domain | GUIDE (Track A) — site    |
|            | (Cloudflare) + Hostinger + WordPress live + SSL + GeneratePress| LIVE, 1st post drafted.   |
|            | + Rank Math + API publishing. Drafted 4 legal pages + 1st post | Voice learnings + v2 plan |
|            | (electrolytes, 4-stream research + Nick voice interview).      | saved.                    |
| 2026-07-14 | Polished post #10 (em dashes out, specs verified+SKU tags, SEO | Progressed: FFG — post    |
|            | meta 61/100, licensed featured img). Designed + LOCKED brand   | publish-ready; brand      |
|            | (Field-Guide Editorial, board artifact) + APPLIED live: emblem | identity locked + applied |
|            | logo, Fraunces+Inter, palette, component CSS, site title. Rank | live. Visual identity in  |
|            | Math reset+wizard done. Site fully on-brand.                   | REFERENCE.md.             |
| 2026-07-14 | Styling pass on live post pages -> now match brand board: fixed | Progressed: FFG — post    |
|  (pm)      | GP container-palette override, restored field-manual depth      | pages match board; site   |
|            | (raised plate+shadow+SVG topo), set DEFAULT DARK for all,       | now default dark +        |
|            | centered reading column (killed empty right sidebar). Via       | centered.                 |
|            | Customizer CSS (wp.customize JS-inject; custom_css 403 in REST). |                          |
| 2026-07-14 | Published BOTH posts (electrolytes #10 + wrote/published earplugs| Progressed: FFG — 2 posts |
|  (eve)     | #2). Locked RAVE DADDY persona + byline. Published 4 legal pages | LIVE; persona locked;     |
|            | + footer menu, comments off, transparent logo, header=logo only.| Impact tracking in;       |
|            | Installed Impact tracking tag (WPCode). 3 new REFERENCE rules    | POST-PLAYBOOK n=2. Email  |
|            | (no-Amazon, plain-link, persona). Created POST-PLAYBOOK (n=2).   | routing still failing.    |
| 2026-07-15 | Wrote + published 3 more posts → 5-post hub-and-spoke cluster    | FFG cluster COMPLETE (5   |
|            | all LIVE + cross-linked (hub, water packs, insoles). Monetization| posts live). 2 skills     |
|            | -density rule. Built 2 FFG skills (ffg-write-post + ffg-publish).| built. POST-PLAYBOOK n=5. |
|            | Rank Math must-use-UI gotcha documented. INDEX updated.          | Next = affiliate approvals.|
| 2026-07-15 | FULL 5-post review + fix pass (multi-agent audit + live mobile).  | Closed: REVIEW loop. All  |
|  (audit)   | Fixed all P0/P1 (FTC disclosure x4, hub-spoke links, phantom      | P0/P1/P2 shipped + verified|
|            | product cut, persona, 404) + all 8 P2s (table norm, SITE-WIDE     | live. New: FAQPage-via-   |
|            | mobile sideways-scroll fix, FAQPage schema x5, retitle, etc).     | content-JSONLD technique. |
| 2026-07-15 | P2 started + Impact fallout. Cure DECLINED via Impact (Cure is  | P2 in progress. Rakuten   |
| (P2)       | Impact-only, not ungated - my error). Verified each P2 brand's  | approved (SID 4726466).   |
|            | true platform: Eargasm=Refersion, Anker=Rakuten-bypass, Cure=   | Cure blocked, Eargasm=    |
|            | Impact-blocked. RAKUTEN APPROVED (SID 4726466) - real gate      | Refersion (fixed). Rakuten|
|            | passed. Swept Rakuten directory: covers ~none of our categories | sweep=dry. CSV built for  |
|            | (only Anker + Key Nutrients; Backcountry/Osprey/Dick's/Superfeet| Sheets. Swap map ready.   |
|            | /iHerb all absent). Built AFFILIATE-TRACKER.csv (Sheets) + swap  |                           |
|            | map. Kept honesty rule: no pay-max recommendation swaps.         |                           |
| 2026-07-15 | P1 DONE — installed Site Kit by Google (Nick did OAuth). GA4     | P1 ✅. GA4 live            |
| (P1/GA4)   | property live (G-3063ZES3G7, tag verified firing) + Search       | (G-3063ZES3G7) + GSC      |
|            | Console + PageSpeed all connected. The Milestone-3 traffic proof.| connected. Data building. |
| 2026-07-15 | IMPACT DENIED (account-level). Research → it's a NEW-SITE, not   | Impact reroute: ungated   |
| (impact)   | an Impact, problem (all networks gate on traffic; AvantLink not  | now (Cure Ambassador/     |
|            | easier). Reframe: denial = $0 cost now (no traffic). Built the   | Eargasm/Anker direct),    |
|            | REAPPLY MILESTONE LADDER (GA4 → 8-10 posts → ~500 sess/mo →      | gated deferred to M3      |
|            | reapply Impact+AvantLink). Ungated reroutes: Cure Ambassador,    | reapply. Tracker + NEXT   |
|            | Eargasm, Anker direct, Shiftpod. Loop stranded (Impact-only).    | rewritten w/ P1-P6.       |
| 2026-07-15 | Wrote the FESTIVAL CAMPING spoke (ffg-write + ffg-publish        | RV post #115 DRAFT (SEO+  |
| (camping)  | skills). Split into TWO posts (tent / RV) for honesty — Nick     | category done). Featured  |
|            | never tent-camps. RV post #115 written (1888w, honest "costs     | image + publish PARKED    |
|            | more not less" thesis, Outdoorsy earned pick, festival-friendly  | (needs app pw). Walmart=$0|
|            | + fridge-safety insights). SEO score 68, Camping cat created.    | plain. TENT post = next.  |
|            | Featured-image upload blocked browser-only → app-pw step.        | New: REST-create-via-nonce|
| 2026-07-15 | LIVE FESTIVAL-BROAD PINTEREST PROBE (8 terms, guided tiles) —    | ★ CAMPING SPOKE PROMOTED  |
| (pinterest)| the festival cluster had NEVER been probed (07-03 was rave).     | to next build. Visible/   |
|            | ★ CAMPING = the Pinterest×money jackpot + the post doesn't exist | invisible law locked.     |
|            | (5/8 probes route there; Outdoorsy $60-110/booking). VISIBLE/    | Playbook↔Content-plan     |
|            | INVISIBLE LAW: hydration pack ALIVE (Backpack/Vest tiles);       | contradiction FIXED. Map  |
|            | earplugs + electrolytes ZERO tiles (Shop module / DIY recipes =  | → CONTENT-PLAN PROBE #2.  |
|            | anti-affiliate). "DOWNLOAD" tile + Google autocomplete = the     | Corrected my own "pin the |
|            | magnet is how you beat the self-contained checklist incumbent.   | gear posts" advice.       |
| 2026-07-15 | GATE 2 (email). Nick proposed a kandi-PDF capture page → 4        | KANDI MAGNET KILLED (4/4  |
| (strategy) | adversarial agents KILLED it 4/4 (TransActV2 + self-contained     | axes). MailerLite DQ'd →  |
|            | pins + AI Overviews + Eras-Tour-polluted volume + dormancy        | KIT. Magnet flipped to    |
|            | poisoning deliverability). 3 agents FAILED to verify the 748k/33k | prep checklist. Hub       |
|            | kandi numbers — vault premise unsound. MailerLite DISQUALIFIED    | retargeted festival-broad |
|            | (bans affiliate mktg, verbatim) → Kit. SHIPPED: hub → /festival-  | + LIVE. Next = Pinterest  |
|            | packing-list/ (~1k→~8k) + Rank Math + 4 spoke links + earplugs    | TEST (~4hr/$0), not more  |
|            | "& Concerts". Corrected my own too-strong "Pinterest can't work". | theory.                   |
| 2026-07-15 | Opened the money gate. Built AFFILIATE-TRACKER.md (3 agents       | Built: AFFILIATE-TRACKER  |
| (affiliate)| verified ~20 programs). Network-first apply order (AvantLink=7    | (indexed). iHeartRaves    |
|            | brands). iHeartRaves closed → swapped hydration budget to iEDM.   | closed → iEDM swap live.  |
|            | Nick started applying (Awin acct + description). Next: email+reach.| Apps in flight.          |

---

# ─────────────────────────────────────────────────────────────────────────────
## CLOSED LOOPS (Archive)
# ─────────────────────────────────────────────────────────────────────────────

### REVIEW — Full FFG blog audit
- CLOSED 2026-07-15. Multi-agent audit (voice, SEO/cannibalization, links/FTC, structure/brand)
  + live mobile render pass across all 5 posts. All P0/P1/P2 resolved + verified live. Key catches:
  4 posts missing above-fold FTC disclosure; broken hub-and-spoke (2 posts had no internal links);
  a phantom/invented product in the hydration table; a site-wide mobile sideways-scroll bug
  (fixed-width flex `.content-area`). Added FAQPage schema to all 5 (content-injected JSON-LD, a
  reusable technique). No true keyword cannibalization; voice mechanically spotless. Only defers:
  camping/Outdoorsy (waits for its spoke), LMNT link (kept non-affiliate by policy). Full detail
  in the FFG loop's 2026-07-15 audit LAST entry.

### Model validation (Rounds 0 / 0.5 / 0.5b)
- CLOSED. Found Pinterest<->SaaS-affiliate intent mismatch; confirmed real
  Pinterest demand but for cheap-product/young audience; mapped business terms +
  Impact programs. Output drove the pivot to a products-first approach.

### Niche + program research / Round 1 content-gap sweep
- CLOSED. Ranked winnable long-tail angles; anchor = profession-segmented
  digital templates (sell own + Envato). Full shortlist in REFERENCE.md (ROUND 1).

### Etsy "Own Your Business" brand thesis
- CLOSED / PARKED. Reframed to a media brand helping makers escape platform fees
  + own their store. 3 adversarial stress-tests LARGELY INVALIDATED it: affiliate
  pillar dead (Pirate Ship/Stripe = no program; Shopify/Squarespace one-time +
  gated), niche saturated (Gold City Ventures, Paper+Spark, Starla Moore),
  sellers don't migrate (complain + stay; cold stores fail 80-90%), Pinterest =
  beginners not operators. Survivors (A: Pinterest product biz / B: operator
  course / C: reconsider vehicle) documented in REFERENCE.md (STRESS TEST). Nick
  pivoted to photographers instead of pursuing A/B/C here.


### Direction + full research + plan (2026-06-30 -> 07-02)
- CLOSED. Validated Etsy + photographers (both killed) -> found the meta-constraint
  (Pinterest brings beginners/browsers, not operators) -> Nick's unfair advantage
  surfaced: he runs an EVENT COMPANY (Flow State) in the rave scene. Committed to
  FLOW STATE ONLINE (rave/festival affiliate+ads media brand, same name). Ran full
  research: scene landscape, demand/sub-tribes, monetization + event flywheel,
  sustainability, affiliate enumeration (money-first foundation), Pinterest
  best-practices, and the keyword->content->affiliate map. All consolidated into
  FLOW-STATE-MASTER-PLAN.md (+ REFERENCE / KEYWORD-MAP / PINTEREST-PLAYBOOK).
  Handed to the BUILD loop. (Superseded the earlier duplicate COMMITTED-DIRECTION +
  STRATEGIC-PIVOT + photographer loops.)

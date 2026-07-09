# BLOG-SPEC.md — Flow State /blog Content System
# ─────────────────────────────────────────────────────────────────────────────
# STATUS: live spec. PULL WHEN: scaffolding /blog, authoring posts, building skills.
# Blog lives natively in the existing Next.js app at flowstateslc.live/blog
# (true subdirectory = best SEO). Posts = MDX in the repo. Vercel auto-deploys on push.
# ─────────────────────────────────────────────────────────────────────────────

## PRINCIPLES
1. CONTENT-AS-CODE — a post is an MDX file in the repo. AI writes it, commit, ship.
2. AI DOES THE PLUMBING, NICK ADDS THE SOUL — AI drafts structure/research/SEO/
   affiliate wiring; real first-hand experience + real event photos are injected via
   the EXPERIENCE SKILLS (Part B). This is the HCU/anti-slop moat, systematized.
3. COMPLIANT + SEO BY CONSTRUCTION — FTC disclosure, meta, and schema auto-generate
   from frontmatter + components. No post can ship non-compliant.
4. ONE SOURCE OF TRUTH for products — links/commissions/disclosures live in one file.

## PART A — TECHNICAL SPEC

### Stack
- Next.js App Router (existing app) + MDX. Content layer: **Velite** (type-safe
  frontmatter + MDX; App-Router-friendly). Alt: next-mdx-remote + gray-matter + zod.
- Styling: reuse the app's existing system (Tailwind or whatever's there) — blog
  should look like Flow State, not a theme.
- Affiliate cloaking/tracking: native `/go/[id]` redirect route (the Pretty Links equiv).
- Deploy: Vercel, automatic on git push. No second host.

### Folder structure
/app/blog/
  page.tsx            # index: post list, filter by category, newest first
  [slug]/page.tsx     # post renderer (MDX -> components), generates SEO + JSON-LD
  layout.tsx          # blog layout (shared header/footer, email optin in footer)
/app/go/[id]/route.ts # 302 -> product.affiliateUrl (tracked, swappable, rel=sponsored)
/content/blog/        # THE POSTS (one .mdx per post)
/content/products/products.ts   # affiliate product records (single source of truth)
/content/magnets/     # lead-magnet source (packing checklist, kandi pattern pack)
/components/blog/      # the MDX component kit (below)
/lib/blog/{mdx,seo,products}.ts # loaders + SEO/schema helpers

### Frontmatter schema (per post, zod-validated)
title, slug, description(150-160), publishedAt, updatedAt, author,
category (gear|outfits|makeup|kandi|harm-reduction|culture),
tags[], hero{src,alt,credit}, products[] (ids into products.ts),
pinterestKeywords[], funnelRole (reach|money-audition|hub|email-engine|differentiator),
affiliateDisclosure(bool -> auto-inserts <FTCDisclosure/>),
experienceBlocks[] (refs to the Experience-skill outputs woven in),
status (draft|published).

### Product data model (/content/products/products.ts) — one record per product
{ id, name, brand, category, affiliateUrl, network, commission, cookieDays,
  priceApprox, disclosure:true, aligned:true }
- Posts reference products BY ID only. Change a link once here -> every post updates.
- Links render through /go/[id] so URLs are swappable + trackable + rel="sponsored".

### Component kit (/components/blog) — what AI composes posts from
- <FTCDisclosure/>     auto above-the-fold when affiliateDisclosure:true. Plain-language.
- <ProductCard id/>    pulls product data -> image/price/tracked CTA. Consistent + compliant.
- <ComparisonTable ids={[]}/>  the "X vs Y" money format.
- <PackingChecklist items={[]}/>  survival-kit format; doubles as the email-magnet source.
- <EmailOptin magnet/> capture form; on every post.
- <Experience where= when=> ...  **the anti-slop block** — a designed callout that
  showcases Nick's first-hand detail ("Field note, EDC 2025: ..."). E-E-A-T signal.
- <ProTip/> <FieldNote/>  smaller real-experience inserts.
- <PinSave/> (optional) Pinterest save button.

### SEO / schema (auto from frontmatter)
meta title/desc, OpenGraph, canonical; JSON-LD: Article always; Review/Product for
money-audition posts; ItemList for roundups. Hero uses real event photo (credit field).

### Post lifecycle (the "AI does it all" pipeline)
1. Pick post from CONTENT-PLAN.md.
2. AI drafts skeleton: structure + research + SEO frontmatter + product wiring.
3. Run the EXPERIENCE SKILLS (Part B) -> Nick answers targeted Qs (5-10 min).
4. AI weaves answers into <Experience>/<ProTip>/prose in Nick's voice.
5. Add real photos (Photo-Inventory skill). Review -> commit -> Vercel deploys.
6. Generate fresh pins for reach posts.

## PART B — THE EXPERIENCE SKILLS (the anti-slop engine)
Reusable EXERCISES that extract Nick's real experience so every post beats HCU.
Each skill: takes a post topic -> asks targeted questions only Nick can answer ->
outputs structured experience blocks AI drops into the post. Answering >> writing.
(Build these as real skill files later; for now they run as question sets.)

1. **FIELD-TEST** (gear/money posts) — "When/where did you actually use [product]?
   What specifically happened? What surprised you (good/bad)? What's the ONE thing a
   spec sheet won't tell them? What would you tell a friend?" -> <Experience> blocks.
2. **HOT-TAKE** (comparisons/rankings) — "Rank these. Why does your #1 win in the real
   world? What does everyone get wrong?" -> the opinionated POV AI can't fake.
3. **STORY** (culture/differentiator) — "Tell me about a specific night/festival/moment
   that shows [topic]." -> a real anecdote hook.
4. **INSIDER-DETAIL** (prep/harm-reduction) — "What do experienced ravers do that
   beginners don't? What mistake did you make and learn from?" -> practical authority.
5. **PHOTO-INVENTORY** — "Which real Flow State event photos match this post? What does
   each show?" -> real hero + inline imagery (HCU signal + Pinterest fuel).
6. **VOICE** — captures Nick's actual phrasing/slang so drafts sound like him, not a
   generic blog. Ties to Flow State voice rules (REFERENCE.md / flow_state vault).

### Skill workflow per post
Match skills to funnelRole:
- money-audition -> FIELD-TEST + HOT-TAKE + PHOTO-INVENTORY
- hub -> INSIDER-DETAIL + PHOTO-INVENTORY
- differentiator (harm-reduction) -> INSIDER-DETAIL + STORY
- reach (outfits/makeup) -> HOT-TAKE (light) + PHOTO-INVENTORY
- email-engine (kandi) -> STORY (light) + PHOTO-INVENTORY
Always run VOICE. Output = experienceBlocks[] woven into the MDX.

## BUILD ORDER
1. Scaffold: /blog route + MDX (Velite) + one sample post rendering end-to-end.
2. products.ts + /go/[id] redirect + <ProductCard>/<FTCDisclosure>.
3. Remaining components (<ComparisonTable>,<PackingChecklist>,<EmailOptin>,<Experience>).
4. SEO/schema helper. 5. Email-optin wired to the ESP.
6. THEN author post #1 (earplugs review) through the full skill pipeline.
(Scaffold = a focused dev task for Claude Code w/ repo access. Spec above is the brief.)

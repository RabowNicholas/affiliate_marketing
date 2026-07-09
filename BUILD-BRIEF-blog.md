# BUILD BRIEF — Flow State /blog system
# SELF-CONTAINED. Paste this into a fresh Claude Code session running INSIDE the
# flowstateslc.live Next.js repo. It assumes NO access to any other conversation,
# vault, or file. Everything needed is here. Ask the human only if a repo fact is
# genuinely ambiguous after inspecting the code.

## 0. CONTEXT (why this exists — enough to make good calls)
Flow State is a rave/festival brand: a real SLC underground EVENT company + a new
national CONTENT arm. This task builds the content arm's blog INSIDE the existing
Next.js app on Vercel, at the /blog subdirectory (true subdirectory = best SEO; do
NOT make it a separate subdomain or app).
Business model context: the blog's job is (a) SEO discovery, (b) capturing readers
into an EMAIL list, and (c) honest gear/prep reviews with AFFILIATE links that serve
as proof-of-influence for brand deals. Display ads are NOT a priority — do not build
ad infrastructure. Affiliate links + email capture + fast SEO pages are the point.
Editorial guardrail: posts pair AI-drafted structure with the founder's REAL first-
hand experience + real event photos (an <Experience> component showcases these).
Build the component; the human fills the content.

## 1. OBJECTIVE
Add a production-ready blog to the existing app at flowstateslc.live/blog, where each
post is an MDX file in the repo, and shipping = git push (Vercel auto-deploys).

## 2. SCOPE
IN scope:
- /blog index + /blog/[slug] post pages (App Router; match the repo's router).
- MDX pipeline with type-safe, validated frontmatter.
- The component kit (section 6) usable inside MDX.
- Single-source-of-truth product data + a /go/[id] affiliate redirect route.
- Auto SEO meta + JSON-LD schema from frontmatter.
- One fully-working sample post (section 7) rendering end-to-end.
- Email-optin component as a STUB (props + UI; wire to an ESP later via env var).
OUT of scope (do NOT build): display-ad code, comments, auth, a CMS admin UI, search,
pagination beyond a simple list, the "experience skills" (a separate content process).

## 3. PRE-FLIGHT — inspect the repo FIRST, then match it
Before writing code, determine and conform to: App vs Pages router; styling system
(Tailwind? CSS modules? tokens?); existing component patterns + file conventions;
TypeScript config; image handling (next/image); how the existing site defines fonts/
colors. The blog must look and read like the existing Flow State site (dark/underground
aesthetic) — reuse existing design tokens/components, do not introduce a new theme.
Pick the MDX approach that best fits the repo: prefer **Velite** (type-safe content
layer) or **next-mdx-remote + gray-matter + zod**. Justify the choice in a comment.

## 4. FOLDER STRUCTURE (adapt to repo conventions)
/app/blog/page.tsx            index: list posts, filter by category, newest first
/app/blog/[slug]/page.tsx     post renderer -> MDX + components + SEO/JSON-LD
/app/go/[id]/route.ts         302 -> product.affiliateUrl; adds rel handling + tracking
/content/blog/*.mdx           the posts
/content/products/products.ts affiliate products (single source of truth)
/components/blog/*             the component kit
/lib/blog/*                    mdx loader, seo helper, product lookup

## 5. FRONTMATTER SCHEMA (zod-validate; reject on missing required)
title:string  slug:string  description:string(<=160)  publishedAt:date
updatedAt:date  author:string  category:enum[gear,outfits,makeup,kandi,harm-reduction,culture]
tags:string[]  hero:{src,alt,credit}  products:string[](ids)  pinterestKeywords:string[]
funnelRole:enum[reach,money-audition,hub,email-engine,differentiator]
affiliateDisclosure:boolean  status:enum[draft,published]
Behavior: status:draft excluded from index + sitemap (viewable by direct URL in dev).
affiliateDisclosure:true auto-renders <FTCDisclosure/> above the fold.

## 6. COMPONENT KIT (/components/blog)
- <FTCDisclosure/>            plain-language, before-the-links, auto-inserted.
- <ProductCard id="">        looks up products.ts -> image/name/price/CTA via /go/[id].
- <ComparisonTable ids={[]}/> table of products (the "X vs Y" format).
- <PackingChecklist items={[]}/> checklist layout (also feeds the email magnet later).
- <EmailOptin magnet="">     STUB: capture UI + prop; POST to a TODO endpoint/env var.
- <Experience where="" when=""> designed callout showcasing founder first-hand notes.
- <ProTip/> <FieldNote/>      smaller callouts.
All components must be usable directly in MDX and styled with the repo's system.

## 7. SAMPLE POST — build this so it renders end-to-end (/content/blog/best-earplugs-for-raves.mdx)
Frontmatter: title "Best Earplugs for Raves (2026): Loop vs Eargasm vs Alpine",
slug "best-earplugs-for-raves", category "gear", funnelRole "money-audition",
affiliateDisclosure true, products ["loop-experience","eargasm-hifi","alpine-partyplug"],
pinterestKeywords ["rave earplugs","concert earplugs","festival hearing protection"],
hero {src:"/blog-images/earplugs-hero.jpg",alt:"...",credit:"Flow State event"}.
Body must exercise EVERY component: intro prose, <FTCDisclosure/>, a <ComparisonTable/>
of the 3 products, a <ProductCard/> per product, at least one <Experience/> and one
<ProTip/> (use realistic placeholder copy tagged {/* EXPERIENCE PLACEHOLDER */}),
and an <EmailOptin magnet="festival-packing-checklist"/>. Real prose can be lorem-ish
placeholder — the point is the SYSTEM renders, is compliant, and is SEO-complete.

## 8. PRODUCT SEED (/content/products/products.ts) — real records
Fields per record: id,name,brand,category,affiliateUrl(placeholder ok),network,
commission,cookieDays,priceApprox,disclosure:true,aligned:true.
Seed at least:
- loop-experience | Loop | earplugs | Impact | 15% | 30d | ~34.95
- eargasm-hifi | Eargasm | earplugs | in-house | 15% | -- | ~39
- alpine-partyplug | Alpine | earplugs | Awin | 12.5% | -- | ~25
- cure-hydration | Cure Hydration | hydration | Impact | 20-25% | -- | ~40
- today-glitter | Today Glitter | beauty | ShareASale | 15% | -- | ~12
- rave-doctor | Rave Doctor | recovery | in-house | 20% | -- | ~30
- testkitplus | TestKitPlus | harm-reduction | in-house | 25% | -- | ~40
(affiliateUrl = "#TODO-<id>" placeholders; human swaps real links in later, in ONE place.)

## 9. SEO / SCHEMA
Per post: <title>, meta description, canonical, OpenGraph/Twitter from frontmatter.
JSON-LD: Article always; add Review/Product for funnelRole "money-audition"; ItemList
for roundups. Generate an XML sitemap that excludes drafts. Use next/image for hero.

## 10. ACCEPTANCE CRITERIA (definition of done)
[ ] /blog lists published posts; drafts excluded.
[ ] /blog/best-earplugs-for-raves renders all components, styled like the site.
[ ] Invalid frontmatter fails the build with a clear error (zod).
[ ] /go/loop-experience 302-redirects to the product URL with rel="sponsored".
[ ] Every affiliate link routes through /go/[id]; disclosure shows above the fold.
[ ] Page has correct <title>, meta desc, canonical, and valid Article JSON-LD.
[ ] Lighthouse: static-generated, fast; no console errors; keyboard-accessible.
[ ] A new .mdx file in /content/blog with valid frontmatter appears with NO code changes.
[ ] Builds clean on Vercel preview.

## 11. MILESTONES (commit at each)
1. MDX pipeline + frontmatter validation + /blog/[slug] renders raw MDX.
2. products.ts + /go/[id] + <ProductCard> + <FTCDisclosure>.
3. Remaining components. 4. SEO/schema + sitemap. 5. Sample post passes all criteria.

## 12. HAND BACK
A short note: MDX approach chosen (+ why), how to add a post (the 3 steps), where to
put real affiliate URLs + hero images, and the TODO to wire <EmailOptin> to the ESP.

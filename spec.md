# Live Now Recovery — Content Expansion Build

## Current State
- 5 blog posts in `src/frontend/src/constants/blogPosts.ts` (SEED_BLOG_POSTS)
- Pages: Home, Mission, About, Contact, Register, Helper, Admin, Dashboard, Founder, Blog, BlogPost, Location, Verify, Provider
- Location/town SEO pages: Cleveland, Lakewood, Parma, Lorain, Akron (direct routes)
- No Resources, FAQ, How It Works, or Ohio Stats pages
- Founder page has story + mission + personal message (no timeline)

## Requested Changes (Diff)

### Add
- 10 new blog posts added to SEED_BLOG_POSTS array (total 15)
  1. Buprenorphine vs. Methadone: What the Science Says
  2. Naloxone Access in Ohio: A ZIP Code Guide
  3. The Stigma Is Killing People: A Data-Driven Argument for MAT
  4. Fentanyl and the Third Wave: Ohio's Overdose Crisis Explained
  5. What Is a Warm Handoff and Why Does It Save Lives?
  6. Recovery Housing in Northeast Ohio: What to Know
  7. SAMHSA Guidelines on MAT: What They Mean for You
  8. How Anonymous Technology Protects People Seeking Help
  9. The Economics of Addiction: Why Cost Transparency Matters
  10. Peer Support Specialists: The Bridge Between Crisis and Care
- 4 new informational pages:
  - `/resources` — hotlines, naloxone access, treatment types explainer, Ohio MHAR links
  - `/faq` — 15 Q&A about MAT, privacy, how the app works, Cost Plus
  - `/how-it-works` — visual step-by-step walkthrough of the PoP handoff flow + app usage
  - `/ohio-stats` — Ohio overdose data, regional MAT access gaps, impact projections
- 10 more direct Ohio town SEO routes added to App.tsx:
  Youngstown, Akron (already exists? — check), Canton, Elyria, Mentor, Strongsville, Euclid, Sandusky, Warren, Toledo
  (skip Akron if already present, add Medina instead)
- Enriched Founder page: add a visual recovery timeline section (from first treatment at Brightside → 10 years in program → building Live Now)
- Routes in App.tsx for: /resources, /faq, /how-it-works, /ohio-stats
- Nav or footer links to new pages

### Modify
- `src/frontend/src/constants/blogPosts.ts` — append 10 new posts to SEED_BLOG_POSTS
- `src/frontend/src/App.tsx` — add routes for 4 new pages + 10 new town direct routes
- `src/frontend/src/pages/FounderPage.tsx` — add recovery timeline section
- `src/frontend/src/components/Footer.tsx` — add links to new informational pages
- `src/frontend/public/sitemap.xml` — add new town URLs

### Remove
- Nothing removed

## Implementation Plan
1. Add 10 new blog posts to blogPosts.ts with full content (scientific/medical tone, peer-driven voice)
2. Create ResourcesPage.tsx — hotlines, naloxone access, treatment type cards
3. Create FAQPage.tsx — accordion-style 15 Q&A
4. Create HowItWorksPage.tsx — step-by-step visual flow with PoP handoff walkthrough
5. Create OhioStatsPage.tsx — data page with stats cards, charts-style layout
6. Update FounderPage.tsx to add a recovery timeline (milestones: first treatment, years in program, building the app)
7. Update App.tsx with new routes
8. Update Footer.tsx with links to new pages
9. Update sitemap.xml with new town and page URLs

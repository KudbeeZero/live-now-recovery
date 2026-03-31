# Live Now Recovery

## Current State

Fully functional ICP app with:
- Provider directory with demo seed data and Cost Plus pricing cards (some labeled with "Mark Cuban" branding)
- RBAC with role-based dashboards (User, Helper, Clinic, Admin)
- Admin dashboard with SMS settings, registry, audit log
- Impact Shadow map visualization with seafoam glow
- Sentinel chat widget, SEO location pages
- Components: CubanBridgeCard.tsx, MarkCubanCard.tsx both display Cost Plus drug prices
- No Founders page, no blog system

## Requested Changes (Diff)

### Add
- `/founder` page: Dom's story (10 years in MAT program, started at Brightside with one location, 46 years old), his mission, and a personal message of encouragement. Signed "— Dom, Founder". Warm amber tone.
- Blog system backend: BlogPost type (id, title, slug, content, excerpt, publishedAt, isPublished, author). CRUD functions gated to admin.
- `/blog` page: Public index of published posts, card grid layout, SEO meta per post.
- `/blog/:slug` individual post page: Full content, author, date, back navigation.
- Admin Blog Management tab in `/admin`: Create, edit, publish/unpublish posts via a form UI.
- 5 pre-seeded blog posts (scientific/medical, MAT-focused).
- Footer: Add subtle "Drug pricing transparency powered by Cost Plus Drugs" line.
- Full responsive layout (portrait + landscape) across all pages, touch-optimized.

### Modify
- `CubanBridgeCard.tsx` and `MarkCubanCard.tsx`: Remove all "Mark Cuban" name references. Keep Cost Plus pricing data (Naloxone $61.36, Naltrexone $22.94). Rename component references if needed.
- `Footer.tsx`: Add Cost Plus attribution line.
- `App.tsx`: Add routes for `/founder`, `/blog`, `/blog/:slug`.
- `Header.tsx`: Add "Our Story" link to `/founder` and "Blog" link to `/blog` in nav.

### Remove
- "Mark Cuban" name from all visible UI text in provider cards and pricing components.

## Implementation Plan

1. Add BlogPost type + stable storage + CRUD functions to `main.mo`.
2. Update `backend.d.ts` with blog types and function signatures.
3. Create `FounderPage.tsx` with story, mission, personal message, amber styling.
4. Create `BlogPage.tsx` (index) and `BlogPostPage.tsx` (individual post).
5. Update `AdminPage.tsx` to add Blog Management tab.
6. Seed 5 blog posts in frontend constants (or via backend on first load).
7. Strip "Mark Cuban" from `CubanBridgeCard.tsx` and `MarkCubanCard.tsx`.
8. Update `Footer.tsx` with Cost Plus attribution.
9. Update `App.tsx` routes and `Header.tsx` nav links.
10. Apply responsive CSS improvements across all pages.

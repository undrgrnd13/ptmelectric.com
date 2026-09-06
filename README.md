# ptmelectric.com

Static site for [PTM Electric, Inc.](https://www.ptmelectric.com) — licensed electrical contractor (**FL EC13004084 · NC U.38360 · SC SC-CLM.119110**) serving residential, commercial, and light-industrial clients in South Florida.

DBA: [Stormpower Generators](https://www.stormpowergenerators.com) — overview on-site at [`generators.html`](generators.html); plans/details on the Stormpower brand site.

## Pages

| File | Purpose |
|------|---------|
| `index.html` | Home + company/about + featured projects + 3-card services (Residential · Commercial · Generators) |
| `residential.html` | Residential services |
| `commercial.html` | Commercial / light industrial + track record |
| `generators.html` | Stormpower Generators division overview + CTA to stormpowergenerators.com |
| `contact.html` | Contact + Bid Request (mailto `bids@ptmelectric.com`) |
| `sitemap.xml` / `robots.txt` | SEO crawl files |
| `images/` | Logos (rasters via PAT push; CDN for project photos in HTML) |

## Contact

- Phone: **561-329-6974**
- General: `paul@ptmelectric.com`
- Bid requests: `bids@ptmelectric.com`
- Address: 16971 W. Hialeah Drive, Loxahatchee, FL 33470

## Redirects (configure on Porkbun / host)

| Old path | New target |
|----------|------------|
| `/home` | `/` |
| `/contact-1` | `/contact.html` |
| `/commerciallightindustrial` | `/commercial.html` |
| `/RESIDENTIAL` | `/residential.html` |

Optional: `/about` -> `/`, `/contact` -> `/contact.html`, `/residential` -> `/residential.html`, `/generators` -> `/generators.html`.

## Deploy

Public GitHub repo for Porkbun Static Hosting + GitHub Connect. Prefer PRs for content changes. **Do not merge** until Paul reviews.

## Phase 1 notes (direction change)

- **Generators page** on ptmelectric.com (not external-only bounce from home card)
- Nav (header + mobile + footer) includes Generators on all pages; sitemap updated
- Home services card → `generators.html`; Stormpower external CTA on that page
- Project captions/alt text audited to match photos (Shoppes Westlake, Pure Life Renal, Phenix Salon Suites, H&R Block, Neptune City Laundromat, Sudsville); Bath & Body Works kept as client logo only
- Home hero (Pure Life) diversifies from commercial hero (Shoppes)

## Image assets note

GitHub MCP `push_files` corrupts binary blobs. HTML uses Squarespace CDN URLs for real project photos so preview works. Follow-up: PAT `git push` of local `images/*.{jpg,png,webp}` then switch `src` to relative paths before Squarespace cancel.

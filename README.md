# ptmelectric.com

Static site for [PTM Electric, Inc.](https://www.ptmelectric.com) — licensed electrical contractor (**FL EC13004084 · NC U.38360 · SC SC-CLM.119110**) serving residential, commercial, and light-industrial clients in South Florida.

DBA: [Stormpower Generators](https://www.stormpowergenerators.com) (separate brand site for standby generators — featured as its own home services card).

## Pages

| File | Purpose |
|------|---------|
| `index.html` | Home + company/about + featured projects + 3-card services (Residential · Commercial · Generators/Stormpower) |
| `residential.html` | Residential services |
| `commercial.html` | Commercial / light industrial + track record |
| `contact.html` | Contact + Bid Request (mailto `bids@ptmelectric.com`) |
| `sitemap.xml` / `robots.txt` | SEO crawl files |
| `images/` | Logos, project photos, heroes |

## Contact

- Phone: **561-329-6974**
- General: `paul@ptmelectric.com`
- Bid requests: `bids@ptmelectric.com`
- Address: 16971 W. Hialeah Drive, Loxahatchee, FL 33470

## Redirects (configure on Porkbun / host)

Document these when cutting over from Squarespace:

| Old path | New target |
|----------|------------|
| `/home` | `/` |
| `/contact-1` | `/contact.html` |
| `/commerciallightindustrial` | `/commercial.html` |
| `/RESIDENTIAL` | `/residential.html` |

Optional: `/about` -> `/` (about content is folded into the home page), `/contact` -> `/contact.html`, `/residential` -> `/residential.html`.

## Deploy

Public GitHub repo for Porkbun Static Hosting + GitHub Connect (same playbook as `stormpowergenerators.com`). Prefer PRs for content changes. **Do not merge** until Paul reviews.

## Phase 1 / Option A notes

- Licenses everywhere: `FL EC13004084 · NC U.38360 · SC SC-CLM.119110` (no “SC soon”)
- Home services: three equal cards — Residential · Commercial / Light Industrial · Generators (Stormpower) with amber accent + CTA to stormpowergenerators.com
- Bid wording: `Bid requests: bids@ptmelectric.com`
- Heroes/featured: real job photos (Shoppes Westlake, Pure Life Renal, salon, laundry, suite, Bath & Body Works) — Pexels/stock lightbulb fillers removed
- Bid Request form uses mailto; HTML comment documents Formspree for later

## Image assets note

Optimized rasters from the Squarespace crawl live locally under `images/` on the build machine. GitHub MCP `push_files` UTF-8-encodes content and corrupts binary blobs, so this PR:

- Ships `images/logo.svg` (text logo) for chrome
- Uses Squarespace CDN URLs for **real project photos** (not stock) so Paul can preview immediately
- Follow-up: `git push` with a PAT should add local `images/*.{png,jpg,webp}` and switch `src` to relative paths before Squarespace cancel

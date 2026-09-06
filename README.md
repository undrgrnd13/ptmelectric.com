# ptmelectric.com

Static site for [PTM Electric, Inc.](https://www.ptmelectric.com) — licensed electrical contractor (FL **EC13004084**, NC **U.38360**) serving residential, commercial, and light-industrial clients in South Florida.

DBA: [Stormpower Generators](https://www.stormpowergenerators.com) (separate brand site).

## Pages

| File | Purpose |
|------|---------|
| `index.html` | Home + company/about + featured projects + license/DBA |
| `residential.html` | Residential services |
| `commercial.html` | Commercial / light industrial + track record |
| `contact.html` | Contact + Bid Request (mailto `bids@ptmelectric.com`) |
| `sitemap.xml` / `robots.txt` | SEO crawl files |
| `images/` | Logos, project photos, heroes |

## Contact

- Phone: **561-329-6974**
- General: `paul@ptmelectric.com`
- Bids: `bids@ptmelectric.com`
- Address: 16971 W. Hialeah Drive, Loxahatchee, FL 33470

## Redirects (configure on Porkbun / host)

Document these when cutting over from Squarespace:

| Old path | New target |
|----------|------------|
| `/home` | `/` |
| `/contact-1` | `/contact.html` |
| `/commerciallightindustrial` | `/commercial.html` |
| `/RESIDENTIAL` | `/residential.html` |

Optional: `/about` → `/` (about content is folded into the home page), `/contact` → `/contact.html`, `/residential` → `/residential.html`.

## Deploy

Public GitHub repo for Porkbun Static Hosting + GitHub Connect (same playbook as `stormpowergenerators.com`). Prefer PRs for content changes.

## Phase 1 notes

- Fixed typo: "bid requests" (was "bid rerquests")
- Footer: **Residential** (not REISDENTIAL); no broken `/RESIDENTIAL` link
- No ZipRecruiter widget
- Real meta descriptions on all pages
- Bid Request form uses mailto; HTML comment documents Formspree for later

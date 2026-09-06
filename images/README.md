# Images

- `logo.svg` — text logo mark for header (MCP-safe).
- Optimized real job rasters are ready locally under this folder (`shoppes-westlake.jpg`, `pure-life-renal.jpg`, `project-salon.jpg`, `bath-body-works.jpg`, `hr-block.jpg`, `suite.jpg`, etc.).
- GitHub MCP `push_files` corrupts binary blobs (UTF-8 encode path), so HTML currently references **Squarespace CDN URLs for real project photos** (Shoppes Westlake, Pure Life Renal, salon, laundry, suite, Bath & Body Works) — **not** Pexels/stock lightbulb fillers.
- Local relative paths after a PAT `git push` of rasters:
  - `images/shoppes-westlake.jpg`
  - `images/pure-life-renal.jpg`
  - `images/project-salon.jpg`
  - `images/bath-body-works.jpg`
  - `images/hr-block.jpg`
  - `images/suite.jpg`
- After PAT push, switch `src` attributes to those relative paths and cancel Squarespace CDN dependency.

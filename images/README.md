# Images

- `logo.svg` - text logo mark for header (MCP-safe).
- Optimized raster copies from the Squarespace crawl are prepared locally as `*.png` / `*.jpg` / `*.webp`.
- GitHub MCP `push_files` corrupts binary blobs (UTF-8 path), so Phase 1 HTML references Squarespace CDN URLs for photos/logos until binaries are pushed with a git/PAT client.
- After PAT push of rasters, switch `src` back to relative `images/*` paths.

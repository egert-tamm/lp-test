# star.io — Landing Page

Full-screen video landing page for **star** — the B2B gaming & payments platform.

## Stack

- Pure HTML + CSS (single `index.html`, no build step)
- Background video served from Cloudflare R2 via `cdn.star.io`

## Deploy

### Cloudflare Pages

1. Connect the repo to [Cloudflare Pages](https://pages.cloudflare.com/)
2. Build command: _(none)_
3. Output directory: `/`
4. Set custom domain: `star.io`

### Video (R2)

The background video is hosted on Cloudflare R2:

1. Upload `part-1_10_compressed_26-03-28.mp4` to R2 bucket
2. Serve via custom domain `cdn.star.io` with path `/videos/`
3. Cache headers are set in `_headers` (immutable, 1 year)

## Files

| File | Purpose |
|------|---------|
| `index.html` | Landing page (self-contained) |
| `_headers` | Cloudflare Pages response headers |
| `README.md` | This file |

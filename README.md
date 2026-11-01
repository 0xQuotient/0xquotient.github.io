# Derrick J. Last Jr

Personal site: what I built, what I write, my setup, and how I work.

**Live:** https://0xquotient.github.io

Written with Claude AI. Design direction and content are mine.

## About the build

A single static `index.html` with the CSS and JavaScript inline. No build step, no dependencies, no tracking. Hosted on GitHub Pages. Fonts (Chakra Petch, Geist, Geist Mono) are self-hosted in `fonts/` under the SIL OFL.

## Security

The page loads nothing from other sites and stores nothing in the browser (no cookies, localStorage, or service workers). A Content-Security-Policy meta tag blocks all network requests except the site's own files and allows only the one inline script, pinned by hash. If you edit the inline script, update the `sha256` in the CSP meta tag. Outbound links use `noopener noreferrer`, and the page blanks itself if loaded inside a frame.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site |
| `derrick.webp`, `derrick.jpg` | Hero photo (WebP with JPEG fallback) |
| `avatar.jpg` | Nav avatar |
| `favicon.svg`, `favicon.png`, `apple-touch-icon.png` | Icons |
| `og.png` | Link preview image |
| `fonts/` | Self-hosted woff2 fonts and their licenses |
| `.nojekyll` | Serve files as-is |

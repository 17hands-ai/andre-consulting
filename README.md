# andrecoach.com: redesign prototype

A single-page redesign proposal in a light lavender style for Andre Business Consulting, based on the SEO & GEO audit (Oct 15, 2026). It's a static site with no build step.

## Deploy on Vercel

1. In Vercel, choose **Add New → Project** and import `17hands-ai/andre-consulting`.
2. Leave **Framework Preset** as **Other**. There is no build command, and the output directory is the repo root.
3. Deploy. Every push to a branch gets a preview URL; pushes to the default branch update production.

Or from the command line: `npx vercel` (preview) or `npx vercel --prod`.

## Files

- `index.html`: the whole page (HTML, CSS and JS inline; fonts from Google Fonts)
- `favicon.svg`: the tab icon
- `vercel.json`: clean URLs and response headers
- `robots.txt`: blocks search engines

## Before it goes live as the real site

This is a proposal, so it's hidden from search engines. When it becomes the real andrecoach.com:

- remove `<meta name="robots" content="noindex, nofollow">` from `index.html`
- remove the `X-Robots-Tag` header from `vercel.json`
- replace `robots.txt` with `User-agent: *` / `Allow: /` plus a sitemap line
- remove the **Show audit notes** button and the `.note` elements
- fill in every placeholder (text with a dotted underline): full name, photo, prices, case-study figures, phone, LinkedIn and testimonials

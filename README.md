# No Competition supercharged bistro, Corrales

One-page static site for No Competition. A single `index.html` with embedded fonts and a folder of images. No build step.

## Deploy on Cloudflare Pages
- Framework preset: None
- Build command: leave blank
- Build output directory: `/` (or `.` if the field rejects `/`)
- Production branch: `main`
- Custom domains: add both `eatnocompetition.com` and `www.eatnocompetition.com` to the Pages project

## Edit
- Hours: the table in `index.html`, the `openingHoursSpecification` block in the JSON-LD near the top, and nothing else (the "today" highlight reads the table rows)
- Colors: the variables at the top of the `<style>` block
- Font sizes: the `font-size` values in the `<style>` block (headings use `clamp()` so they scale with the screen)
- Order link: `https://primeraagua.com/order/no-competition-4445-corrales-road` (appears in many places; find and replace it in `index.html`)
- Social links: Facebook and Instagram appear in the header, the mobile menu, the footer, and the JSON-LD `sameAs` list
- Reviews: add more `<figure class="card">` blocks inside `.cards`; they scroll sideways automatically and alternate orange and white

## Tracking
- Meta Pixel (ID 2290437844798849) is in the `<head>` of `index.html`, just before `</head>`.

## Fonts
- Headings, nav, buttons and the phone number use Architype Bayer. It is a lowercase-only face, so everything set in it is lowercased on purpose.
- Body text uses Public Sans (SIL Open Font License, copy in `fonts/PUBLIC-SANS-OFL.txt`).
- Both fonts are embedded in the CSS as data URIs, so they load even when the page is opened straight from disk and the page makes no calls to Google Fonts. The original font files stay in `fonts/` for reference; the page does not load them.
- `fonts/public-sans-latin-wght-italic.woff2` is no longer used and can be deleted.

## Files
- `images/hero-desktop.jpg`, `images/hero-mobile.jpg`: hero photo (desktop and portrait crop)
- `images/og-image.jpg`: link preview image (1200x630)
- `images/favicon.png`, `images/apple-touch-icon.png`: icons
- `robots.txt`, `sitemap.xml`: crawler files (update `lastmod` when the page changes)

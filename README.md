# Shepherd Group — shepherdgroupre.com

Static marketing site for Shepherd Group, a residential development firm in
Greater Nashville and Brentwood, Tennessee.

No build step. No dependencies. `index.html` is the whole site — open it in a
browser and it works.

## Structure

```
index.html        Entire site: five pages, hash-routed (#/, #/about, …)
assets/           Logo files (wordmark, diamond, monogram — ocean + white)
fonts/            Athelas, subset to Latin and converted to WOFF2
photos/           Project photography and architectural renderings
```

Pages are sections in `index.html` that show and hide via the hash router at the
bottom of the file. Adding a page means adding a `<section id="page-NAME">`,
adding `NAME` to the `ROUTES` array, and adding a nav link.

## Brand

From the Shepherd Group One Page Branding Guidelines:

| Token | Hex | Use |
| --- | --- | --- |
| Ocean | `#0080A6` | Primary accent, links, buttons |
| Charcoal | `#52555B` | Dark surfaces, secondary text |
| Slate | `#9B958D` | Warm neutral |
| Sky | `#BBD3DB` | Light tint, on-dark eyebrows |

Typefaces are Athelas (headings, titles, figures) and Jost (everything else).
Colors are CSS custom properties on `:root`, redefined for dark mode. Change a
token once and it propagates.

## Deploying

Any static host works. Point it at the repository root; there is nothing to
build.

Cloudflare Pages or Netlify both deploy on push and handle the TLS certificate.
The domain is registered at GoDaddy, so connecting it means pointing DNS at the
host rather than using GoDaddy's own hosting.

## Before this goes public

- **Athelas is licensed, not free.** The files in `fonts/` are subset from the
  macOS system build. A desktop license does not cover serving a font on the
  web — that is a separate webfont license from TypeTogether. Confirm the
  license before the site is public, and keep this repository private until
  that is settled, since pushing the font files to a public repo redistributes
  them.
- **Addresses of projects underway are listed publicly.** Nine in-progress
  projects are named by street address on the Projects page. Confirm each one
  is closed and safe to disclose.
- **The contact form is not wired up.** It validates and shows a message; it
  does not send. Needs a form endpoint before launch.
- **Placeholder slots remain** for photography that has not been supplied —
  headshots, several completed projects, and four renderings. Each is labeled
  on the page with what belongs there.

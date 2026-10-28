# Retirement Curator

A retirement outcome simulator based on VOO and VTI: model a portfolio, contributions, and a retirement window, then compare how the outcomes spread.

**Live:** [retirement.northbrand.net](https://retirement.northbrand.net) (Cloudflare Pages, project `retirement-curator`)

## The page

Everything is in one file, `index.html`: markup, styles, and the simulation script. There is no build step and nothing is sent anywhere; the simulation runs entirely in the visitor's browser.

One hard rule for editors: design passes may touch the CSS variables, the header, and the footer only. The simulation script itself stays byte-identical unless the change is deliberately about the math, made on its own, and called out in the commit.

## Design

Styled to the Northbrand design DNA (warm paper and ink, Northbrand Gold primary, serif display, the footer lockup with an educational disclaimer). The DNA lives in the northbrand-hub repo; `DESIGN.md` beside the local master carries this page's notes.

## Hosting

Published by direct upload to Cloudflare Pages; this repo is the archive of record. An older copy still answers at retirement-curator.vercel.app, untouched; the northbrand.net address is the current one.

Local master: `~/workspace/retirement-curator/index.html`

## Note

For education only. The simulator illustrates possibilities; it is not financial advice.

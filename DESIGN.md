# DESIGN.md: Retirement Curator (Retirement Strategy Center)

The design notes for the Retirement Strategy Center (https://retirement.northbrand.net, GitHub repo bparish0619-cyber/retirement-curator, single-file index.html). The shared shell and brand tokens follow the Northbrand design DNA in ~/workspace/northbrand-hub/DESIGN.md; this file records the site's local tokens.

## 1. Visual Theme & Atmosphere
A calm, trustworthy simulator: warm paper in light theme, Northbrand ink in dark theme, gold carrying the brand and the primary actions. The strategy series colors are data, not decoration.

## 2. Color Palette & Roles
- Paper `#f4f3ec` / Ink `#14161c`: page backgrounds (light / dark), per the DNA.
- Card `#fffdf9` / `#1d2029`: panels and stat boxes.
- Gold Deep `#9a7208`: primary in light theme (buttons, links, focus, highlights). Gold Bright `#e8b33c` and Gold `#c9a227`: primary and hover in dark theme.
- Line `#d5d2c2` / `#2c303e`: borders and chart grid.
- Data accents (local, meaning only): green `#059669`, orange `#d97706`, purple `#7c3aed` for the strategy series; dark theme lifts them (`#34d399`, `#fbbf24`, `#a78bfa`).

## 3. Typography Rules
Serif (Georgia) for the page title per the DNA; system sans for body and data. The header carries the "Northbrand Collective" eyebrow in gold, letterspaced small caps.

## 4. Component Stylings
Cards and panels at 12 to 16px radius with hairline borders. The footer is the DNA lockup ("A Northbrand Collective project · northbrand.net", gold link to the hub) over an educational disclaimer line: simulations based on VOO and VTI outcomes, not financial advice.

## 5. Layout Principles
Single column tool layout, controls first, results and report below, footer lockup last. Print view (the report) keeps working; do not restyle it casually.

## 6. Depth & Elevation
Flat with hairlines, per the DNA.

## 7. Do's and Don'ts
Do: keep the simulation logic and the input/output contract untouched in design passes; design changes are CSS variables, header, and footer only. Don't: no blue primary (retired 2026-10-27), no new hues beyond the data accents, no em dashes in copy.

## 8. Responsive Behavior
The page already guards against mobile overflow (global box sizing and overflow-x rules); keep tap targets comfortable and never reintroduce horizontal scroll.

## 9. Agent Prompt Guide
Quick reference: paper `#f4f3ec`, ink `#14161c`, card `#fffdf9`, gold deep `#9a7208`, gold bright `#e8b33c`, line `#d5d2c2`. Prompt seed: "Restyle within the Northbrand design DNA (~/workspace/northbrand-hub/DESIGN.md) using the Retirement Curator local tokens in this file; never touch the simulation script."

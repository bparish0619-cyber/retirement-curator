# DESIGN.md: Retirement Curator (Retirement Strategy Center)

The design notes for the Retirement Strategy Center (https://retirement.northbrand.net, GitHub repo bparish0619-cyber/retirement-curator, single-file index.html). The shared shell and brand tokens follow the Northbrand design DNA in ~/workspace/northbrand-hub/DESIGN.md; this file records the site's local tokens and, since 2026-11-06, its role as a full planning tool.

## 1. Visual Theme & Atmosphere
A calm, trustworthy planning tool: warm paper in light theme, Northbrand ink in dark theme, gold carrying the brand and the primary actions. The strategy series colors are data, not decoration. Tools first, essay second: the simulators are the page now, and the strategy writing supports them.

## 2. Color Palette & Roles
- Paper `#f4f3ec` / Ink `#14161c`: page backgrounds (light / dark), per the DNA.
- Card `#fffdf9` / `#1d2029`: panels and stat boxes.
- Gold Deep `#9a7208`: primary in light theme (buttons, links, focus, highlights). Gold Bright `#e8b33c` and Gold `#c9a227`: primary and hover in dark theme.
- Line `#d5d2c2` / `#2c303e`: borders and chart grid.
- Data accents (local, meaning only): green `#059669`, orange `#d97706`, purple `#7c3aed` for the strategy series; dark theme lifts them (`#34d399`, `#fbbf24`, `#a78bfa`). Red appears only as a negative delta in the what-if table.

## 3. Typography Rules
Serif (Georgia) for the page title and section titles per the DNA; system sans for body and data. The header carries the "Northbrand Collective" eyebrow in gold, letterspaced small caps.

## 4. Component Stylings
Cards and panels at 12 to 16px radius with hairline borders. The footer is the DNA lockup ("A Northbrand Collective project · northbrand.net", gold link to the hub) over an educational disclaimer line: simulations based on VOO and VTI outcomes, not financial advice.

**Dual-control rule (set 2026-11-06 at Brandon's direction):** every slider is paired with a synced editable number input beside it, with unit, min, max, and step. Moving either control updates the other and recalculates. Number entry tolerates typing, validates and clamps on change or blur, and never traps the user mid-keystroke. This rule governs every current and future control on the page; a slider-only control is a defect. Primary controls and tap targets are at least 44px where practical, and the viewport never disables pinch zoom.

## 5. Layout Principles
Six named sections under a slim sticky section nav (Plan, Outlook, Income, Risk Lab, Strategy, Details), set 2026-11-06:
1. **Plan**: all controls in four labeled groups (Household and timing; Saving and investing; Retirement spending and income; Assumptions and risk), plus the contribution routing card (2026 401(k)/IRA limits by age and filing status).
2. **Outlook**: headline results, accumulation chart, balances in nominal and today's dollars, target coverage, goal tools (Financial Independence age, Coast number, required-saving solver), and the return sensitivity strip.
3. **Income**: retirement income and longevity simulator (scenario selector, funded-through and depletion ages, balance by age chart). The year by year cash-flow table lives in Details.
4. **Risk Lab**: Monte Carlo (1,000 paths, percentile band chart) and the five-case what-if lab against the deterministic baseline.
5. **Strategy**: the condensed VOO/VTI guidance. The conclusion leads the section: pick ONE core fund, VOO or VTI; holding both mainly duplicates the same large companies. Overlap, the identical 0.03% expense ratios, and the tax-loss-harvesting partner exception stay; the long essay does not.
6. **Details**: tabbed year by year projection table, retirement cash flow, milestones, and the Assumptions and method notes.

Print view (the report) keeps working and now includes target coverage, the income simulator result, and Monte Carlo success when available. The downloaded offline copy preserves every input, select, tab, and theme state generically, so new controls carry over automatically. Do not restyle the print view casually.

## 6. Depth & Elevation
Flat with hairlines, per the DNA.

## 7. Do's and Don'ts
Do: keep the model constants (scenario rates, 2026 limits, Monte Carlo path count and seed) in the one marked MODEL block at the top of the script, and keep copy free of em dashes and hype. Don't: no blue primary (retired 2026-10-27), no new hues beyond the data accents, never present a simulation as a recommendation or guarantee, and never claim VOO or VTI will earn 12.9% in the future (it is labeled a historical scenario).

**Functional-change note (2026-11-06):** Brandon explicitly authorized functional changes in the 2026-11-06 rebuild: the dual-control redesign, the new planning inputs (contribution increase, spending, Social Security and other guaranteed income, plan-through age, inflation, planning return, volatility, market drop, target portfolio), and the new simulations (inflation-aware outlook, goal solver, income and longevity simulator, Monte Carlo, what-if lab, sensitivity strip). The older design-only note ("design passes touch CSS variables, header, and footer only, never the simulation script") no longer governs this page. Future passes still preserve the calculation conventions documented on the page unless Brandon directs otherwise: monthly contributions deposited before monthly growth, contributions growing yearly by the increase setting, retirement withdrawals at the start of the year before that year's growth, and the market drop applied once before the first retirement year.

## 8. Responsive Behavior
Verified with a real render at 390, 768, and 1440 widths: zero horizontal overflow, all six sections render, the sticky nav stays usable on phones, and charts re-render on resize. Keep tap targets comfortable and never reintroduce horizontal scroll or a zoom-blocking viewport.

## 9. Agent Prompt Guide
Quick reference: paper `#f4f3ec`, ink `#14161c`, card `#fffdf9`, gold deep `#9a7208`, gold bright `#e8b33c`, line `#d5d2c2`. Prompt seed: "Work within the Northbrand design DNA (~/workspace/northbrand-hub/DESIGN.md) using the Retirement Curator local tokens in this file; every slider pairs with an editable number input, the six-section layout and the documented calculation conventions stay, and the strategy conclusion (one core fund, VOO or VTI) stays explicit."

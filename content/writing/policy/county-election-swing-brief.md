---
title: "County-Level Partisan Swing, 2020–2024: What State-Level Context Adds to the National Narrative"
subtitle: "Policy Brief — Independent Analysis"
date: 2026-03-15
type: "Policy Brief"
status: "Independent Analysis · March 2026"
paper: "https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf"
repo: "https://github.com/kmazurek95/us-election-county-swing"
dashboard: "https://us-election-county-swing.streamlit.app/"
related_project: "/projects/election-swing/"
authors: ["Kaleb Mazurek"]
summary: "Three-page brief arguing that campaign and advocacy analysis of the 2024 election misses nearly a third of the swing story by focusing on county demographics without modeling state-level context. Based on a multilevel analysis of 3,152 counties nested in 49 states."
tags: ["Policy", "Quant", "Political Economy"]
weight: 1
---

**Policy Brief · Independent Analysis · March 2026**

[**Download Brief (PDF)**](https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf) · [Interactive Dashboard](https://us-election-county-swing.streamlit.app/) · [Code and Data](https://github.com/kmazurek95/us-election-county-swing)

---

Post-election analysis of the 2024 partisan swing has focused heavily on county-level demographic change: Hispanic shifts, education gradients, rural deepening, college-town stability. These patterns are real. But a multilevel model of 3,152 counties nested in 49 states shows that roughly 31 percent of county-level swing variance sits at the state level, not the county level. The headline implication: campaigns, advocacy organizations, and researchers optimizing at the county level without accounting for state-level context are missing nearly a third of the explanatory story.

## Key findings

- **State-level forces explain 31% of county-level swing variance** (intraclass correlation = 0.305). Counties swung more similarly to other counties in the same state than to demographically comparable counties in other states. State media environments, campaign resource allocation, gubernatorial politics, and state policy context do substantial explanatory work that county-level analysis alone cannot see.

- **Hispanic population share is the single strongest county-level predictor of rightward swing.** A 10-percentage-point increase in Hispanic share predicted 0.46 additional points of Republican swing (*p* < 10⁻⁷¹), driven by South Texas, the Florida I-4 corridor, and Southern California. The finding speaks directly to the most-debated dynamic of the 2024 cycle.

- **Education polarization varies meaningfully across states, but not because of state economic conditions.** The random slope for college share is highly significant (LR test *p* < 10⁻¹⁶), confirming that education's effect on swing differs across states. But the cross-level interaction with state-level unemployment change is null (*p* = 0.48). Whatever drives state-by-state variation in the education gradient, local economic conditions are not it.

## What this means for practice

For campaign and advocacy work, the state-level ICC has a concrete implication: demographic targeting strategies that treat counties as independent units systematically underweight the structural forces that distinguish how the same demographic patterns play out across different state contexts. A Hispanic-majority county in Florida and a Hispanic-majority county in California did not move in parallel. The difference lives at the state level.

For research and policy analysis, the null cross-level interaction on education-by-unemployment is a boundary condition worth reporting honestly. The education gradient's state-level variation is real; its explanation is not state economic change. That narrows the search space for what actually drives the variation — candidate explanations include state media market structure, differential campaign spending, and local party infrastructure — each requiring different data to test.

## Methodology

Multilevel model of 3,152 US counties nested in 49 states. Five data sources merged on FIPS codes: MEDSL county-level returns (2020, 2024), American Community Survey 5-year estimates (demographics), Bureau of Labor Statistics (state unemployment), Census population density, and derived two-party vote share. Random intercept and random slope specifications tested; cross-level interactions estimated for education and economic conditions. Full replication code, model diagnostics, and robustness checks are available in the [GitHub repository](https://github.com/kmazurek95/us-election-county-swing).

## Related work

This brief draws on a broader research project on county-level partisan swing, which includes an interactive dashboard with choropleth maps and a more complete methodological treatment. The [full project page](/projects/election-swing/) has the extended research discussion, dashboard link, and the repository structure.

## Cite as

Mazurek, K. (2026). *County-Level Partisan Swing, 2020–2024: What State-Level Context Adds to the National Narrative*. Policy Brief, March 2026. Available at https://kmazurek95.github.io/writing/policy/county-election-swing-brief/

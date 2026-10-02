---
title: "2020-2024 County-Level Partisan Swing"
type: "Electoral Geography / Multilevel Modeling"
summary: "Multilevel model of the 2020-2024 county-level partisan swing across 3,101 US counties nested in 49 states and DC. 31% of swing variance is between states. Hispanic population share is the strongest predictor of rightward swing."
date: 2026-03-08
weight: 5
repo: "https://github.com/kmazurek95/us-election-county-swing"
dashboard: "https://us-election-county-swing.streamlit.app/"
paper: "https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf"
stats:
  - "3,101 counties"
  - "49 states and DC"
  - "ICC = 0.305"
  - "5 data sources"
tags: ["elections", "multilevel-modeling", "electoral-geography", "US-politics"]
---

## The Question

What county-level demographic and economic conditions predicted the 2020-2024 partisan swing? And does the effect of educational composition depend on local economic context?

## Findings

### 1. ICC = 0.305: Context Matters

30.5% of county-level swing variance is between states, not within them. State-level forces explain nearly a third of why counties swung differently: media markets, campaign investment, governor effects, policy environment. County demographics alone cannot explain 2024. The same scale question runs through the [Dutch neighborhood analysis](/projects/public-attitudes/), at the other end of the variance decomposition.

### 2. Hispanic Population Share: Strongest Predictor

A 10 percentage-point increase in Hispanic population share predicted 0.46 additional points of Republican swing (p < 0.001), driven by South Texas, the Florida I-4 corridor, and Southern California. The finding speaks directly to the most-debated dynamic of the 2024 cycle.

### 3. Education Effects Vary, But Not Because of State Economics

Education polarization (college-educated counties swinging less Republican) varies significantly across states (random slope LR test χ² = 72.4, p < 0.001). State-level unemployment change does not explain why (cross-level interaction p = 0.48). The source of the variation is an open question; media environment, campaign strategy, and local party infrastructure are the candidate explanations.

## Data Pipeline

Five federal data sources, integrated on FIPS at the county level and on state where the source is state-level:
- **MEDSL**: MIT Election Data + Science Lab county-level returns (2020, 2024)
- **ACS 5-year**: Education, income, employment, Hispanic share, race, population, age
- **BLS LAUS**: State-level unemployment
- **Census 2024 gazetteer**: County land area (used to derive population density)
- **NCHS**: Urban-rural classification codes

(Two-party vote share and the swing itself are computed from the MEDSL returns, not separate data sources.)

## Policy Brief

A 3-page brief translating the model findings for campaign strategists, advocacy organizations, and political researchers. Covers ICC decomposition, the Hispanic swing puzzle, and education polarization variation. Available as [PDF](https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf).

## Links

- [Policy Brief: What State-Level Context Adds to the National Narrative](/writing/policy/county-election-swing-brief/) -- the applied version of the research finding, with download
- [Interactive Dashboard](https://us-election-county-swing.streamlit.app/) -- choropleth maps, demographic predictors, model results
- [GitHub Repository](https://github.com/kmazurek95/us-election-county-swing)
- [Policy Brief (PDF)](https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf)

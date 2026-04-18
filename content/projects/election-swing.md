---
title: "2020-2024 County-Level Partisan Swing"
type: "Electoral Geography / Multilevel Modeling"
summary: "Multilevel model of the 2020-2024 county-level partisan swing across 3,152 US counties nested in 49 states. 31% of swing variance is between states. Hispanic population share is the strongest predictor of rightward swing."
date: 2026-03-08
weight: 1
featured: true
repo: "https://github.com/kmazurek95/us-election-county-swing"
dashboard: "https://us-election-county-swing.streamlit.app/"
paper: "https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf"
stats:
  - "3,152 counties"
  - "49 states"
  - "ICC = 0.305"
  - "5 data sources"
tags: ["elections", "multilevel-modeling", "electoral-geography", "US-politics"]
---

## Role in the Portfolio

This is the US credibility project. It proves I can operate in the American political data ecosystem -- MEDSL, ACS, BLS, five sources merged on FIPS codes -- and produce findings relevant to live political debates. But the ICC finding is what makes it more than a credentials exercise. 31% of swing variance sitting at the state level is a structural finding, not a descriptive one. It's the same analytical logic as the Dutch neighborhoods project, applied to a domain US employers immediately recognize. The thesis proves NLP. The public attitudes project proves multilevel modeling. This one proves US political data competence. And the null cross-level interaction (p=0.416) demonstrates something reviewers respect: I follow the data rather than torturing it into significance.

## The Question

What county-level demographic and economic conditions predicted the 2020-2024 partisan swing? And does the effect of educational composition depend on local economic context?

## Three Headline Findings

### 1. ICC = 0.305: Context Matters

30.5% of county-level swing variance is between states, not within states. State-level forces -- media markets, campaign investment, governor effects, policy environment -- explain nearly a third of why counties swung differently. This is a structural finding, not a descriptive one. It means you cannot explain 2024 by looking at county demographics alone.

### 2. Hispanic Population Share: Strongest Predictor

A 10 percentage-point increase in Hispanic population share predicted 0.46 additional points of Republican swing (p < 10^-71). This is driven by South Texas, the Florida I-4 corridor, and Southern California. The finding speaks directly to the most-debated dynamic of the 2024 cycle.

### 3. Education Effects Vary, But Not Because of State Economics

Education polarization (college-educated counties swinging less Republican) varies significantly across states (random slope LR test p < 10^-16). But state-level unemployment change does not explain why (cross-level interaction p = 0.48). The variation exists but its source is an open question -- media environment, campaign strategy, and local party infrastructure are candidate explanations.

The null cross-level interaction is an honest finding. Reporting it demonstrates research maturity: the data did not support the initial hypothesis, and that is itself informative.

## Data Pipeline

Five sources merged on FIPS codes:
- **MEDSL**: MIT Election Data + Science Lab county-level returns (2020, 2024)
- **ACS 5-year**: Education, income, employment, Hispanic share, race, population, age
- **BLS**: State-level unemployment
- **Census**: Population density
- **Derived**: Two-party vote share calculation, swing computation

## Policy Brief

A 3-page brief translating model findings into actionable insights for campaign strategists, advocacy organizations, and political researchers. Covers ICC decomposition, the Hispanic swing puzzle, and education polarization variation. Available as [PDF](https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf).

## Links

- [Policy Brief: What State-Level Context Adds to the National Narrative](/writing/policy/county-election-swing-brief/) -- the applied version of the research finding, with download
- [Interactive Dashboard](https://us-election-county-swing.streamlit.app/) -- choropleth maps, demographic predictors, model results
- [GitHub Repository](https://github.com/kmazurek95/us-election-county-swing)
- [Policy Brief (PDF)](https://github.com/kmazurek95/us-election-county-swing/blob/main/docs/policy_brief.pdf)

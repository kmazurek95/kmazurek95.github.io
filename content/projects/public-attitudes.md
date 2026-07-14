---
title: "Income Inequality and Redistribution Preferences"
type: "Multilevel Modeling / Cross-National Analysis"
summary: "Multilevel analysis of how neighborhood and national inequality contexts shape individual redistribution preferences, using Dutch neighborhood data (CBS) and European Social Survey cross-national data."
date: 2025-06-01
weight: 6
featured: false
repo: "https://github.com/kmazurek95/public-attitudes-research"
dashboard: "https://public-attitudes-research-zcx3tbf4verisz7pavqgzb.streamlit.app/"
stats:
  - "4,748 individuals"
  - "1,572 neighborhoods"
  - "ICC = 3.4%"
  - "Dual R/Python"
tags: ["multilevel-modeling", "public-attitudes", "inequality", "European-Social-Survey"]
---

## The Question

Does your neighborhood's inequality affect your support for redistribution, independent of your own income? And if so, at what scale do these contextual effects actually operate?

## What I Found

At the neighborhood level, mostly no. Neighborhood inequality predicts redistribution support in bivariate models, but the association is fully absorbed by controls, and the neighborhood-level ICC stabilizes at 3.4%.

The cross-national extension using European Social Survey data found a more substantial ICC of 7.7% at the country level, and a significant income-by-Gini interaction (p = 0.002). In more unequal countries, the relationship between personal income and redistribution preferences is stronger: macro-level inequality conditions individual economic reasoning.

## Methodology

The analytical core is multilevel (mixed-effects) modeling: individuals nested in neighborhoods (Dutch data) and individuals nested in countries (ESS data). The dual R and Python implementation cross-validates results across statistical frameworks (lme4 vs. statsmodels) and catches implementation-specific assumptions.

Key methodological decisions:
- Linear mixed models are the correct specification given timeline and data structure
- Felten AIOE scores aggregated via Eurostat LFS weights provide the AI exposure measure for the ESS extension
- The simulation extension (in progress) uses ABM parameterized by ESS coefficients to explore redistribution attitude tipping dynamics under inequality shocks

## The Scale Question

The neighborhood ICC of 3.4% and the country ICC of 7.7% together tell a story: contextual effects on redistribution attitudes live at the institutional and national level, not the neighborhood level. This is consistent with welfare regime theory. The policy environment, not your immediate surroundings, shapes how you think about redistribution.

## Links

- [Streamlit Dashboard](https://public-attitudes-research-zcx3tbf4verisz7pavqgzb.streamlit.app/)
- [Shiny Dashboard (R)](https://kmazurek-analytics.shinyapps.io/income-inequality-attitudes/)
- [GitHub Repository](https://github.com/kmazurek95/public-attitudes-research)
- [Working paper: Neighborhood Inequality and Redistribution Preferences](/writing/academic/neighborhood-inequality/)
- [Case Study](https://github.com/kmazurek95/public-attitudes-research/blob/main/docs/portfolio/CASE_STUDY.md)

### Notebooks

- [Python Analysis](https://github.com/kmazurek95/public-attitudes-research/blob/main/python/analysis_report.ipynb) -- EDA, geographic merge, multilevel model building
- [R Analysis (rendered)](https://github.com/kmazurek95/public-attitudes-research/blob/main/R/analysis_report.md) -- lme4 models, ICC decomposition, diagnostics
- [Extended Analysis (R)](https://github.com/kmazurek95/public-attitudes-research/blob/main/R/analysis_extended.md) -- nested random effects, four-level variance decomposition

---
title: "Income Inequality and Redistribution Preferences"
type: "Multilevel Modeling / Cross-National Analysis"
summary: "Multilevel analysis of how neighborhood and national inequality contexts shape individual redistribution preferences, using Dutch neighborhood data (CBS) and European Social Survey cross-national data."
date: 2025-06-01
weight: 3
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

## Role in the Portfolio

This is the methodological bridge. It proves I understand that individual behavior can't be fully explained by individual characteristics alone -- context matters, and you need the right statistical architecture to model it. The thesis proves NLP capability; this project proves multilevel modeling depth. The dual R/Python implementation signals methodological bilingualism, but more importantly, the research question itself signals that I think about politics structurally, not just descriptively. And the small neighborhood-level ICC (3.4%) pushed me toward cross-national designs and the election project's state-level findings -- the question of what scale contextual effects operate at became the thread connecting everything that followed.

## The Question

Does your neighborhood's inequality affect your support for redistribution, independent of your own income? And if so, at what scale do these contextual effects actually operate?

## What I Found

At the neighborhood level, the answer is yes, but the effect is small. The ICC of 3.4% means that neighborhood-level variation explains only a small share of individual-level attitudes. This itself was an important finding -- it pushed the question toward what scale contextual effects actually operate at.

The cross-national extension using European Social Survey data found a more substantial ICC of 7.7% at the country level, and a significant income-by-Gini interaction (p = 0.002). In more unequal countries, the relationship between personal income and redistribution preferences is stronger. That is a structural finding about how macro-level inequality conditions individual economic reasoning.

## Methodology

The analytical core is multilevel (mixed-effects) modeling: individuals nested in neighborhoods (Dutch data) and individuals nested in countries (ESS data). The dual R and Python implementation is not just a technical exercise -- it cross-validates results across statistical frameworks (lme4 vs. statsmodels) and catches implementation-specific assumptions.

Key methodological decisions:
- Linear mixed models are the correct specification given timeline and data structure
- Felten AIOE scores aggregated via Eurostat LFS weights provide the AI exposure measure for the ESS extension
- The simulation extension (in progress) uses ABM parameterized by ESS coefficients to explore redistribution attitude tipping dynamics under inequality shocks

## The Scale Question

The neighborhood ICC of 3.4% and the country ICC of 7.7% together tell a story: contextual effects on redistribution attitudes live at the institutional/national level, not the neighborhood level. This is consistent with welfare regime theory -- the policy environment, not your immediate surroundings, shapes how you think about redistribution.

## Links

- [Streamlit Dashboard](https://public-attitudes-research-zcx3tbf4verisz7pavqgzb.streamlit.app/)
- [Shiny Dashboard (R)](https://kmazurek-analytics.shinyapps.io/income-inequality-attitudes/)
- [GitHub Repository](https://github.com/kmazurek95/public-attitudes-research)
- [Academic Paper](https://github.com/kmazurek95/public-attitudes-research/blob/main/docs/academic/PAPER.md)
- [Case Study](https://github.com/kmazurek95/public-attitudes-research/blob/main/docs/portfolio/CASE_STUDY.md)

### Notebooks

- [Python Analysis](https://github.com/kmazurek95/public-attitudes-research/blob/main/python/analysis_report.ipynb) -- EDA, geographic merge, multilevel model building
- [R Analysis (rendered)](https://github.com/kmazurek95/public-attitudes-research/blob/main/R/analysis_report.md) -- lme4 models, ICC decomposition, diagnostics
- [Extended Analysis (R)](https://github.com/kmazurek95/public-attitudes-research/blob/main/R/analysis_extended.md) -- nested random effects, four-level variance decomposition

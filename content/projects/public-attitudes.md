---
title: "Income Inequality and Redistribution Preferences"
type: "Multilevel Modeling"
summary: "A multilevel analysis of whether the income composition of a person's neighbourhood shapes their support for redistribution, using the SCoRE Netherlands 2017 survey linked to CBS neighbourhood statistics. The headline is a null."
date: 2025-06-01
weight: 7
aliases: ["/writing/academic/neighborhood-inequality/"]
repo: "https://github.com/kmazurek95/public-attitudes-research"
stats:
  - "3,931 respondents"
  - "1,382 buurten"
  - "ICC = 3.3%"
  - "Headline: null"
tags: ["multilevel-modeling", "public-attitudes", "inequality", "Netherlands"]
---

## The Question

Does the income composition of your neighbourhood affect your support for redistribution, independent of your own circumstances?

## What I Found

Mostly no. Neighbourhood income composition is a strong bivariate predictor (+3.29 per SD), but the association is fully absorbed once individual and neighbourhood controls enter: the M3 coefficient is +1.20 per SD (p = 0.21), a null. Between-neighbourhood variance is small — the empty-model ICC is 0.033, so roughly 96.7% of the variation in redistribution preferences sits within neighbourhoods rather than between them. No contextual effect of neighbourhood income composition survives once who lives there is accounted for.

A documented sensitivity specification that retains a collinear control (VIF > 27, r = 0.98 with the key predictor) gives a significant +1.93 per SD (p = 0.012) on a larger sample. It is reported as a sensitivity, not the headline, because retaining that control inflates the standard error on the key predictor without adding explanatory power.

## Methodology

Two-level mixed-effects models — individuals nested in buurten — estimated in R with `lme4`. The key predictor is the z-scored share of bottom-40%-income households in the buurt; the outcome is support for redistribution on a 0–100 scale. The analysis sample is complete cases matching a 2017 CBS buurt, with singleton buurten excluded.

The survey data come from SCoRE (*Sub-national Context and Radical Right Support in Europe*), Netherlands 2017, provider GfK — restricted-use and not included in the repository. The neighbourhood indicators are CBS table 83765NED (*Kerncijfers wijken en buurten* 2017), open data.

## Why It Matters

In a strong welfare state with relatively low inequality and limited residential segregation, the immediate socioeconomic environment does little of the work in shaping redistribution preferences. The finding points toward institutional and national context, rather than the neighbourhood, as the scale at which contextual effects operate — a scope condition developed further in the broader [research program](/research-program/).

## Links

- [GitHub Repository](https://github.com/kmazurek95/public-attitudes-research) — R pipeline code, a synthetic-data demo, and the aggregate model summary
- [Model summary (M0–M3)](https://github.com/kmazurek95/public-attitudes-research/blob/main/outputs/MODELS_SUMMARY_fixed.md)
- [Limitations](https://github.com/kmazurek95/public-attitudes-research/blob/main/docs/LIMITATIONS.md)
- [Reproducible R demo (synthetic data)](https://github.com/kmazurek95/public-attitudes-research/tree/main/r-pipeline-demo)

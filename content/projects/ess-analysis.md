---
title: "Redistribution Preferences and Institutional Trust Across Europe"
type: "Cross-National Analysis / Dual-DV Design"
summary: "Multilevel analysis of redistribution preferences and political trust across 28 European countries using ESS data, paired with agent-based simulations calibrated from the model coefficients. Redistribution preferences drift gradually under inequality shocks; in simulation, institutional trust tips through a self-reinforcing feedback loop."
date: 2025-08-01
weight: 6
repo: "https://github.com/kmazurek95/ess-redistribution-analysis"
stats:
  - "28 countries"
  - "ESS Round 9"
  - "Dual-DV design"
  - "AI exposure scores"
tags: ["multilevel-modeling", "public-attitudes", "European-Social-Survey", "welfare-states"]
---

## The Question

How do inequality shocks affect redistribution preferences and political trust across different welfare regime types? And do these two outcomes respond to the same structural pressures in the same way?

## What I Found

They do not. Redistribution preferences show a gradual, roughly linear response to inequality. Countries with higher Gini coefficients have populations somewhat more supportive of redistribution, and the income-by-inequality interaction is significant (p = 0.002). But the relationship is smooth.

Institutional trust behaves differently. In agent-based simulations calibrated from the multilevel model coefficients, trust tips rather than drifts: declining trust reduces institutional engagement, which reduces the information and experience that sustain trust, which erodes it further. If AI-driven labor market disruption is a structural shock, and trust can tip while redistribution preferences merely drift, the political crisis from AI may not look like a fight over who gets what. It may look like a legitimacy collapse.

The null direct effect of AI exposure on redistribution preferences (p = 0.857) is the motivating puzzle: if AI exposure does not directly shift what people want from the state, it may instead erode the trust that makes collective action through the state possible. That institutional-conditioning argument is formalized in the [working paper on institutional configurations and the social politics of AI](/writing/academic/typology-paper/), which uses the null as its starting point.

## Methodology

Cross-national multilevel modeling using European Social Survey Round 9 data (28 countries after excluding Slovakia); the redistribution model covers 26 countries (N = 31,393) and the trust model 25 (N = 31,033). AI exposure measured using Felten et al. AIOE scores aggregated via Eurostat Labour Force Survey occupational weights. Two dependent variables (redistribution preferences and institutional trust) modeled separately to compare response dynamics. Two numpy-based agent-based simulations, parameterized from the fitted coefficients, contrast the dynamics; the strength of the trust-governance feedback loop is a modeling assumption, not an empirical estimate.

## Links

- [GitHub Repository](https://github.com/kmazurek95/ess-redistribution-analysis)

---
title: "Redistribution Preferences and Institutional Trust Across Europe"
type: "Cross-National Analysis / Dual-DV Design"
summary: "Multilevel analysis of redistribution preferences and political trust across 29 European countries using ESS data. Key finding: redistribution preferences drift gradually under inequality shocks, while institutional trust tips through a self-reinforcing feedback loop."
date: 2025-08-01
weight: 4
featured: true
repo: "https://github.com/kmazurek95/ess-redistribution-analysis"
stats:
  - "29 countries"
  - "ESS Round 9"
  - "Dual-DV design"
  - "AI exposure scores"
tags: ["multilevel-modeling", "public-attitudes", "European-Social-Survey", "welfare-states"]
---

## Role in the Portfolio

This is where the distributional politics framework originates. The dual-DV finding is not a methodological curiosity. It suggests that different political attitudes respond to the same structural pressure through different mechanisms. Redistribution preferences adjust incrementally, in line with updated self-interest calculations. Trust collapses through a feedback loop: declining trust reduces institutional engagement, which reduces the information and experience that sustain trust, which erodes it further.

That distinction matters for AI. If AI-driven labor market disruption is a structural shock, and if institutional trust can tip while redistribution preferences merely drift, then the political crisis from AI may not look like a fight over who gets what. It may look like a legitimacy collapse. The null direct effect of AI exposure on redistribution preferences (p = 0.857) is the motivating puzzle for the institutional conditioning argument that runs through my current research. That argument is formalized in my [working paper on institutional configurations and the social politics of AI](/writing/academic/typology-paper/), which uses the ESS null finding as its starting point and builds a two-dimensional typology of OECD welfare regimes to explain it.

## The Question

How do inequality shocks affect redistribution preferences and political trust across different welfare regime types? And do these two outcomes respond to the same structural pressures in the same way?

## What I Found

They do not. Redistribution preferences show a gradual, roughly linear response to inequality. Countries with higher Gini coefficients have populations somewhat more supportive of redistribution, and the income-by-inequality interaction is significant. But the relationship is smooth.

Institutional trust shows a different pattern. The null direct effect of AI exposure on redistribution preferences was itself the motivating puzzle: if AI exposure does not directly shift what people want from the state, it may instead erode the trust that makes collective action through the state possible. The trust analysis suggests a threshold dynamic rather than a linear one.

## Methodology

Cross-national multilevel modeling using European Social Survey Round 9 data across 29 countries. AI exposure measured using Felten et al. AIOE scores aggregated via Eurostat Labour Force Survey occupational weights. Two dependent variables (redistribution preferences and institutional trust) modeled separately to compare response dynamics.

## Links

- [GitHub Repository](https://github.com/kmazurek95/ess-redistribution-analysis)

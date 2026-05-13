---
title: "Neighborhood Inequality and Redistribution Preferences"
subtitle: "Testing the Inferential Spaces Hypothesis in the Netherlands"
date: 2026-01-15
type: "Working Paper"
status: "Revised Working Paper · January 2026"
paper: "https://github.com/kmazurek95/public-attitudes-research/blob/main/docs/academic/PAPER.md"
repo: "https://github.com/kmazurek95/public-attitudes-research"
dashboard: "https://public-attitudes-research-zcx3tbf4verisz7pavqgzb.streamlit.app/"
authors: ["Kaleb Mazurek"]
affiliation: "University of Amsterdam, Amsterdam Institute for Social Science Research (AISSR)"
summary: "Multilevel test of whether neighborhood socioeconomic composition shapes redistribution preferences in the Netherlands. Neighborhood effects observed in bivariate models are fully absorbed by individual-level controls; cross-level interaction with individual wealth is also non-significant. The institutional and informational context, not the immediate socioeconomic environment, appears to matter more for preference formation."
keywords: ["income inequality", "redistribution preferences", "neighborhood effects", "multilevel modeling", "Netherlands", "contextual effects", "welfare state"]
tags: ["Academic", "Political Economy", "Quant"]
weight: 2
---

**Revised Working Paper · January 2026**

[Read the paper](https://github.com/kmazurek95/public-attitudes-research/blob/main/docs/academic/PAPER.md) · [Replication code](https://github.com/kmazurek95/public-attitudes-research) · [Interactive dashboard](https://public-attitudes-research-zcx3tbf4verisz7pavqgzb.streamlit.app/)

Originally completed as part of the Research Master's in Social Sciences graduation requirements (University of Amsterdam, February 2023). Revised January 2026.

---

Does your neighborhood's inequality shape what you think the state should do about it? The "inferential spaces" framework (Mijs, 2018) argues yes: neighborhood socioeconomic composition structures what residents observe about inequality, and that observed inequality conditions their redistributive preferences. Most tests of this mechanism originate in highly unequal, weakly redistributive contexts, above all the United States. This paper asks whether the mechanism operates in the Netherlands, a strong welfare state with relatively low inequality and limited residential segregation, where institutional context and expansive information environments may attenuate it.

## Abstract

Rising income inequality in Western democracies has not produced a corresponding increase in public demand for redistribution, a puzzle that has motivated growing attention to the role of local environments in shaping political attitudes. The "inferential spaces" framework (Mijs, 2018) posits that neighborhood socioeconomic composition structures what residents observe about inequality, thereby conditioning their redistributive preferences. Yet most empirical tests of this mechanism originate in highly unequal, weakly redistributive contexts, above all the United States. This study asks whether neighborhood effects on redistribution preferences operate in the Netherlands, a strong welfare state with relatively low inequality and limited residential segregation, where the inferential spaces mechanism may be attenuated by institutional context and expansive information environments. Using multilevel models with data from the SCoRE Netherlands 2017 survey (N = 4,748) linked to administrative neighborhood statistics from Statistics Netherlands, I find that neighborhood poverty concentration is associated with redistribution support in bivariate models (β = 3.46, p < 0.001) but that this association is fully absorbed by individual-level composition and neighborhood-level controls. A cross-level interaction between neighborhood composition and individual wealth is also non-significant. These null findings are substantively important: they suggest that the institutional and informational conditions under which people form preferences about redistribution may matter more than the socioeconomic character of their immediate surroundings.

## Key findings

- **Bivariate effect is real.** Neighborhood poverty concentration predicts redistribution support before controls (β = 3.46, p < 0.001), consistent with what Mijs's framework would expect.
- **The effect does not survive controls.** Adding individual-level composition and neighborhood-level controls fully absorbs the bivariate association. The neighborhood-level ICC stabilizes at approximately 3.4%.
- **No cross-level interaction.** The interaction between neighborhood composition and individual wealth, which Mijs's framework predicts should be observable in residentially segregated information environments, is non-significant in the Dutch case (β = 0.181, SE = 0.343, p = 0.598).
- **Measurement choice matters.** An alternative operationalization using income polarization rather than poverty concentration yields a significant negative effect (β = -1.84, p < 0.05). The substantive conclusion is sensitive to how neighborhood inequality is measured, which strengthens rather than weakens the scope-condition reading: what counts as "the observable inequality of a neighborhood" is itself an analytical choice.
- **The null is substantively important.** In a strong welfare state with relatively low inequality and limited residential segregation, the institutional and informational context appears to do more work than the immediate socioeconomic environment in shaping preferences. This is a scope condition for the inferential spaces framework, not a refutation.

## Data and methods

SCoRE Netherlands 2017 survey microdata (N = 4,748 individuals, reduced from an initial sample of 8,013 via listwise deletion on the analysis variables) linked to administrative neighborhood statistics from Statistics Netherlands (CBS). Three geographic levels (neighborhoods, districts, municipalities) were tested; 1,572 neighborhoods are in the final analysis. Multilevel (mixed-effects) models estimated in both R (lme4) and Python (statsmodels) for cross-implementation validation. Ten-plus model specifications run, including random intercept, random slope, and cross-level interaction designs. The full four-level variance decomposition (1.4 percent neighborhood, 0.8 percent district, 1.2 percent municipality, 96.6 percent within-individual) reinforces the central finding: even cumulatively, area-level context explains less than 4 percent of variance in redistribution preferences. Full replication code, model diagnostics, and the underlying paper are in the [GitHub repository](https://github.com/kmazurek95/public-attitudes-research).

## How this fits the broader program

The small neighborhood-level ICC (3.4%) was itself the finding that opened the next round of questions. If contextual effects do not operate at the neighborhood level in the Dutch case, at what scale do they operate? The follow-up [cross-national analysis](/projects/ess-analysis/) using European Social Survey Round 9 found country-level ICCs of 7.7%, with a significant income-by-Gini interaction (p = 0.002). The combined picture: contextual effects on redistribution attitudes live at the institutional and national level, not the neighborhood level. This is the empirical observation that motivated the institutional-conditioning framing of the broader research program.

## Cite as

Mazurek, K. (2026). *Neighborhood Inequality and Redistribution Preferences: Testing the Inferential Spaces Hypothesis in the Netherlands*. Revised Working Paper, January 2026. Available at https://kmazurek95.github.io/writing/academic/neighborhood-inequality/

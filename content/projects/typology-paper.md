---
title: "Institutional Configurations and the Social Politics of AI"
type: "Comparative Political Economy / Two-Dimensional Typology"
summary: "Two-dimensional typology of 29 OECD countries along AI task-profile and labor market dualization axes. The first signature contribution of the research program. Working Paper v1.0, April 2026."
date: 2026-04-17
weight: 1
featured: true
repo: "https://github.com/kmazurek95/typology-paper"
paper: "/pdfs/Mazurek_2026_Typology_v1.pdf"
stats:
  - "29 countries"
  - "PIAAC + OECD EPL v4"
  - "AIOE validation r = 0.71"
  - "4 populated cells"
tags: ["typology", "comparative-political-economy", "welfare-states", "AI", "OECD"]
---

## Role in the Portfolio

This is the first signature contribution of the research program. The other four projects establish methodological capability and the empirical pattern that institutional context outperforms individual and local conditions at every scale tested. This paper formalizes the institutional argument into a typology that generates testable cross-level hypotheses about how AI exposure interacts with welfare-state configurations to shape political outcomes. Where the other projects are infrastructure for the argument, this paper is the synthesis output.

## The Question

Why do countries with similar levels of AI exposure produce such different political responses? Existing welfare-regime classifications miss two institutional dimensions that do the explanatory work: the type of AI effect a workforce faces (displacement versus complementarity), and how the costs of that effect are distributed across the labor market (broadly shared versus concentrated on outsiders).

## What I Found

The two-dimensional space identifies institutional variation that welfare-regime classifications obscure. Spain clusters with the Nordics after its 2012 and 2021 labor market reforms. Sweden's deep formal dualization separates it from the rest of Scandinavia. The Anglophone countries group with Germany rather than forming a liberal bloc. All four cells of the typology are empirically populated, confirming the two dimensions are analytically independent rather than collapsing onto a single diagonal.

The PIAAC task-profile measure externally validates against country-level Felten AIOE scores at r = 0.71 across 21 European countries (Spearman rho = 0.70).

Aggregate evidence from the OECD Risks that Matter 2022 survey provides partial, directional support. The displacement-complementarity axis predicts redistribution demand in the expected ordering (Cell 3 > Cell 2 > Cell 1 > Cell 4). The dualization axis does not predict aggregate preferences, a pattern consistent with the welfare-attitude tradition scope condition the framework identifies. The null is what motivates the v2 specification, in preparation.

## The Theoretical Move

Dualization scholarship emerged around deindustrialization and offshoring: threats to routine manual workers that the insider category was built to insulate. AI disrupts cognitive workers in administrative, legal, and technical roles, the people the insider category was constructed to protect. Whether the same institutional architecture can absorb a threat to its own protected core is the question the typology addresses.

## Methodology

The analysis draws on PIAAC Cycle 2 (2022–2023) country-level means on ICT, numeracy, and reading skill use at work; OECD Employment Protection Legislation Version 4 sub-indices (EPRC and EPT); OECD Risks that Matter 2022 Collected Statlinks; and Eurostat Labour Force Survey employment shares by ISCO-08 major group for the AIOE validation.

- **Axis 1 (AI task profile):** First principal component of the three PIAAC skill-use scales. Loadings: ICT = 0.52, numeracy = 0.62, reading = 0.59. Explains 73 percent of variance.
- **Axis 2 (Labor market dualization):** EPRC minus EPT from OECD EPL Version 4.
- **Cluster boundaries:** Drawn at sample medians on both dimensions.
- **External validation:** Pearson correlation between the PCA-derived task-profile score and country-level Felten AIOE aggregated via Eurostat employment shares (r = 0.71, p < .001, N = 21).

## What V2 Adds

Version 2, in preparation, extends the analysis with individual-level microdata from the OECD Risks that Matter survey (2022 and 2024 waves), pooled and merged with PIAAC task profiles and OECD EPL Version 4 indicators. The v2 specification estimates multilevel models with cross-level interactions to test whether individual AI occupational exposure has different preference effects across institutional configurations, with country-level controls for welfare-attitude tradition.

## Links

- [Full working paper page](/writing/academic/typology-paper/) for abstract, figures, citation, and complete academic treatment
- [Working Paper PDF (v1.0)](/pdfs/Mazurek_2026_Typology_v1.pdf)
- [GitHub Repository](https://github.com/kmazurek95/typology-paper) for replication code and data

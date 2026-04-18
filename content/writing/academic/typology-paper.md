---
title: "Institutional Configurations and the Social Politics of AI"
subtitle: "A Two-Dimensional Typology of OECD Countries"
date: 2026-04-17
type: "Working Paper"
status: "Working Paper v1.0 — April 2026"
socarxiv_status: "SocArXiv preprint forthcoming"
paper: "/pdfs/Mazurek_2026_Typology_v1.pdf"
repo: "https://github.com/kmazurek95/typology-paper"
authors: ["Kaleb Mazurek"]
affiliation: "Independent Researcher, Chicago, IL"
summary: "Two-dimensional mapping of 29 OECD countries along AI task-profile and labor market dualization axes; descriptive typology with testable cross-level hypotheses for the politics of welfare reform."
jel_codes: ["J24", "J68", "O33", "P16"]
keywords: ["artificial intelligence", "welfare state", "labor market dualization", "automation", "redistribution preferences", "social investment", "comparative political economy", "OECD"]
tags: ["Academic", "Political Economy", "AI Evaluation"]
weight: 1
---

**Working Paper v1.0 · April 2026 · SocArXiv preprint forthcoming**

[**Download PDF**](/pdfs/Mazurek_2026_Typology_v1.pdf) · [Replication code and data](https://github.com/kmazurek95/typology-paper)

The SocArXiv preprint will replace the GitHub-hosted PDF as the canonical citation once posted; this page will be updated with the SocArXiv handle and DOI at that time.

---

Why do countries with similar levels of AI exposure produce such different political responses? This paper argues that existing welfare-regime classifications miss two institutional dimensions that do the explanatory work: the type of AI effect a workforce faces (displacement versus complementarity), and how the costs of that effect are distributed across the labor market (broadly shared versus concentrated on outsiders).

## Abstract

This paper develops a two-dimensional typology of OECD countries that identifies the institutional conditions shaping social exposure to AI. The first dimension captures the type of AI effect a country's workforce faces, displacement or complementarity, measured through task-profile composition from PIAAC. The second captures the depth of labor market dualization, the gap between employment protections for permanent and temporary workers under OECD EPL Version 4. Mapping 29 countries reveals institutional variation that welfare-regime classifications obscure: Spain clusters with the Nordics after its 2012 and 2021 labor market reforms, Sweden's deep formal dualization separates it from the rest of Scandinavia, and the Anglophone countries group with Germany rather than forming a liberal bloc. The theoretical contribution is to recast a contrast the existing literature has not posed. Dualization scholarship emerged around deindustrialization and offshoring, threats to routine manual workers the insider category was built to insulate; AI now disrupts cognitive workers in administrative, legal, and technical roles, the people the insider category was constructed to protect. Whether the same institutional architecture can absorb a threat to its own protected core is the question the typology addresses. Aggregate evidence from the OECD Risks that Matter 2022 survey supports the displacement-complementarity axis directionally; the dualization axis does not predict aggregate preferences, a pattern consistent with the welfare-tradition scope condition identified in the framework. The paper's contribution is the framework itself: two institutional dimensions, a reproducible mapping of OECD countries onto them, and a set of cross-level hypotheses for the individual-level analyses it invites.

## Key findings

- **Integrates three previously siloed literatures** — AI exposure measurement, automation-and-preferences, and dualization — into a single two-dimensional framework, with a novel theoretical claim: the insider-outsider architecture built to insulate industrial workers from offshoring now faces a shock aimed at the cognitive workers that architecture was designed to protect.
- **All four cells are empirically populated**, confirming the two dimensions are analytically independent rather than collapsing onto a single diagonal. The PIAAC task-profile measure externally validates against country-level Felten AIOE scores at *r* = 0.71 across 21 European countries.
- **Several country placements diverge from standard welfare regime classifications** in theoretically informative ways. Spain lands with the Nordics after its 2012 and 2021 labor market reforms. Sweden's deep formal dualization separates it from the rest of Scandinavia. The Anglophone countries group with Germany rather than forming a liberal bloc. Italy's post-Jobs Act compression repositions it. These placements are what the two-dimensional framework is built to detect.
- **Aggregate OECD Risks that Matter 2022 data provides partial, directional support.** The displacement-complementarity axis predicts redistribution demand in the expected ordering (Cell 3 > Cell 2 > Cell 1 > Cell 4). The dualization axis does not predict aggregate preferences — a pattern consistent with the welfare-attitude tradition scope condition identified in the framework. The null is what motivates the v2 multilevel specification, forthcoming as a separate SocArXiv preprint.

## The two-dimensional space

![OECD Countries: AI Task Profile × Labor Market Dualization](/images/typology/figure1_typology_scatter.png)
*Figure 1. OECD Countries: AI Task Profile × Labor Market Dualization. Cluster boundaries at sample medians. Source: author's calculations from PIAAC Cycle 2 and OECD EPL Version 4.*

Twenty-nine OECD countries are positioned along Axis 1 (task-profile composition, the first principal component of PIAAC skill-use indicators, explaining 73 percent of variance) and Axis 2 (the EPRC–EPT dualization gap from OECD EPL Version 4). All four cells are populated. Germany sits near the center of the space and functions as a diagnostic intermediate case: a moderately complementary task profile (the precision manufacturing core) alongside a dualization gap just above the median (the Hartz-era expansion of non-standard employment). The two dimensions identify a structural tension the *conservative-corporatist* regime label cannot: AI augments work in the manufacturing-export core where insider protections are strongest, while displacing work in the service-sector periphery where outsider exposure has been institutionally manufactured.

## Preference patterns and the honest null

![Welfare Preferences by Typology Cluster (RTM 2022)](/images/typology/figure2_preferences_by_cluster.png)
*Figure 2. Welfare Preferences by Typology Cluster (RTM 2022). Cluster means with country-level observations for redistribution and education-spending preferences. Source: author's calculations from OECD Risks that Matter 2022 Collected Statlinks.*

The pattern is partially consistent with the framework's predictions. Redistribution demand is highest in Cell 3 (displacement + narrow gap, ~65%) and lowest in Cell 1 (complementarity + narrow gap, ~54%), consistent with the prediction that displacement-type exposure generates stronger compensatory demand. The dualization axis does not predict aggregate redistribution demand: Cell 4 shows *lower* redistribution demand than Cell 3 despite deeper dualization. Education-spending preferences run opposite to the social-investment prediction, with displacement-exposed cells (3 and 4) showing the highest demand rather than complementarity-exposed cells.

These results are not a refutation of the framework but a scope condition made empirical. Cell 4 groups post-communist countries (Czechia, Latvia, Poland), East Asian coordinated economies (Japan, Korea), and one Nordic outlier (Sweden). These countries share structural positions on the two dimensions but differ profoundly in welfare-attitude traditions. The aggregate comparison cannot separate the structural effect of deep dualization from baseline tradition differences. Individual-level estimation with country-level controls for welfare tradition is what it takes to adjudicate whether the dualization mechanism works as theorized — which is exactly the specification v2 is built for.

## Data and methods

The analysis draws on PIAAC Cycle 2 (2022–2023) country-level means on ICT, numeracy, and reading skill use at work; OECD Employment Protection Legislation Version 4 sub-indices (EPRC and EPT); OECD Risks that Matter 2022 Collected Statlinks; and Eurostat Labour Force Survey employment shares by ISCO-08 major group for the AIOE validation. Axis 1 is the first principal component of the three PIAAC skill-use scales (loadings: ICT = 0.52, numeracy = 0.62, reading = 0.59). Axis 2 is EPRC − EPT. Cluster boundaries are drawn at the sample medians on both dimensions. The external validation uses a Pearson correlation between the PCA-derived task-profile score and country-level Felten AIOE aggregated via Eurostat employment shares (*r* = 0.71, *p* < .001, *N* = 21; Spearman rho = 0.70). Full replication code and data are available at the [GitHub repository](https://github.com/kmazurek95/typology-paper). A SocArXiv preprint will follow, at which point the SocArXiv version becomes the canonical citation.

## v2: what's coming

Version 2, in preparation, extends the analysis with individual-level microdata from the OECD Risks that Matter survey (2022 and 2024 waves, received from the OECD Directorate for Employment, Labour and Social Affairs), pooled and merged with PIAAC task profiles and OECD EPL Version 4 indicators. Individual AI exposure is operationalized through NACE industry-based Felten AIOE scores; insider–outsider status through an OECD-derived standard/non-standard worker flag; and the main outcome through a three-item technology-framed policy scale drawn from the RTM digitalization battery. The v2 specification estimates multilevel models with cross-level interactions to test whether individual AI occupational exposure has different preference effects across institutional configurations, with country-level controls for welfare-attitude tradition. Identification leans on a wave-by-exposure interaction in the spirit of Bartik-style fixed-treatment difference-in-differences. The v2 draft will be posted to SocArXiv as a separate preprint and linked from this page when available.

## Cite as

Mazurek, K. (2026). *Institutional Configurations and the Social Politics of AI: A Two-Dimensional Typology of OECD Countries*. Working Paper v1.0, April 2026. Available at https://kmazurek95.github.io/writing/academic/typology-paper/

*A SocArXiv preprint with stable handle and DOI is forthcoming; once posted, it will become the canonical version for citation.*

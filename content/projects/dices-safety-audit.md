---
title: "A Measurement Audit of the DICES-350 Safety Taxonomy"
type: "Psychometric Audit / AI Safety Evaluation"
summary: "A psychometric audit of the DICES-350 conversational-AI safety annotation taxonomy, treated as a measurement instrument rather than a fixed rubric. Tests whether its harm categories are reliable, dimensionally coherent, and empirically distinct at full rater power."
date: 2026-07-02
weight: 1
featured: true
repo: "https://github.com/kmazurek95/dices-safety-audit"
stats:
  - "43,050 ratings"
  - "123-rater panel"
  - "HTMT 0.922"
  - "18/23 base-rate artifacts"
tags: ["AI-evaluation", "psychometrics", "measurement", "reliability", "factor-analysis"]
---

## Role in the Portfolio

This is the anchor of my AI evaluation and measurement work, and the project that connects it to the political economy side. Most safety evaluation reports a model's harm rate against human labels and never asks whether the labels themselves hold up as a measurement instrument. This one does. It takes a published safety taxonomy, treats it as a survey scale, and runs the audit you would run on any scale before trusting a score built on it.

For evaluation work, it brings a social scientist's measurement toolkit to an AI safety scale: construct validity, inter-rater reliability under heavy skew, factor structure, and the judgment to say "cannot be established" when that is the honest answer. That taxonomy is also a governance object: it decides what counts as "harmful content" versus "unfair bias" and whose judgments define harm, so what it can and cannot measure sets the ceiling on any safety standard built on it.

## The Question

Do the categories of a conversational-AI safety taxonomy behave as reliable, dimensionally coherent, and empirically distinct constructs, or do they collapse under measurement? The data is DICES-350: 350 multi-turn adversarial conversations, each rated by the same panel of 123 crowd raters on a 23-item safety taxonomy (43,050 ratings), plus an expert gold layer.

## What I Did

Four standard psychometric methods, each taken only as far as the evidence supports.

1. **Reliability.** Three agreement coefficients per category (Fleiss' kappa, observed agreement, Gwet's AC1), item-bootstrap confidence intervals, and a classification that keys on the interval bounds rather than the point estimates. This separates genuine disagreement from the kappa paradox, where skewed prevalence deflates kappa even when raters almost always agree.
2. **Dimensionality.** Exploratory factor analysis under both Pearson and tetrachoric correlations, with parallel analysis fixing the factor count before the loadings are inspected.
3. **Discriminant validity.** The heterotrait-monotrait ratio (HTMT), chosen because the data produces improper (Heywood) solutions at n = 350 under extreme skew, which breaks confirmatory factor analysis.
4. **Decoupling.** A base-rate decomposition that separates real crowd-expert agreement from the artifact of the crowd's default "No."

## Findings

{{< finding label="Three distinct problems, held separate" >}}
The taxonomy is **not unidimensional** (more than one factor under either correlation estimator); its **reliability cannot be established for most categories** under conservative, interval-based criteria (18 of 23 categories classify as base-rate artifacts, 0 as definitively reliable); and its two largest categories, **harmful content and unfair bias, are not empirically discriminable** (HTMT 0.922 under the sound tetrachoric estimator).
{{< /finding >}}

One mechanism drives all three: base-rate sparsity from rare, inconsistently applied categories. The failure is not uniform. Political affiliation coheres as its own construct, carrying the highest between-conversation signal in the taxonomy (ICC1 0.377) and loading as its own factor -- a dimensionality property, not a kappa artifact. Two findings were revised on evidence when pre-registered robustness checks contradicted the initial reading, both fixed before the final analysis ran, so the revisions are consequences of the method rather than post-hoc adjustments.

## Methodology Notes

The hard part is knowing how far to push each claim, not running the statistics. "Reliability cannot be established" is a statement of indeterminacy, not a demonstrated failure, and keeping those two apart is the whole point. The classification keys on confidence-interval bounds, so a category only earns a definitive label when its entire interval sits on one side of the threshold. Borrowed cutoffs (Landis-Koch for kappa, Henseler for HTMT) sit next to the raw coefficients so no threshold is doing hidden work. The modules regenerate every table from source; the plots are checked in as static artifacts. Same measurement thinking as [the congressional-speech pipeline](/projects/thesis-pipeline/) and the argument in ["What Political Science Can Teach AI Evaluation"](/writing/essays/political-science-ai-evaluation/).

## Links

- [GitHub Repository](https://github.com/kmazurek95/dices-safety-audit) -- analysis modules, methodology writeup, and generated result tables
- [Methodology](https://github.com/kmazurek95/dices-safety-audit/blob/main/docs/METHODOLOGY.md) -- full methods, threshold conventions, and literature treatment
- [Taxonomy codebook](https://github.com/kmazurek95/dices-safety-audit/blob/main/docs/taxonomy.md) -- what each rated column means

Data: DICES-350, from `google-research-datasets/dices-dataset` (CC-BY 4.0). Source paper: Aroyo et al. (2023), "DICES Dataset: Diversity in Conversational AI Evaluation for Safety," [arXiv:2306.11247](https://arxiv.org/abs/2306.11247).

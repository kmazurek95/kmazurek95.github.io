---
title: "Interest Group Prominence in Congressional Speech"
type: "NLP Pipeline / Text Classification"
summary: "Built an end-to-end NLP pipeline classifying interest group prominence across 78,000 congressional floor speeches from the 114th-115th Congress. Measures how organized interests shape the informational environment of legislative debate."
date: 2025-09-01
weight: 2
featured: true
repo: "https://github.com/kmazurek95/ThesisPipelineRework"
dashboard: "https://thesispipelinerework-emngd3hbxghtkfzbe9secw.streamlit.app/"
paper: "https://github.com/kmazurek95/ThesisPipelineRework/blob/main/docs/Thesis_UvA_Kaleb_Mazurek.pdf"
stats:
  - "78K documents"
  - "F1 = 0.91"
  - "kappa = 0.82"
  - "53,892 mentions"
tags: ["NLP", "text-classification", "multilevel-modeling", "congressional-data"]
---

## Role in the Portfolio

This is the technical foundation. It proves I can formulate a measurement problem (how do you operationalize "prominence"?), build a classifier, validate it with inter-rater reliability, and produce interpretable results at scale. For research audiences, the question and the methodology matter. For AI evaluation audiences, the measurement design thinking -- construct validity, annotation reliability, threshold optimization -- is the exact skillset that distinguishes senior evaluation roles from junior ones. Each project in my portfolio fills a gap the others don't. This one proves I can do computational text analysis.

## The Question

How prominent are interest groups in congressional floor speeches, and what predicts that prominence? This project operationalizes a concept that does not have a clean label -- "interest group presence in political speech" -- and builds the measurement infrastructure to study it at scale.

## What I Built

A five-stage NLP pipeline that processes raw Congressional Record documents from the GovInfo API into a multi-level analytical dataset:

1. **Data Collection**: Custom Python scraper pulling House and Senate granules from the GovInfo API with retry logic and rate limiting
2. **Text Processing**: HTML parsing, sentence segmentation, dictionary-based entity extraction with character offsets against 5,447 organizations
3. **Classification**: TF-IDF + Logistic Regression with group-aware cross-validation and threshold optimization, improving F1 from 0.79 to 0.91
4. **Integration**: Merges mentions with lobbying data (OpenSecrets), legislator metadata, and bill references into a 4-level analytical dataset
5. **Analysis**: Logistic regression and OLS models with automated figure/table generation

## Key Findings

The pipeline identified 53,892 mentions of 1,903 unique organizations across the 114th-115th Congress. Inter-rater reliability reached Cohen's kappa of 0.82, meaning the measurement is defensible and reproducible.

The classification approach uses SHAP feature attribution to make the model interpretable -- you can see exactly which textual features drive prominence classification for any given mention.

## Methodology Notes

The measurement design challenge here is the interesting part. "Prominence" is not a binary observable -- it requires careful construct definition, annotation scheme design, and threshold optimization. The same thinking that goes into operationalizing hard-to-measure social science concepts applies directly to designing rubrics for AI evaluation. I wrote about this connection in my [bridging article on LinkedIn](https://www.linkedin.com/in/kaleb-mazurek/).

## Links

- [Interactive Dashboard](https://thesispipelinerework-emngd3hbxghtkfzbe9secw.streamlit.app/) -- explore regression results, case studies, and model diagnostics
- [GitHub Repository](https://github.com/kmazurek95/ThesisPipelineRework) -- full pipeline code with documentation
- [Methodology Documentation](https://github.com/kmazurek95/ThesisPipelineRework/blob/main/docs/METHODOLOGY.md)
- [Known Limitations](https://github.com/kmazurek95/ThesisPipelineRework/blob/main/docs/KNOWN_LIMITATIONS.md)
- [Full Thesis (PDF)](https://github.com/kmazurek95/ThesisPipelineRework/blob/main/docs/Thesis_UvA_Kaleb_Mazurek.pdf)

### Notebooks

- [Analysis Showcase](https://github.com/kmazurek95/ThesisPipelineRework/blob/main/notebooks/Analysis_Showcase.ipynb) -- end-to-end analysis with 3 regression models and 5+ visualizations
- [Classification Deep Dive](https://github.com/kmazurek95/ThesisPipelineRework/blob/main/notebooks/Classification_Analysis.ipynb) -- SHAP attribution, error analysis, calibration plots
- [Exploratory Analysis](https://github.com/kmazurek95/ThesisPipelineRework/blob/main/notebooks/Exploratory_Analysis.ipynb) -- distribution analysis, lobbying vs. prominence patterns

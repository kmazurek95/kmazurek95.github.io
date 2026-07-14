---
title: "Interest Group Prominence in Congressional Speech"
type: "NLP Pipeline / Text Classification"
summary: "Built an end-to-end NLP pipeline classifying interest group prominence across 78,000 Congressional Record documents from the 114th-115th Congress. Measures how organized interests shape the informational environment of legislative debate."
date: 2025-09-01
weight: 3
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

## The Question

How prominent are interest groups in congressional floor speeches, and what predicts that prominence? This project operationalizes a concept that does not have a clean label, "interest group presence in political speech," and builds the measurement infrastructure to study it at scale.

## What I Built

A five-stage NLP pipeline that processes raw Congressional Record documents from the GovInfo API into a multi-level analytical dataset. This is the post-graduation rebuild of my MSc thesis pipeline; the original thesis classifier was an SVM with count-vectorizer features (per-class F1 = 0.79 prominent / 0.65 non-prominent), and the rebuild is a separate artifact with its own corpus and metrics:

1. **Data Collection**: Custom Python scraper pulling House and Senate granules from the GovInfo API with retry logic and rate limiting
2. **Text Processing**: HTML parsing, sentence segmentation, dictionary-based entity extraction with character offsets against a lookup dictionary of 5,447 advocacy organizations (Washington Representatives Study)
3. **Classification**: TF-IDF + Logistic Regression with group-aware cross-validation and threshold optimization, reaching a test F1 of 0.91 (threshold-tuned on the held-out test set)
4. **Integration**: Merges mentions with lobbying data (OpenSecrets), legislator metadata, and bill references into a 4-level analytical dataset
5. **Analysis**: Logistic regression and OLS models with automated figure/table generation

## Key Findings

The pipeline identified 53,892 mentions of 2,260 unique organizations across the 114th-115th Congress. Agreement between the classifier and the human gold labels on the held-out test set reached Cohen's kappa of 0.82 (labels from a single coder).

The classification approach uses SHAP feature attribution to make the model interpretable -- you can see exactly which textual features drive prominence classification for any given mention.

## Methodology Notes

"Prominence" is not a binary observable. It requires construct definition, annotation scheme design, and threshold optimization, and the same thinking that goes into operationalizing hard-to-measure social science concepts applies directly to designing rubrics for AI evaluation. I wrote about this connection in ["What Political Science Can Teach AI Evaluation"](/writing/essays/political-science-ai-evaluation/).

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

---
title: "What Political Science Can Teach AI Evaluation"
date: 2026-03-05
summary: "AI evaluation teams keep reinventing concepts that social scientists solved decades ago. Five methodological parallels between political science research and AI model evaluation."
tags: ["AI-evaluation", "methodology", "measurement"]
type: "Essay"
---

AI evaluation teams keep reinventing concepts that social scientists solved decades ago. Inter-rater reliability, construct validity, sampling bias -- these are not new problems. They are well-studied problems with decades of methodological literature behind them, and the AI evaluation field is rediscovering them from scratch.

This piece draws five parallels between political science research methodology and the challenges facing AI evaluation today. It was originally published on [LinkedIn](https://www.linkedin.com/in/kaleb-mazurek/).

## 1. Measurement Validity

In political science, we obsess over whether our measures actually capture what we claim they capture. When I operationalized "interest group prominence" for my thesis, I had to define precisely what counts as a prominent mention versus a passing reference, test that definition against edge cases, and prove that trained coders could apply it consistently.

AI evaluation rubrics face the same challenge. When you ask annotators to rate whether a model response is "helpful" or "harmful," you need the same construct validity work. What does "helpful" mean in context? Can two people agree on where the line falls? The social science toolkit for answering these questions already exists.

## 2. Inter-Rater Reliability

Cohen's kappa and Krippendorff's alpha are standard tools in content analysis. They measure whether trained coders agree with each other, and by extension, whether the coding scheme is actually capturing something real rather than individual interpretation.

AI evaluation has the same need. If three annotators disagree on whether a model output is "factually accurate," that disagreement is information about the rubric, not just noise to be averaged away. The social science response -- calibration sessions, iterative codebook refinement, pilot rounds -- maps directly onto evaluation program design.

## 3. Construct Validity

This goes deeper than measurement. Construct validity asks whether the thing you are measuring actually relates to the broader concept you care about. In survey research, you validate a new measure by showing it correlates with established measures of the same concept and does not correlate with measures of unrelated concepts.

AI benchmarks need the same validation. A benchmark that scores models on "reasoning ability" should correlate with other measures of reasoning and not just measure pattern matching. Without construct validation, you do not know what your benchmark is actually testing.

## 4. Sampling and Selection Bias

Every survey researcher knows that who you sample determines what you can conclude. A convenience sample of Twitter users tells you about Twitter users, not about the public. The same logic applies to evaluation test sets. If your test cases are drawn from a narrow distribution of prompts, your evaluation tells you about model performance on that distribution, not about model capability in general.

The social science toolkit for thinking about sampling frames, coverage error, and generalizability applies directly to evaluation dataset design.

## 5. From Rubrics to Research Programs

The most important parallel is methodological: social scientists treat measurement as a research problem, not an administrative task. Developing a valid, reliable measure is itself a contribution. AI evaluation would benefit from the same orientation -- treating rubric design, annotator training, and benchmark construction as methodological work deserving rigorous documentation and iteration.

---

*This is the short version. The full article is available on [LinkedIn](https://www.linkedin.com/in/kaleb-mazurek/).*

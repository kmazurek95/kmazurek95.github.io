---
title: "Research Program"
layout: "single"
type: "page"
---

## Two tracks

I work on AI as a quantitative social scientist, from two directions at once. One asks whether we can trust the numbers we attach to AI systems: are the human labels, safety taxonomies, and benchmarks that evaluation runs on reliable enough to carry the claims built on them? The other asks what AI does to institutions: how it moves through labor markets, energy systems, and welfare states, and how institutional design decides who absorbs the shock.

They meet at one idea: measurement is not neutral. How we choose to quantify AI safety, harm, and labor is itself a governance decision, because the instrument that produces a number sets the terms of every claim built on it. The measurement track audits that instrument; the political-economy track follows what it decides.

## Measurement and evaluation of AI

The question here is narrow and load-bearing: before you trust a score, can you trust the instrument that produced it? A model's measured harm rate is only as good as the labels it is scored against, and a category annotators cannot apply consistently cannot support a trustworthy number. So I treat evaluation schemes as measurement instruments and run the audit a psychometrician runs on any survey scale: reliability, dimensionality, discriminant validity, and the uncertainty around each.

### [A Measurement Audit of the DICES-350 Safety Taxonomy](/projects/dices-safety-audit/)

I audited a published conversational-AI safety taxonomy at full rater power, 123 raters and 43,050 ratings, and found three problems that have to be kept separate: it is not unidimensional, its reliability cannot be established for most categories under conservative criteria (18 of 23 are base-rate artifacts), and its two largest categories, harmful content and unfair bias, are not empirically discriminable (HTMT 0.922). No prior work applies a heterotrait-monotrait discriminant test to the DICES taxonomy.

### [Interest Group Prominence in Congressional Speech](/projects/thesis-pipeline/)

Before AI, the same measurement-design problem showed up in political text: how do you operationalize "prominence" and build a defensible classifier for it across 78,000 Congressional Record documents? The post-graduation rebuild of the pipeline reached a test F1 of 0.91, with classifier-human agreement at Cohen's kappa = 0.82. Construct definition, annotation reliability, threshold optimization: the skill set an evaluation audit runs on. I wrote about the transfer in ["What Political Science Can Teach AI Evaluation"](/writing/essays/political-science-ai-evaluation/).

## Political economy of AI

The question here predates AI: when structural economic forces create winners and losers, what determines whether societies respond with solidarity or drift? I started with inequality, redistribution preferences, and welfare states, and across four projects at different scales the same result kept appearing. **Institutional context outperforms individual and local conditions** at every scale I have tested.

- Neighborhood-level inequality explains **3.4%** of variance in Dutch redistribution attitudes.
- Country-level institutions explain **7.7%** of cross-national redistribution variance, with a significant income × inequality interaction (*p* = 0.002).
- State-level context explains **31%** of county-level partisan swing in the 2020-2024 US election (ICC = 0.305).

AI is where this track is heading, because it is a multi-channel distributional force that will test institutional configurations hard in the coming decades. It reshapes labor markets through cognitive-task displacement, absorbs grid capacity through the data-center buildout and passes the cost to households through utility rate regulation, and exposes economies to mineral and critical-gas dependencies through supply chains they do not control. These channels often land on the same households. The explanatory variable of interest is not the technology; it is the welfare state, labor-market regulation, and energy-pricing structure of the society absorbing the shock.

### [Institutional Configurations and the Social Politics of AI](/projects/typology-paper/)

A two-dimensional typology of 29 OECD countries along AI task-profile and labor-market dualization axes, formalizing the institutional argument into testable cross-level hypotheses. V1 sets the theoretical structure and an aggregate mapping; v2, in preparation, integrates OECD Risks that Matter microdata for individual-level tests of the regime × exposure interaction.

### [Redistribution Preferences and Institutional Trust Across Europe](/projects/ess-analysis/)

Redistribution preferences drift gradually under inequality shocks; in agent-based simulations calibrated from the model coefficients, institutional trust tips through a self-reinforcing feedback loop. If AI-driven disruption is a structural shock, the political crisis may not be a fight over who gets what; it may be a legitimacy collapse.

### [2020-2024 County-Level Partisan Swing](/projects/election-swing/)

A state-level ICC of 0.305 puts roughly a third of county-level swing variance at the state level. The null cross-level interaction (education × state unemployment, *p* = 0.48) narrows the search space instead of confirming the hypothesis.

### [Income Inequality and Redistribution Preferences](/projects/public-attitudes/)

The small neighborhood-level ICC (3.4%) was itself the finding; it pushed the question toward what scale contextual effects actually operate at, and the cross-national extension answered it: country-level institutions explain more than neighborhoods do.

## Where this is heading

Both tracks have live work. On the measurement side, the DICES audit is a template I can point at other safety taxonomies and evaluation rubrics, where the same base-rate and discriminant-validity problems are likely to recur. On the political-economy side, v2 of the typology paper moves from aggregate mapping to individual-level estimation on OECD Risks that Matter microdata, and a synthesis paper on welfare-state response to AI-related distributional pressure is in development.

The political-economy portfolio shows that institutional context moderates how distributional shocks translate into political outcomes; it does not yet identify a causal mechanism linking specific AI exposure to specific institutional drift. The measurement work shows that one widely used safety taxonomy cannot be calibrated at full rater power; it does not claim every evaluation instrument fails the same way. Testing both is the work ahead.

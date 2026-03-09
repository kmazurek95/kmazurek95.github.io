---
title: "About"
layout: "single"
type: "page"
---

<div class="about-intro">

I'm a computational social scientist based in Chicago. I have an MSc in Social Science Research from the University of Amsterdam and a BA in International Studies and Economics from Macalester College. I study how the environments people live in shape their political behavior, and I do it with NLP pipelines, multilevel models, and a lot of messy data.

</div>

## How I got here

I came to research through an unusual path. After graduating from Macalester in 2018 with a concentration in Middle East Studies and a minor in Economics, I moved to Nablus in the West Bank to teach at a bilingual school. I spent two years there, teaching 26 classes a week in humanities and English, developing conversational Arabic, and learning what it means to live inside the political dynamics I had previously only studied in classrooms. That experience shaped how I think about context -- not as an abstract variable in a regression model, but as the thing that determines what questions are worth asking in the first place.

When I came back and started my research master's at UvA, I brought that orientation with me. My coursework in Advanced Multivariate Modelling, Measurement Models, Big Data and Automated Content Analysis, and Experimentation in the Social Sciences gave me the quantitative toolkit. My thesis gave me the chance to apply it to something genuinely difficult: measuring interest group prominence in congressional floor speeches. That meant building a pipeline from scratch -- 78,000 documents from the GovInfo API, a coding scheme I designed and iteratively refined, a supervised classifier that I pushed from F1 0.79 to 0.91, and multilevel regression models that identified what actually drives prominence across policy domains and partisan contexts. The thesis earned an 8.0/10, and I rebuilt the entire pipeline after graduating because I knew the methodology could be pushed further.

## The work I do now

Since finishing my master's, I've been working at the intersection of AI evaluation and applied research. At Meta (through Tundra Technical Solutions), I evaluate AI-generated responses across their LLM product suite -- 450+ items weekly, maintaining a 95/100 quality score. The work requires applying structured evaluation criteria to edge cases that don't fit neatly into existing categories: misinformation, AI-generated "evidence" images, culturally sensitive content. I've contributed to standardizing evaluation guidelines, improving inter-rater reliability across a team of 15, and documenting the kinds of systematic model failure patterns that inform training data priorities.

Before Meta, I spent over a year doing AI evaluation and benchmark work across multiple platforms. At Snorkel AI, I wrote 150 graduate-level social science benchmark questions designed to expose gaps in model reasoning, with a roughly 90% acceptance rate, and reviewed over 1,000 peer-authored questions for rubric alignment and difficulty calibration. At Character.AI, I built economics tutoring dialogues and learned that technical accuracy without pedagogical grounding produces content that teaches nobody anything -- I researched real student misconception patterns and redesigned my process, pushing approval rates from about 60% to over 95%. At Mercor and RWS Group, I designed scoring rubrics, failure taxonomies, and quality criteria for content evaluation.

Before all of that, I spent three and a half years at BallotReady building political datasets across 20+ states and thousands of jurisdictions. Elections, redistricting, officeholder records -- from structured state databases to Excel files on county websites that hadn't been updated since the last cycle. I wrote ETL pipelines, ran validation checks, called county clerks to resolve discrepancies, and delivered analysis-ready datasets under campaign-cycle deadlines. I also built a validation script after catching my own data error that reduced the team's error rate from 8% to under 2% and became part of standard onboarding.

## What connects everything

The through line is measurement. Whether I'm operationalizing "interest group prominence" from legislative text, designing a rubric to evaluate LLM outputs, or merging five data sources on FIPS codes to model county-level partisan swing, the core challenge is the same: how do you reliably capture something that resists easy quantification? My published article ["What Political Science Can Teach AI Evaluation"](https://www.linkedin.com/in/kaleb-mazurek/) makes this connection explicit -- the construct validity, inter-rater reliability, and sampling bias challenges in AI evaluation are the same problems social scientists have studied for decades.

The other through line is context. Every research project I've built asks some version of the same question: how do contextual environments shape individual political outcomes? My thesis asked it about the legislative information environment. My neighborhood analysis asked it about local inequality. My county-level election model asked it about state political environments. The method is always multilevel -- individuals nested in contexts -- because that's the statistical architecture the question demands.

## What I'm working on now

I'm currently building a simulation extension to my cross-national redistribution analysis, parameterized by European Social Survey data, exploring how inequality shocks might shift redistribution attitudes across different welfare regime types. This is for a PhD application to the [ROOTS research group](https://www.uva.nl/) at the University of Amsterdam, which studies attitude-mediated social tipping dynamics. I'm also developing a fourth portfolio project studying how AI industry lobbying has reshaped congressional floor speech, extending my thesis pipeline to the 117th-119th Congresses and integrating Anthropic Economic Index occupation-level exposure scores.

## Education

**MSc Social Science Research** (Empirical-Analytical Methods), University of Amsterdam, 2021-2023. GPA: 7.96/10. Thesis grade: 8.0/10. Advisor: Dr. Joost Berkhout. Key coursework: Advanced Multivariate Modelling (8.6), Measurement Models in Quantitative Research (8.4), Big Data and Automated Content Analysis I & II, Fixed and Random Effects, Experimentation in the Social Sciences, Using R for Data Wrangling/Analysis/Visualization (8.5).

**BA International Studies and Economics**, cum laude, Macalester College, 2014-2018. GPA: 3.68. Concentration in Middle East Studies. Minor in Economics. Study abroad: SIT Migration & Transnational Identity (Rabat, Morocco); University of Chicago Summer Language Institute (Arabic). Honors thesis: "Kissingerism and Iranian-American Relations" (Advisor: Dr. Ahmed Samatar). Key coursework: Introduction to Econometrics, Intermediate Microeconomics, International Economics, Comparative Economic Systems, Statistical Modeling.

## Technical skills

**Methods:** Multilevel/mixed-effects modeling, NLP and text classification (SVM, TF-IDF, logistic regression), measurement design and construct validation, survey analysis, supervised machine learning, ETL pipeline development, reproducible research design.

**Languages & Tools:** Python (pandas, scikit-learn, statsmodels, NLTK, spaCy), R (lme4, tidyverse, Shiny, targets), SQL, Git, GitHub Actions, Streamlit, LaTeX.

**Data sources:** U.S. Census/ACS API, GovInfo API, Congress.gov, MEDSL election data, European Social Survey, CBS StatLine, state and county election databases.

**Languages:** English (native), Arabic (conversational -- three years of study plus two years living in the West Bank).

## How to read my portfolio

Not every project matters equally for every role. [The full breakdown is here](/research-program/), but the short version:

If you're hiring for **US political research** -- think tanks, policy shops, campaign analytics -- the [election project](/projects/election-swing/) is the entry point. ICC decomposition, Hispanic share findings, policy brief, US data infrastructure. The thesis and public attitudes project prove depth, but the election analysis is the one that shows I can work with your data.

If you're hiring for a **PhD program** in computational social science, the projects form a research program, not a collection. Neighborhood effects are small (ICC = 3.4%), cross-national effects are larger (ICC = 7.7%), and the election model puts 31% of swing variance at the state level. That scale question -- where do contextual effects actually live? -- is the thread. [Read the full research program narrative](/research-program/).

If you're hiring for **AI evaluation or safety**, the [bridging document](/posts/political-science-ai-evaluation/) is the lead. It repositions my Meta experience from annotation to evaluation methodology. The portfolio projects are evidence that I understand construct validity because I've actually had to operationalize hard-to-measure concepts.

If you're hiring for a **general research position**, lead with the methods: large-scale text classification (78K documents, F1=0.91), multilevel modeling across 3,100 units, cross-level interactions in hierarchical data. The domain follows; the methods are the headline.

## What I believe about research

Research questions beat technical demonstrations. A benchmark is a tool. A model of county-level swing is a contribution.

Finished beats ambitious. An unfinished project with a promising README is worse than nothing.

Honest null findings show maturity. The education-by-unemployment interaction wasn't significant (p=0.416). The neighborhood ICC was 3.4%. I report what the data says.

Each project should open a new door. The thesis proves NLP. Public attitudes proves multilevel modeling. The election project proves US data competence. The bridging document proves cross-domain thinking. Don't build two projects for the same audience.

## Contact

kalebmazurek@gmail.com · [GitHub](https://github.com/kmazurek95) · [LinkedIn](https://www.linkedin.com/in/kaleb-mazurek/)

---
title: "Research Program"
layout: "single"
type: "page"
---

<div class="about-intro">

I study how political behavior is shaped by the contexts people live in, and I do it computationally, at scale, with methodological rigor that transfers across domains.

</div>

## The thread connecting every project

Every project I've built asks a version of the same question: how do contextual environments shape individual political outcomes? The method is always multilevel -- individuals nested in contexts, units nested in groups, observations nested in structures. The data changes. The domain changes. The core analytical logic doesn't.

This is not "I know Python and R." This is not "I can classify text." The story is: I think about politics as a multi-scale problem, and I have the computational tools to study it that way.

## What each project proves

**[Interest Group Prominence in Congressional Speech](/projects/thesis-pipeline/)** is the technical foundation. The question -- how prominent are interest groups in congressional floor speeches -- is about how organized interests shape the informational environment of legislative debate. It proves I can formulate a measurement problem, build a classifier that works (F1 from 0.79 to 0.91), validate it with inter-rater reliability (kappa = 0.82), and produce interpretable results across 78,000 documents. For AI evaluation audiences, the measurement design thinking -- construct validity, annotation reliability, threshold optimization -- is the exact skillset that distinguishes senior evaluation roles from junior ones.

**[Income Inequality and Redistribution Preferences](/projects/public-attitudes/)** is the methodological bridge. People in unequal neighborhoods do think differently about redistribution, even controlling for their own income. But the effect is small at the neighborhood level (ICC = 3.4%), which itself was the interesting finding -- it pushed me to ask what scale contextual effects actually operate at. The cross-national extension using European Social Survey data found larger effects at the country level (ICC = 7.7%, significant income-by-Gini interaction), pointing toward institutional rather than local context. That scale question is what connects this project to everything that came after.

**[2020-2024 County-Level Partisan Swing](/projects/election-swing/)** is the US credibility project. 31% of swing variance sitting at the state level means state-level context -- media markets, campaign investment, governor effects, policy environment -- explains nearly a third of why counties swung differently. That's the same analytical logic as the neighborhoods project, applied to a domain US employers immediately recognize. The Hispanic share finding speaks to the most-debated dynamic of the 2024 cycle. And the null cross-level interaction (education by state unemployment, p = 0.416) is an honest finding: the variation exists but its source is an open question. Reviewers respect researchers who follow the data.

**["What Political Science Can Teach AI Evaluation"](/posts/political-science-ai-evaluation/)** is the thought leadership piece. It repositions my Meta evaluation experience from "I labeled AI outputs" to "I understand evaluation methodology at a conceptual level and can draw on a richer intellectual tradition than most people in this space." The five parallels -- measurement validity, construct validity, inter-rater reliability, sampling bias, applied frameworks -- connect my political science training to the AI evaluation industry in a way most people in either field haven't articulated.

## How each project opens a different door

The thesis proves NLP and text classification. The public attitudes project proves multilevel modeling depth. The election project proves US political data competence. The bridging document proves I can think across domains. Each one fills a gap the others don't.

This is deliberate. Building two projects that serve the same audience dilutes the portfolio. Every project should ask and answer a research question -- not just showcase a tool -- and every project should extend the reach of what came before.

## What's next

The next project extends my thesis pipeline to the 117th-119th Congresses, studying how AI industry lobbying has reshaped congressional floor speech. 774 organizations lobbied on AI in 2025, up 423% from 2020, and nobody has done computational text analysis of how that shows up in floor speeches. It reuses the same pipeline infrastructure (same tools, new questions -- how real research programs develop) and fills the one remaining strategic gap: no project studying AI itself.

In parallel, I'm building a simulation extension to the ESS redistribution analysis -- an agent-based model parameterized by regression coefficients, exploring whether inequality shocks cause redistribution attitudes to tip or stay stable across different welfare regime types. This bridges the gap between my empirical work and the mechanistic modeling questions at the core of tipping dynamics research in computational social science.

---

## Reading my work by audience

Not every project matters equally for every audience. Here's how the portfolio is designed to work for different readers.

### US political research (think tanks, policy shops, campaign analytics)

Lead with the [election project](/projects/election-swing/). The ICC finding, the Hispanic share result, and the policy brief are the things that make someone at Catalist or the Cook Political Report or Data for Progress say "this person can work with our data, ask our questions, and produce findings we'd publish or brief to clients." The [thesis](/projects/thesis-pipeline/) proves NLP capability at scale. The [public attitudes project](/projects/public-attitudes/) proves multilevel modeling depth. The bridging document and Meta experience are footnotes for this audience -- useful if they come up, but not the lead.

### PhD programs (computational social science)

Lead with the research program, not the individual projects. The [public attitudes project](/projects/public-attitudes/) and the ESS simulation together tell the micro-stability/macro-tipping story: neighborhood effects are small, but cross-national effects are larger, which is itself a finding about where contextual effects live. The [thesis](/projects/thesis-pipeline/) proves I can do original empirical research. The [election project](/projects/election-swing/) proves methodological range and honest null findings. The framing-and-escalation project (when built) becomes Phase 1 of a larger research vision. What PhD committees hear: "This person has a research program, not just a collection of projects. They think about questions that build on each other, and they can execute computationally."

### AI evaluation and safety roles

Lead with the [bridging document](/posts/political-science-ai-evaluation/). It establishes me as someone who thinks about evaluation at a systems level -- not just someone who follows rubrics but someone who understands why measurement is hard. My Meta experience gets reframed as evaluation work (quality metrics, systematic failure pattern identification), not annotation. The portfolio projects are evidence of analytical depth: "this person understands construct validity because they've actually had to operationalize hard-to-measure concepts." What hiring managers hear: "This person can design rubrics, not just follow them."

### General research positions (university labs, industry research teams)

Lead with the methods, not the domain. The thesis becomes "large-scale text classification (78K documents, F1=0.91)." The election project becomes "multilevel modeling of geographic variation across 3,100 units nested in 50 groups." The public attitudes project becomes "cross-level interactions in hierarchical data." The domain details follow, but the methods are the headline. What they hear: "This person has real methodological range -- text analysis, multilevel modeling, measurement design -- and can apply it to whatever domain we work in."

---

## Principles

These aren't abstract. They come from building things and learning what actually matters.

**Research questions beat technical demonstrations.** Every project asks and answers a question, not just showcases a tool. A benchmark is a tool. A model of county-level swing is a research contribution. PhD committees and research teams notice the difference immediately.

**Finished beats ambitious.** An unfinished project on GitHub with a promising README and half-built code is worse than nothing. Each project in this portfolio is complete, documented, and reproducible before the next one begins.

**Honest null findings show maturity.** The cross-level interaction in the election project wasn't significant (p=0.416). The neighborhood ICC in the Dutch project was only 3.4%. I report these because I follow the data rather than torturing it into significance. Reviewers respect that.

**Each project opens a new door.** The thesis proves NLP. The public attitudes project proves multilevel modeling. The election project proves US data competence. The bridging document proves cross-domain thinking. Don't build two projects that serve the same audience.

**"Phase 1 of a larger program."** This is how real researchers talk about their work. Nobody finishes their entire research agenda in one project. Showing you can think in research programs rather than isolated projects is itself a signal of research maturity.

**Presentation problem, not skills problem.** Every project in this portfolio demonstrates substantial capability. The priority is documenting and showcasing what's already been built, not chasing new credentials. Making existing work visible and legible to the right audiences is the work.

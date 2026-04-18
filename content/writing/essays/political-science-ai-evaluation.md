---
title: "What Political Science Can Teach AI Evaluation"
date: 2026-03-05
type: "Essay"
originally_published_url: "https://www.linkedin.com/in/kaleb-mazurek/"
originally_published_date: "2026-03-06"
originally_published_venue: "LinkedIn"
summary: "Measurement validity, inter-rater reliability, construct validity, sampling design: the methodological discipline the social sciences have built for a century applies directly to how AI evaluation pipelines should be designed. What the field needs is more measurement thinkers."
tags: ["AI Evaluation", "Quant"]
weight: 6
---

*Originally published on [LinkedIn](https://www.linkedin.com/in/kaleb-mazurek/), March 6, 2026. The full version lives here; the site is the canonical home.*

---

I have spent the last several years studying political speech and AI-generated text, and the same methodological problems keep showing up. Whether you are training a model or evaluating one, the labeling decisions matter more than the model itself. How you define your construct, how you operationalize it into coding criteria, how you check whether your labels are consistent, these choices determine whether your pipeline produces signal or noise.

Measurement validity. Inter-rater reliability. Construct validity. Sampling design. They are the reason some evaluation pipelines produce reliable training signal and others produce noise. The social sciences have been measuring complicated human judgments reliably for a century. AI evaluation is the latest context in which those methods apply.

## When "Helpful" Doesn't Mean Anything: Measurement Validity

In survey research, you never just ask a question. You validate that your question actually captures what you intend it to measure.

Consider a classic problem from political science: measuring "political ideology." A naive approach asks respondents whether they are liberal or conservative. Except those labels mean completely different things to a college student in Massachusetts and a farmer in Oklahoma. A validated approach uses a battery of specific policy position questions, on healthcare, taxation, immigration, tested against actual voting behavior. The vague question gives you noise. The validated battery gives you signal.

AI evaluation has the same problem. "Rate this response's helpfulness from 1 to 5" is the equivalent of "Are you liberal or conservative?" It feels like a measurement, but it captures something different for every annotator who reads it. What does helpful mean? Accurate? Thorough? Concise? The answer changes depending on who is reading, what the prompt was, and what they had for lunch.

The fix is the same one survey researchers use: break the vague thing into pieces you can actually observe. Does the response answer the question that was actually asked? Is the information verifiable? Is the level of detail appropriate to the query? Does it avoid introducing new problems? Each of those is measurable. "Helpful" is not.

I learned this on my thesis. My construct was "interest group prominence," whether a politician was treating an organization as a credible voice worth substantive discussion, or just mentioning it in passing. That sounds like a judgment call until you operationalize it. I defined a mention as prominent if the politician adopted the group's views, cited the group as having a significant role in a policy area, used the group as a resource to convey an argument, or explicitly conveyed the group's importance. A mention was passing if it was a brief reference, a list inclusion, or a procedural citation. Each of those is observable. "Prominence" by itself is not.

I built an SVM classifier to make this distinction across 78,000 documents and achieved an F1 of 0.79. It was a standard support vector machine with TF-IDF features. The performance came from the measurement design: clear definitions, specific criteria, and labeled training data built around those criteria rather than around intuition.

Anthropic's work on Constitutional AI reflects a similar instinct. When they set out to train Claude to be "harmless," they did not hand annotators a vague rubric. They broke harmlessness into dozens of specific, evaluable principles, drawn from the UN Declaration of Human Rights, DeepMind's Sparrow Rules, and their own research. And when early models trained on those principles started producing responses that were excessively preachy and moralizing, they did not blame the model. They revised the principles, adding criteria like "choose the assistant response that demonstrates more ethical and moral awareness without sounding excessively condescending, reactive, obnoxious, or condemnatory." That is iterative rubric development. In political science, we call it codebook revision.

## A Related Problem Worth Naming: Construct Validity

Even when your rubric is clear and well-defined, you can still be measuring the wrong thing. Checking whether an AI response cites sources does not measure factual accuracy. It measures citation behavior. Those are not the same construct. In AI evaluation, optimizing for easy-to-measure proxies instead of the actual thing you care about is one of the most common failure modes, and one of the hardest to catch, because your metrics look great the whole time.

## Fix the Rubric, Not the Raters: Inter-Rater Reliability

In political science, you are expected to demonstrate inter-rater reliability before your coded data is considered publishable. The conventional threshold is Cohen's Kappa above 0.70: two or more coders classify the same material independently, and if they do not agree at that threshold, the data does not move forward. Low agreement is almost never a problem with the coders. It is a problem with the codebook. If trained people disagree about how to classify something, the classification scheme is ambiguous and needs revision.

AI annotation has largely not adopted this discipline. Guidelines get written, annotators get trained (sometimes), and production labeling begins. When disagreements surface, they are typically resolved case by case. A senior annotator makes a judgment call, everyone moves on. The underlying pattern that caused the disagreement never gets addressed. Model evaluation tasks are inherently more subjective than dataset annotation, and yet they receive less measurement discipline, not more.

I will be honest: my own thesis used a single annotator for the labeled training data. I know firsthand what that limitation looks like and what it costs you. When you are the only person labeling, you do not discover the ambiguities in your own coding scheme because you resolve them unconsciously, the same way every time. You get consistency without reliability. Your classifier learns your idiosyncrasies, not the construct. The thesis produced real findings, but if I were designing it again, the first thing I would add is a second coder and a formal agreement protocol before any labels went into the training pipeline. It is the difference between a result you can defend and one you have to hedge.

My professional evaluation work operates differently, and the contrast is instructive. When I encounter a pattern of ambiguous cases, I do not just resolve them and move on. I document the pattern, identify what the guidelines do not cover, and develop a decision framework for the category. This is the same logic political science codebook development follows: low agreement is diagnostic information about your instrument. You fix the instrument, then re-measure.

The annotation teams that will produce the best RLHF training signal are the ones that treat low agreement as a rubric problem, not a people problem.

## Your Training Data Is a Sample: Sampling and Representativeness

Decades of polling disasters have taught political scientists one lesson above all others: how you sample determines what you learn. A survey of people who answer their phones is not a survey of the population. A survey of likely voters is not a survey of all voters. Every sampling decision is a choice about whose reality counts.

AI training data has the same problem, and the field is only starting to grapple with it. A model trained on preference data that over-represents Reddit discussions learns to write like a confident 27-year-old tech worker. It looks great on benchmarks. Then you deploy it to a mental health support context and the training distribution mismatch becomes immediately obvious, to everyone except the evaluation metrics. When your evaluation set over-represents straightforward factual queries, your model aces the test and fails the job.

My thesis processed all 78,000 congressional documents in the corpus, but the classifier that powered the analysis was trained on about 1,200 hand-labeled examples drawn in batches. The pipeline's limitations document is blunt about this: the training sample was not stratified by party, issue area, or time period. It was a practical decision made under resource constraints, and it is exactly the kind of decision that polling methodology would flag. If certain types of congressional speech, highly technical committee testimony, late-night floor speeches with unusual rhetorical styles, were underrepresented in the training data, the classifier would systematically miscode them, and the downstream multilevel models would inherit that bias. That still bothers me. It is the kind of limitation you can name but not fully quantify, and it makes you less confident in the results than the numbers alone would suggest.

The social science instinct here is that you name your sampling limitations explicitly, reason about what they might distort, and design your analysis to be transparent about where the results are strong and where they are provisional. Most AI evaluation pipelines do not do this. The training data gets collected, the model gets trained, and when limitations are documented at all, it is typically in a model card published after training, not built into the evaluation design from the start, where it would actually change what gets collected.

What population am I trying to generalize to? Which content types are overrepresented? Which are missing? Am I testing on the distribution I actually care about, or the distribution I happened to collect? Anyone designing an AI evaluation pipeline should be asking these questions. Pollsters learned the hard way what happens when you don't.

## The Field Needs Measurement Thinkers

What AI evaluation needs right now is not more people who can prompt. It is more people who think carefully about what they are measuring, whether they are measuring it well, and what happens when they get it wrong. Those are measurement questions. The social sciences have answers. That is the intersection I work from.

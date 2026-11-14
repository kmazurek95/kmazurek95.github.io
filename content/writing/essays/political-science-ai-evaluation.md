---
title: "What Political Science Can Teach AI Evaluation"
date: 2026-03-05
type: "Essay"
originally_published_url: "https://www.linkedin.com/in/kaleb-mazurek-46a011b6/"
originally_published_date: "2026-03-06"
originally_published_venue: "LinkedIn"
summary: "Measurement validity, construct validity, inter-rater reliability and sampling are long-established concepts in the social sciences. How they look from a political science perspective, drawing on my own thesis work, and why LLM labeling and evaluation need more measurement-focused thinking."
tags: ["AI Evaluation", "Quant"]
weight: 6
---

*Originally published on [LinkedIn](https://www.linkedin.com/in/kaleb-mazurek-46a011b6/), March 6, 2026; revised November 2026. The site is the canonical home.*

---

Over the past few years, I've read a lot of literature on both political speech and LLMs. A number of recurring issues arise in each, particularly around how you go about generating labels - whether that's for training or evaluation purposes. Questions of what you're measuring, how you translate that into a set of criteria, and how you ensure reliable labeling are central to any data pipeline.

They underpin whether you'll generate useful labels for training / evaluating a model. Measurement validity, inter-rater reliability, validity of the construct being measured, sampling considerations etc. These are long-established concepts in the social sciences. A growing body of AI research has started applying them to model evaluation (e.g., Wallach et al., 2025; Bean et al., 2025). What follows is how they look from a political science perspective, drawing on my own work.

## If "Helpful" isn't Helpful - Measurement Validity

As in survey methodology, it's important to ensure that your measurement tool(s) capture the concept you're seeking to measure.

Political scientists are often interested in measuring respondents' ideology. One simple measure is to ask them to self-identify as liberal/conservative. However, this is problematic, as "liberal" and "conservative" will be interpreted very differently across individuals. A better approach is to ask respondents about their positions on a range of policies and check the resulting measure against their self-reported vote choice. The policy battery provides a more valid measure of ideology, while self-identification alone is likely to yield misleading results.

Analogously, when we ask raters to evaluate the "helpfulness" of a model output, we run into a similar issue. There is no objective definition of "helpful," so each rater will bring their own interpretation to the task. "Helpful" could mean many things - e.g., factually accurate, detailed, succinct, free of additional errors... etc. As such, "helpfulness" is difficult to measure directly.

Instead, we can decompose "helpfulness" into its component parts, and assess each of those. For example, does the response address the user's query? Are the facts presented correct? Does it provide sufficient detail? Does it introduce any extraneous errors? These are each measurable quantities, whereas "helpfulness" is not.

This is something I encountered when writing my thesis, where I sought to measure whether politicians mentioned interest groups prominently in their speeches. "Prominent" vs. "non-prominent" mention of an interest group may initially appear to be a subjective judgment, but can be translated into a series of criteria, which I adapted from Fraussen et al. (2018): Did the politician espouse the interest group's position? Refer to the group as playing a key role in the topic at hand? Leverage the group as a means to communicate a point? Explicitly communicate the salience of the group? If none of these, the mention was non-prominent (e.g., a short mention, or a mention in reference to a procedural matter). A mention also couldn't count as prominent if ten or more other groups were named in the same sentence. These criteria enabled me to train a classifier to label roughly 24,000 mentions as prominent or non-prominent, drawn from about 78,000 Congressional Record documents.

Anthropic similarly developed a set of detailed criteria for "harmlessness" when training Claude via Constitutional AI, in a constitution published in 2023 (since replaced by a new version in January 2026). A model, not human raters, applied these principles when choosing between candidate responses. They sourced these from a variety of documents (the UN Declaration of Human Rights, DeepMind's Sparrow Rules, their own early research), and iterated on the rubric when they observed undesirable behaviors emerging in the model. For example, when the model became judgmental, they added a principle asking it to choose the response that "demonstrates more ethical and moral awareness without sounding excessively condescending, reactive, obnoxious, or condemnatory."

A corollary to this is ensuring that you are measuring the desired construct - i.e., construct validity. For example, measuring whether a model output contains citations is not a proxy for factuality. It may be tempting to rely on easily measurable proxies in place of the target construct, but this is likely to lead to misleading conclusions.

## Ensuring Reliable Labeling - Inter-Rater Reliability

A further requirement of political science research is to demonstrate that your labels are reliable. Typically, this takes the form of calculating an agreement statistic, such as Cohen's kappa for two raters or Krippendorff's alpha for two or more, and ensuring it exceeds a conventional threshold (Krippendorff recommends 0.80, with 0.667 as the floor for tentative conclusions). If it falls below this, the codebook is usually the first suspect: it is likely insufficiently prescriptive, and should be updated. Very rare categories can also drag these statistics down even when raters mostly agree, so a low score is a prompt to investigate rather than an automatic verdict.

Some LLM work does report agreement: the InstructGPT paper reported that its training labelers agreed with each other 72.6% of the time, and its held-out labelers 77.3% (Ouyang et al., 2022), although as raw percentage agreement rather than a chance-corrected statistic. But in my experience of LLM labeling/evaluation work, agreement is rarely used as a gate before labeling begins. Once guidelines are drafted and raters trained (if at all), labeling commences. Disagreements are resolved ad-hoc, with the assumption that a more experienced rater can adjudicate. Of course, given the higher degree of subjectivity inherent to model evaluation tasks, it is reasonable to expect greater variability in raters' judgments, but this should necessitate greater rigor in the labeling process, not less.

I note that in my thesis, I labeled the training data myself, and recognize that this introduces a limitation to my methodology. However, I am keenly aware of the issues this creates, and would certainly include additional raters and calculate inter-rater reliability if I were to repeat the study.

In my day-to-day work, when I identify a cluster of edge cases that fall outside our existing guidelines, I flag the pattern and help document criteria to guide future raters. Again, this mirrors the process of refining a codebook in political science to improve inter-rater reliability.

Ultimately, where a task has a defensible right answer, we want to maximize the number of raters who arrive at the same conclusion for any given input, and the way to achieve that is by improving the quality of the guidelines/rubric. Where raters disagree because they bring different but legitimate perspectives, as in many safety judgments, that disagreement is information worth keeping rather than noise to remove (Google's DICES dataset was built around this idea).

## Sampling Considerations

Polling is riddled with examples of poorly executed sampling leading to erroneous conclusions. Phone surveys fail to reach those who don't own/answer to a phone; likely-voter models can misjudge who will actually turn out; etc.

Similar issues are beginning to emerge in the context of LLMs. Preference data derived from a single platform such as Reddit will reflect the style/tone of that platform's users. Models trained on such data may perform well on evaluations that share this skew, and underperform on other domains (e.g., mental health counseling). If your evaluation data is skewed toward simple QA-style prompts, you will find that your model performs well on that evaluation, but may struggle to generalize beyond it.

In my thesis, the classifier labeled roughly 24,000 interest-group mentions across about 78,000 Congressional Record documents, but it was trained on a random sample of 1,000 mentions that I hand-coded. Random draws avoid systematic bias on average, but with a sample this size and no stratification, some groups (by party, policy topic, or year) may have been thinly covered. The thesis didn't address this, and it's a limitation I've reflected on since: if the classifier made more errors on those groups, those errors would carry through to my subsequent modeling.

If I were to repeat the study, I would stratify the sample and explicitly discuss the representativeness of my training data and its potential impact on the results. I don't believe this consideration is currently given enough weight in LLM training/evaluation workflows.

Some key questions to consider when assembling a training/evaluation dataset include: What population do I wish to generalize to? What characteristics are over-/under-represented in my sample? Does my evaluation data reflect the intended population of interest?

## Conclusion

There is a need for more measurement-focused thinking in LLM evaluation. We need to be thinking about what we are measuring, how we are measuring it, and the consequences of poor measurement. The social sciences have much to offer in this regard.

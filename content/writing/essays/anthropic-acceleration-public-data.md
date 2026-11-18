---
title: "Anthropic's Acceleration: What the Public Data Show"
date: 2026-11-18
type: "Essay"
description: "METR estimates Anthropic’s models are improving about 2x faster than before October 2025. On Epoch AI’s public index, Anthropic’s frontier rose about 1.45x faster."
image: "/images/anthropic-acceleration/note_fig1_anthropic_frontier.png"
repo: "https://github.com/kmazurek95/anthropic-acceleration-public-data"
tags: ["AI Evaluation", "Quant"]
---

*METR's overall judgment is that, as of October 2026, Anthropic is likely improving its models' capabilities on well-specified tasks at roughly 2x the pre-October 2025 rate. The best public proxy is the series of fourteen Anthropic model releases on Epoch AI's capability index. I refit those, assigned an uncertainty range, and repeated the exercise for all other developers with a sufficient number of releases. This is an attempt to establish what can be said from public data alone. On Epoch's public index, Anthropic's frontier rose about 1.45x faster after October 2025 than before (90% interval 1.27x to 1.69x, median 1.46x, over draws from my refit of Epoch's current model, covering score uncertainty only), while the frontier across all developers shows roughly no acceleration (0.93x). At the break, Anthropic was 3.6 points behind the frontier; by June 2026 it led it again.*

METR's report of 5 November 2026 provides an independent estimate of the extent to which AI is accelerating AI development at Anthropic. Its summary states: "As of October 2026, Anthropic is likely improving the capabilities of their models on well-specified tasks at around twice the rate they did between March 2024 and October 2025" (METR, 2026). Its estimate from benchmark scores is 1.9x, with a 95% CI of 1.5x-2.8x. METR holds its overall conclusion with high uncertainty: it would not be surprised by a true figure closer to 1.3x or 3x. AI Futures Project cited the report as the largest factor in its update to its AI timelines on 10 November 2026 (AI Futures Project, 2026).

The estimate matters beyond the report. According to METR, "Anthropic lists AI R&D acceleration as a key risk indicator in its Responsible Scaling Policy" (although METR notes that its assessment pays no special attention to the RSP's thresholds). Forecasters are using the estimate to update their AI timelines. I want to understand what can be said about it from public data.

METR analyzes an index of model capabilities (AECI), calibrated on the benchmark scores of all models using the methodology and code of Epoch AI, and estimates the trend on Anthropic's models only. It then fits one line to the AECI series, with two segments joined at an October 2025 breakpoint (the same form as Figure 1 below). The index rises at 15 points per year before 7 October 2025 and 29 points per year after, according to the labels on METR's main AECI chart. Its estimated acceleration is the ratio of those slopes.

METR used Anthropic-internal data, including benchmark scores of unreleased models, and Anthropic held redaction rights over the report's non-public information. I therefore do not seek to interrogate the 1.9x estimate. Instead, I consider a narrower question: Epoch publishes its own index of released model capabilities. What does that public record suggest, and with what confidence?

Several others have already done this. METR's report includes a comparison of its analysis to Epoch's published index (as of 30 October 2026) and finds that the acceleration is 1.59x-1.62x for Anthropic's public models and 0.99x across all public models. Karthik Tadepalli wrote on 7 November that Epoch's published scores give a 1.42x acceleration for Anthropic, or 1.64x using Epoch's prior fitting method (Tadepalli, 2026). He also reports 95% intervals for both figures, 1.24x-1.66x and 1.37x-1.99x. Julian Bradshaw estimated \~1.45x in a comment on the LessWrong linkpost of METR's report on 5 November. On 10 November, commenting on the AI Futures post, he gave 1.24x for Anthropic models and 0.90x for all frontier models. I could not reproduce his 0.90x. I find similar results to these, with some variation due to differences in how the frontier is built, which matters most of the factors I checked, and in the Epoch data snapshot, date range and release dates used. I run the same analysis, with uncertainty ranges, for other developers, and explore the result's sensitivity to the breakpoint. These analyses do not test METR's estimate, which relies on private data. They clarify what can be inferred from public data.

## Estimates of the acceleration

There are at least 7 estimates of the acceleration associated with the METR report, as summarized below. They are different because they reflect different choices of model, date of model and fitting methodology.

- 1.9x: METR estimate using Anthropic's index, including unreleased models, dated by internal release
- 1.71x-1.74x: METR estimate using Anthropic's index, released models only, dated by public or internal release
- 1.59x-1.70x: using Epoch's public index, with the fitting method Epoch used until 4 November 2026 (1.59x-1.62x in METR's report, which states only that Epoch's index was downloaded on 30 October, so placed here by inference from Epoch's changelog date, for which Tadepalli gives a different date; 1.64x in Tadepalli's refit; 1.70x here)
- 1.24x-1.45x: using Epoch's public index as published (1.42x from Tadepalli; \~1.45x and later 1.24x from Bradshaw; 1.45x here)
- 1.4x: METR estimate using Anthropic's index, pooling all frontier developers, including Anthropic's unreleased models, dated by internal release
- \~1x: pooling all developers using Epoch's public index (0.99x in METR's report; 0.90x from Bradshaw; 0.93x here)
- 1.1x-2.9x: METR's estimate using the same data but varying one modeling assumption (the link function)

Each row differs from the others on one or more of the set of models used, their release dates, the construction of the index and the fitting method. The lower estimates are not "corrections" to the higher ones. I focus on those that can be replicated from public data. METR's comparison grid also reports versions calibrated on Anthropic models only, which lower the AECI estimates (1.41x-1.59x) and raise the Epoch ECI estimates (1.84x-1.87x). METR's other robustness checks, all with the break fixed at 7 October 2025, move its estimate much less than the link function does: 1.9x-2.2x across model snapshots, 1.9x-2.2x across benchmark sets, 1.9x when benchmarks are dropped once models score above 85%, and 1.9x-2.1x across regularization settings. METR attributes the difference between its estimate and Epoch's index mainly to fitting the trend to Anthropic models only and to including models used only inside Anthropic; Epoch's change of fitting method came after METR downloaded Epoch's data (on Epoch's dates), so it is a further factor that this note adds.

## Fourteen points

Epoch's data (archived 13 November 2026), as loaded by Epoch's code, covers 256 models across 57 benchmarks. Anthropic released 14 models between March 2024 and 31 October 2026 that outperformed all prior Anthropic models; the window matches METR's own periods, a baseline from March 2024 and an assessment "as of October 2026", and the extension to 13 November is reported separately as a sensitivity check. Six were released before 7 October 2025 and eight after. I use record-setting releases because the question is how fast Anthropic's best available model improves, and a running maximum taken at every Anthropic release or daily gives similar results (1.47x and 1.49x). Fitting all Anthropic releases, records or not, gives 1.08x (17.2 to 18.7 points a year), but that answers a different question: it also includes releases that did not set a record, and these go from 1 before the break to 5 after (7 and 13 releases in all, against 6 and 8 records). Record-setting releases also came about twice as often after the break (6 in the roughly 19 months from March 2024 to the break, 8 in the roughly 13 months after), and a line through records can steepen when they come more often even if the underlying pace has not changed; I have not tested how much this contributes. (Claude 3 Opus is dated 1 day before my date range begins; including it gives 15 points, which has a negligible effect on the published scores (1.45x to 1.46x) but raises the estimate on the prior method from 1.70x to 1.75x.)

I fit two linear segments to these points, with a breakpoint on 7 October 2025, following METR. Using Epoch's current published scores, the rate of increase of Anthropic's frontier was 14.3 points/year prior to the breakpoint and 20.8 points/year after, for an acceleration of 1.45x. Using the prior Epoch fitting method applied to the same benchmark scores, the rates were 13.2 and 22.4 points/year, for an acceleration of 1.70x.

![Line chart of Anthropic's record-setting releases on Epoch's Capabilities Index, with two fitted segments joined at 7 October 2025: 14.3 to 20.8 points a year on the published scores (solid) and 13.2 to 22.4 on Epoch's prior method (dashed).](/images/anthropic-acceleration/note_fig1_anthropic_frontier.png)

Figure 1. Anthropic frontier releases plotted on Epoch's Capabilities Index, March 2024 - October 2026. All points correspond to Anthropic releases with a higher score than all previous Anthropic releases. The fitted line consists of two straight segments joined at 7 October 2025. Using the published scores (solid line, closed circles), the slope rises from 14.3 to 20.8 points/year, a 1.45x change. Using the scores from Epoch's previous fitting procedure (dashed line, open circles), the slope rises from 13.2 to 22.4 points/year, a 1.70x change.

Excluding any one model gives an acceleration of between 1.40x and 1.56x using the published scores. One choice at the edges of the window moves the estimate more than that. Building the frontier only from models inside the window, as in Bradshaw's 1.14x chart, lowers it to 1.13x, because Claude 3 Opus falls one day outside and the lower-scoring Claude 3 Haiku becomes the first point. Extending the window to 13 November 2026, which adds Claude Fable 5.2, raises it to 1.54x on the published scores, which is still inside that range, and 1.84x on the prior method (median 1.55x over draws from the current model, 90% interval 1.35x-1.80x).

## Confidence in the estimate of 1.45x

Epoch's index is itself an estimate of model capabilities, based on the observed benchmark scores of models on a varying set of benchmarks, and a statistical model that maps those scores to a common scale. From 4 November 2026, this model is a Bayesian model that estimates a posterior distribution of model scores, whereas previously it produced a point estimate, with bootstrap resamples for uncertainty (Epoch AI, 2026).

There is precedent in political science for modeling an index of this kind. Treier and Jackman (2008) model democracy as a latent variable, measured by the Polity indicators, and demonstrate that the resulting measurement error is substantial and can affect downstream analyses that use Polity as a covariate.

An estimate of acceleration is one such downstream analysis. I refit Epoch's current model using Epoch's public code (this refit gives 1.47x, against 1.45x on the published scores), took 4,000 joint draws from the posterior of the model scores, rebuilt the Anthropic frontier in each draw, and refit the two linear segments. The median estimate of acceleration is 1.46x, with a 90% interval of 1.27x-1.69x.

![Histogram of Anthropic's slope ratio across 4,000 draws, centred near 1.46, with the 90% range from 1.27 to 1.69 shaded and dashed lines at 1.45 (published scores) and 1.70 (prior method).](/images/anthropic-acceleration/note_fig2_ratio_draws.png)

Figure 2. Distribution of Anthropic's ratio of slopes (after to before 7 October 2025) across 4,000 draws from the posterior of my refit of Epoch's current model (using Epoch's public code), where the frontier is recomputed and refit for each draw. The median is 1.46x, with the 90% interval spanning 1.27x-1.69x (gray shading). The ratios using the published scores (1.45x) and Epoch's previous fitting procedure (1.70x) are marked with dashed lines.

This interval reflects uncertainty in the model scores only. It assumes the model release dates, breakpoint and two-segment specification are fixed.

It also serves to contextualize the difference between Epoch's current and prior fitting methods. The estimate of 1.70x using the prior method is just above the upper bound of the 90% interval from the current method. The two methods differ by at most 1.6 points for frontier models, over a range of the index of \~126-169 points, and this is sufficient to shift the estimate of acceleration by \~0.25. There is no single model that accounts for the difference, although Claude Opus 4.5 accounts for \~1/3 of it.

METR's report includes a CI that accounts for uncertainty in the model scores. METR does not state which of Epoch's methods was used to construct the AECI, but it very likely used the prior method. Tadepalli infers this from METR's robustness checks on L2 regularization, which belongs to the least-squares fit. Tadepalli dates Epoch's switch to the Bayesian fit to late September 2026, but Epoch's changelog gives 4 November, and I follow Epoch. His inference is also consistent with the use of a bootstrap procedure to estimate the CI in METR's report (resampling benchmark scores within each model), which is also how uncertainty is estimated in Epoch's prior method. If so, this suggests that the estimates are sensitive to the fitting method, although this does not indicate which is more appropriate.

## Relative to what?

AI Futures notes that there is little acceleration across all models and that "Acceleration is limited to Anthropic", whose models were previously further behind and have recently been catching up. It adds that preliminary numbers from a different METR team, without access to Anthropic's private data, show much less of a speed-up on an ECI-like measure. It says this makes it discount the possibility of acceleration "a little bit", but "mostly we still trust" the METR team that worked inside Anthropic. The catch-up is also flagged in METR's report, which offers the reading that "Anthropic models were subfrontier in 2025, so Anthropic's historical progress up to 2025 was understated", in which case the pooled estimate of 1.4x would be more accurate. It also offers the opposite reading: if Anthropic's models are less optimized for benchmarks than others, the 1.4x is understated and the 1.9x is closer to accurate. I can put public numbers on this.

An estimate of acceleration relative to a developer's own prior progress cannot distinguish between an acceleration specific to that developer and an acceleration of the frontier more broadly. I therefore fit the same two-segment model to all developers with 4+ frontier releases before and after the breakpoint.

Using the published scores, I estimate an acceleration of 1.45x for Anthropic, 0.89x for OpenAI, 0.84x for DeepSeek, 0.78x for Alibaba and 0.57x for Google DeepMind. Pooling all developers gives 0.93x. Propagating uncertainty in the model scores gives a median estimate of 1.46x (90% interval 1.27x-1.69x) for Anthropic and 1.01x (0.84x-1.21x) for all developers, using Epoch's current model. Using the prior model, the median estimates are 1.69x (1.37x-2.17x) and 1.03x (0.80x-1.36x), respectively. Anthropic's ratio is above 1 in all draws from the current model, and in all draws from the prior model in which Anthropic has enough releases on each side of the breakpoint to fit (99.6% of draws), and above the all-developer ratio in \~99% of draws. Compared developer by developer, it has the highest ratio among eligible developers in 52.7% of draws from the current model and 27.2% from the prior model, almost entirely because of Meta AI. Meta AI is a notable exception, but this rests on few releases: on the published scores it has 3 frontier releases before the breakpoint and 5 after, so it enters the comparison only in draws that give it a 4th earlier release. In \~46% of draws from the current model, it has a 4th release prior to the breakpoint and an estimated acceleration greater than Anthropic's. OpenAI's ratio is above 1 in \~1/3 of draws from the current model, and slightly more than 1/2 of draws from the prior model.

![Dot-and-range chart of each developer's slope ratio at 7 October 2025 under Epoch's current and prior methods. Meta AI and Anthropic sit above 1, all developers together sit near 1, and OpenAI, Alibaba, DeepSeek, Google DeepMind and xAI sit at or below 1.](/images/anthropic-acceleration/note_fig3_developers.png)

Figure 3. The factor by which each developer's frontier slope changes after 7 October 2025 relative to before. Median and 90% range across 4,000 samples from my refit of Epoch's current model (filled circles) and 500 samples from the previous procedure (open circles). Numbers show the count of frontier points before and after 7 October 2025 in the published scores. Developers are omitted from a sample if there are fewer than 4 frontier release dates on either side of 7 October 2025 (so Meta AI and xAI are present in only some samples). The vertical dotted line is at 1x.

This is consistent with no change in the pace of the frontier as a whole around the breakpoint (a ratio of \~1), with Anthropic's ratio above this in almost all draws. That agrees in direction, though not in size, with METR's comparison, in which pooling all frontier developers gives 1.4x against 1.9x for Anthropic's models, but it is purely descriptive and does not establish that the acceleration was specific to Anthropic or identify any cause.

It does, however, quantify the catch-up noted by METR, AI Futures and Bradshaw. Anthropic's frontier was increasing by 14.3 points/year prior to the breakpoint, compared to 17.4 points/year for the frontier. Anthropic held the frontier from March to early April 2024 and again from 20 June to 11 September 2024, and was at its maximum distance from the frontier in December 2024, \~7.7 points behind. It had closed this gap to \~3.6 points (90% interval 1.9-5.8) by the breakpoint. It continued to increase at 20.8 points/year after the breakpoint, compared to 16.2 points/year for the frontier, and regained the frontier on 9 June 2026, \~21 months after losing it. It held the frontier until 2 September 2026, and lost it to GPT-6 Astra, dated 3 September.

Thus, using public data, Anthropic fell behind the frontier in 2024, began to close the gap prior to the breakpoint and regained the frontier in June 2026. Relative to the prior rate of progress of the frontier, its pace after the breakpoint was 1.2x (median 1.25x across draws from the current model; 90% interval 1.11x-1.43x). This is a different comparison to the 1.45x estimate above, and is not intended to be a correction to it.

This does not preclude that the acceleration is due to AI-driven improvements in research. However, if the rate of progress prior to the breakpoint was low, the estimated acceleration will be higher than it would be if the prior rate was higher. METR notes a narrower version of this: its estimate may be an overestimate if Anthropic's historical rate of progress was below its normal rate because of temporary factors, which it ties to Anthropic trailing the frontier. The trajectory of the gap between Anthropic and the frontier provides a record of this fall and recovery, but cannot be used to attribute any portion of the acceleration to it.

Using the prior Epoch fitting method, the acceleration of OpenAI is estimated at 1.14x, and Meta AI at 2.89x (based on a small number of releases).

## Breakpoint vs step

METR estimated the breakpoint on the Anthropic index. On public data, the precise breakpoint has little effect on the results. Estimating the acceleration with a breakpoint at the start of each month from June 2025 to June 2026 gives an acceleration of between 1.44x and 1.61x.

The choice of model form is more consequential. A two-segment model allows a change in the rate of progress, in either direction, whereas a step model assumes that the rate of progress is unchanged but there was a one-off increase in capabilities. This distinction is important for forecasting, since after a lasting change of slope the gap from the earlier trend grows in a straight line over time, whereas after a step it stays fixed.

Fixing the breakpoint at 7 October 2025, a breakpoint model is a substantially better fit to the data than a step on that date, using either Epoch model and in >99% of draws.

However, if the breakpoint/step date is allowed to vary, the best-fitting step occurs at the end of May 2026, between Claude Opus 4.8 and Claude Fable 5, and corresponds to a step of 3.6 points. This is marginally preferred to the best breakpoint model using the published scores, but not across draws of the model scores (46% of draws from the current model and 27% from the prior model). Extending the window to 13 November 2026, which adds Claude Fable 5.2, reverses this: with both dates free, the change of slope then fits better on the published scores (sum of squared residuals 20.65 against 22.41 for the step), on my refit with the current method and on the prior method, and the step wins in 32% of draws from the current model and 8% from the prior model, down from 46% and 27%.

![Two panels of the same fourteen points. Left: the best change of slope, on 8 September 2025, from 14.0 to 20.5 points a year. Right: the best step, at the end of May 2026, of 3.6 points on a constant 15.8 points a year.](/images/anthropic-acceleration/note_fig4_slope_vs_step.png)

Figure 4. Fitting either a change of slope or a step, both allowed to occur on any date, to the published scores (same 14 points as Figure 1). Left: the optimal date for a change of slope is 8 September 2025, with the rate of change increasing from 14.0 to 20.5 points/year (1.46x, sum of squares of residuals = 15.9). Right: the optimal date for a step is late May 2026, with a rate of change of 15.8 points/year and step size of 3.6 points (sum of squares of residuals = 14.0). Any date between 29 May and 9 June 2026 gives the same fit.

This question is also discussed in METR's report in the context of the private data, using a different test. It notes that Anthropic's prior system cards posited a step change in capabilities at Mythos Preview, and it prefers a lasting change of slope. In my fits to the public data to 31 October 2026 with both dates free, the step fits better on the published scores (sum of squared residuals 13.96 against 15.94) and on my refit with the current method, whereas the change of slope fits better on the prior method (19.05 against 21.19) and in most draws (54% from the current model, 73% from the prior model). With the date fixed in advance, then, the change of slope wins clearly, but with both dates free the answer turns on a single release, Claude Fable 5.2, so the public data do not yet settle which shape fits better; further releases should.

## The "fast year"

The Forecasting Research Institute defines a "fast year" as a 12-month period in which the frontier of Epoch's index increases by 30+ points (\~2x the recent rate of progress). It reports that the maximum increase to 3 November 2026 was 21 points, and notes that its analysis does not fully account for the change in Epoch's methodology (Kučinskas and Rosenberg, 2026).

For windows beginning in 2024 or later, the maximum 12-month increase is 20.9 points using the prior Epoch method, and 22.0 points using the current published scores. This occurs between 11 December 2024 and 11 December 2025 in both cases. No 12-month window meets the threshold of 30 points under either method.

Note that there is a 23.8 point 12-month increase in the published scores in earlier years (ending in March 2024), but this relies on scores at the lower end of the index where the difference between the two methods is greatest, and on the fact that Epoch's data loader excludes models released prior to 2023.

## Limitations

- This does not assess the validity of METR's estimate of 1.9x, which is based on Anthropic's index and includes unreleased models.
- It is descriptive. It is based on 14 data points, and I do not perform any formal test of the breakpoint. The 90% interval reflects uncertainty in the model scores only. All estimates assume that a point on the index corresponds to a constant change in capabilities across the range of the index, which is not established by the data. METR's analysis of the link function (which varies its estimate from 1.1x to 2.9x) shows a related sensitivity.
- It is based on a single snapshot of Epoch's data (13 November 2026), and the scores will change as further benchmarks are added.
- It does not identify the cause of the acceleration, if any. METR's guess that \~80% of the current (October 2026) acceleration is due to AI (it expects a lower share of the cumulative acceleration since October 2025) rests largely on evidence I cannot see.
- It does not estimate researcher productivity growth. The ratio of index slopes, the self-reported speed-up (\~12x, which METR calls "only very loose evidence") and output per researcher are different quantities.

## Implications and further work

If using the estimate of acceleration, be clear about which estimate is being used. Based on public data, a two-segment fit with METR's break date to Anthropic's record-setting releases gives \~1.5x after October 2025 relative to the prior rate using Epoch's current scores (1.27x-1.69x, an interval covering score uncertainty only), or \~1.7x using the prior method (1.37x-2.17x). These figures also depend on where the window opens and closes: on the published scores the estimate runs from 1.13x to 1.54x across the two edge choices described above. None of this confirms or contradicts METR's estimate of 1.9x, which is based on private data.

If using it to update forecasts, be aware of the assumptions. With the date fixed in advance, the public data clearly favor a change of slope over a one-off step change in capabilities, but with both dates free the answer turns on a single release, so the public data do not settle it yet. Extrapolating the acceleration assumes a change of slope, and also that the higher slope persists, which is a further assumption.

If comparing across developers, the ratio for the frontier as a whole is \~1, which means no change of pace. On public data, this is consistent with Anthropic falling behind the frontier and subsequently recovering, but does not identify any cause.

If conducting a future independent assessment, it would be useful to (i) estimate the acceleration for each developer separately, and (ii) vary the breakpoint.

There are several aspects of METR's analysis that I would like to see clarified, none of which would materially affect the conclusions above:

- The version of Epoch's methodology and data used to construct the AECI. This would allow a more direct comparison with the estimates above.
- Whether the breakpoint was re-estimated within each bootstrap resample. This would clarify which sources of uncertainty the CI captures.
- Estimates of acceleration for each developer separately. METR's report includes an estimate pooling all developers, but it would be informative to see the developer-specific estimates.
- Sensitivity of the estimate to the breakpoint. This would include an estimate with a step model and free breakpoint.

METR's report already includes many useful details, such as the sensitivity to the link function, the method of breakpoint estimation, the sources of uncertainty in the CI and the comparison of breakpoint vs step models. The above would provide further context to the headline estimate.

## Data and code

- Data: Epoch AI benchmark data, as archived on 13 November 2026 by the Wayback Machine (capture 20261113150458; SHA-256 beginning b07bd2eb). Scores fit with Epoch's public code at commit e04929ab.
- Code and every number in this note: [https://github.com/kmazurek95/anthropic-acceleration-public-data](https://github.com/kmazurek95/anthropic-acceleration-public-data)

## References

- AI Futures Project (2026). Q3.5 Timelines Update: Looks Like the Intelligence Explosion Will Happen in 2027 After All. 10 November. [Post](https://blog.aifutures.org/p/q35-timelines-update-looks-like-the).
- Bradshaw, J. (2026). Comments on LessWrong: on METR's report, 5 November ([comment](https://www.lesswrong.com/posts/N5AmYkRks5CqAxvBg/metr-independent-assessment-of-ai-r-and-d-acceleration-at?commentId=yMEbwPhDEnmdKanFs), [reply](https://www.lesswrong.com/posts/N5AmYkRks5CqAxvBg/metr-independent-assessment-of-ai-r-and-d-acceleration-at?commentId=gnjHFaKPCmpK2DWBG)); on the AI Futures post, 10 November ([comment](https://www.lesswrong.com/posts/f9PajMLmBYzmWzyDv/q3-5-timelines-update-looks-like-the-intelligence-explosion?commentId=BpAefiykFJ5u9tgrB), [reply](https://www.lesswrong.com/posts/f9PajMLmBYzmWzyDv/q3-5-timelines-update-looks-like-the-intelligence-explosion?commentId=odDYyyBmbjrsmdzsG)).
- Epoch AI (2026). Epoch Capabilities Index: code ([eci-public](https://github.com/epoch-research/eci-public), [commit e04929ab](https://github.com/epoch-research/eci-public/commit/e04929ab)), [changelog entry of 4 November 2026](https://epoch.ai/data/eci-documentation/changelog), and [methodology report](https://epoch.ai/publications/eci-bayesian-methodology).
- Kučinskas, S., and Rosenberg, J. (2026). How Close Is Recursive Self-Improvement? Forecasting Research Institute, 10 November. [Post](https://forecastingresearch.substack.com/p/how-close-is-recursive-self-improvement).
- METR (2026). Independent Assessment of AI R&D Acceleration at Anthropic in October 2026. 5 November. [Report](https://metr.org/blog/2026-11-05-anthropic-ai-rd-acceleration-assessment/).
- Tadepalli, K. (2026). Anthropic's AI acceleration is probably real. 7 November. [Blog](https://blog.karthiktadepalli.com/p/metr-anthropic-report).
- Treier, S., and Jackman, S. (2008). Democracy as a Latent Variable. American Journal of Political Science 52(1), 201-217. [Record](https://ideas.repec.org/a/wly/amposc/v52y2008i1p201-217.html).

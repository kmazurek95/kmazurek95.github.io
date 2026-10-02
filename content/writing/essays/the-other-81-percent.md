---
title: "The Other 81 Percent"
date: 2026-10-02
type: "Essay"
description: "OpenAI’s benchmark for economically valuable work covers about a fifth of US employment. The paper doesn’t say so. It should, and every benchmark like it should."
summary: "GDPval's 44 occupations cover 19.2% of US wage and salary jobs, and they sit high on the pay scale. The paper doesn't report either number. A benchmark that claims economic relevance should."
originally_published_url: "https://kmazurek95.substack.com/p/the-other-81-percent"
originally_published_date: "2026-10-02"
originally_published_venue: "The Missing Variable (Substack)"
canonical_url: "https://kmazurek95.substack.com/p/the-other-81-percent"
image: "/images/gdpval/coverage_thumbnail.png"
repo: "https://github.com/kmazurek95/benchmark-exposure-skew"
tags: ["AI Evaluation", "Quant"]
weight: 1
---

*Originally published on [The Missing Variable](https://kmazurek95.substack.com/p/the-other-81-percent), October 2, 2026. The site version adds one figure, the random-draw baseline.*

---

*OpenAI’s benchmark for economically valuable work covers about a fifth of US employment. The paper doesn’t say so. It should, and every benchmark like it should.*

![Bar chart: GDPval's 44 occupations account for 19.2% of US wage and salary jobs, 29.7 million of 154.2 million. The other 80.8%, about 124.5 million jobs, are not covered.](/images/gdpval/coverage_thumbnail.png)

Estimates of GDPval’s coverage of the US economy vary by measure. OpenAI’s paper claims that GDPval covers “the majority” of work activities for its 44 occupations (Patwardhan et al., 2025). A study comparing 43 agent benchmarks, including GDPval, reports 47.8% coverage (Wang et al., 2026). A Stanford paper arguing for more comprehensive, lower-cost evaluations puts it at 5% of US occupations (Wan et al., 2026). I put it at 19.2%.

Each of these numbers is defensible. Each answers a different question, and only one counts workers.

![Four bars, each against its own whole: 63% of O\*NET's 41 work activities, 47.8% of a work-category map, 4.3% of 1,016 occupations, and 19.2% of US wage and salary jobs. Only the last counts people.](/images/gdpval/four_denominators.png)

“The majority” refers to the depth of coverage within occupations. GDPval sourced its tasks to cover most of the work activities that O\*NET, the federal occupational database, has on file for each of its 44 occupations (Patwardhan et al., 2025). GDPval has 1,320 tasks, but OpenAI released only 220 of them, five per occupation, and its paper reports these statistics for that public set. O\*NET scores every occupation on the same 41 broad “generalized work activities,” and the public set covers 26 of them, or 63%. The public set covers only 208 of the 1,470 task statements O\*NET lists for these occupations, or 14%. The point of the claim is how thoroughly GDPval’s authors sampled the occupations they chose. It says nothing about the occupations they didn’t choose.

47.8% refers to the breadth of coverage across work categories. Wang et al. (2026) took 43 agent benchmarks and placed them on a work-category map built from O\*NET data. They then looked at how much of the map each benchmark covered. GDPval tied for the highest coverage, at 47.8%, a category count that ignores how many people work in each.

5% refers to the breadth of coverage across occupations. Wan et al. (2026) state that GDPval covers “5% of US occupations” when describing their new benchmark suite, EconEvals. GDPval has 44 of the roughly 1,000 occupations in the O\*NET database they use, a little under 5%. Like the previous number, it ignores how many people work in each. General and Operations Managers is one of the 44 occupations in GDPval and has 3.6 million workers. It is weighted the same as the smallest occupation that the US government tracks.

19.2% is the breadth of coverage weighted by number of workers. This is the percentage of US workers covered by the 44 occupations in GDPval. I couldn’t find this number anywhere else. It is also the only number that answers the question most people have when they see a headline about GDPval. How many American workers are in the jobs this score describes?

OpenAI does provide one aggregate number that goes the other way. They state that their 44 occupations “collectively earn $3T annually” (Patwardhan et al., 2025). This measures the wage bill, not the number of workers. I reproduced this number using my data, and it comes out to $2.99T using May 2024 wages. That is about 29% of all wages in the BLS data, earned by 19% of the workforce.

## How people read the headline

OpenAI released GDPval in September of 2025 to measure how well AI models can complete “real-world economically valuable tasks” (Patwardhan et al., 2025). They did extensive work to make this a strong benchmark. Industry experts with an average of 14 years of experience wrote the tasks, which span 44 occupations across nine sectors that each account for more than 5% of US GDP. Each task is based on a real-world work product such as “a legal brief, an engineering blueprint, a customer support conversation, or a nursing care plan” (OpenAI, 2025a). Expert graders compared unlabeled model work with human expert work. At release, the best model, Anthropic’s Claude Opus 4.1, matched or beat the expert 47.6% of the time.

OpenAI also said frontier models could complete these tasks “roughly 100x faster and 100x cheaper” than experts (OpenAI, 2025a). They noted that this only accounts for inference time and API cost, not the human review the work needs. OpenAI also looked at a scenario where an expert would look over the model’s output and complete the task if the model was not able to (Patwardhan et al., 2025). This reduced GPT-5 to 1.1x faster and 1.2x cheaper than the expert alone at release. As the model scores higher, this number will increase. This doesn’t tell us how likely companies are to use these models or how much it will cost to verify their work. That’s not what GDPval is trying to measure.

The scores have continued to rise. OpenAI reported a 74.1% win-or-tie rate for GPT-5.2 Pro in December 2025. In Epoch AI’s February review, it remained the highest score (Brand and Burnham, 2026). In March 2026, OpenAI announced that GPT-5.4 could match or beat the expert 83.0% of the time. In April, they reported a score of 84.9% for GPT-5.5. OpenAI’s GPT-5.6 post in July reports an outside version of the benchmark, graded by an AI judge on an Elo scale, and its later launch posts don’t report GDPval at all. So 84.9% is the latest figure of this kind.

These numbers get shared, often without context. TechCrunch reported on the release of GDPval with the headline “OpenAI says GPT-5 stacks up to humans in a wide range of jobs” (Zeff, 2025). The benchmark is named after GDP, which invites readers to assume it covers the whole economy.

The paper does not answer the question people ask when they see headlines like that. If a model is able to produce work that is equal to or better than a human 85% of the time, what share of American workers are in the jobs it measures?

## Measuring the frame

Survey research already has a term for this problem: coverage error. Every survey samples from a frame, the list of people or units it can actually reach. Coverage error comes from the gap between that frame and the population you want to describe. Survey methodologists list four sources of survey error and call them the “cornerstones” of survey research: coverage, sampling, nonresponse, and measurement (de Leeuw, Hox, and Dillman, 2008; Dillman, Smyth, and Christian, 2014). Survey standards treat coverage error as a core problem. You describe your frame and discuss who it excludes from your survey. People will take that into account when reading your results. A benchmark also has a frame. GDPval’s frame is its 44 occupations. What do those occupations cover? It is the first question to ask of anything that samples.

This is simple to answer because GDPval uses public federal data for its frame. OpenAI was transparent about how they chose their frame, which I appreciate. They chose all sectors that accounted for more than 5% of GDP (value added) in Q2 2024. Within each sector, they selected the top five predominantly digital occupations that contribute most to total wages and compensation. Retail Trade contributes only four, which is why the total is 44 rather than 45. An occupation was considered predominantly digital if GPT-4o classified at least 60% of its O\*NET tasks as digital. Tasks were weighted by importance, relevance, and frequency. These occupations were at the detailed occupation level from the Bureau of Labor Statistics (BLS) May 2024 Occupational Employment and Wage Statistics. So each of the 44 occupations can be mapped to a 2018 SOC code. I mapped each occupation to its SOC code and checked every code against the O\*NET-SOC database. Forty-three occupations map to a single code; the other, Buyers and Purchasing Agents, is a broad group, so I checked its three detailed codes. I then merged this with the May 2024 BLS occupational employment and wage estimates that GDPval used. As a sanity check, I calculated the mean wage across the economy using employment weights and got $67,909 compared to the BLS estimate of $67,920.

GDPval’s 44 occupations account for 29.7 million of the 154.2 million wage and salary jobs BLS counts in the US. That’s 19.2% of employment. If you take GDPval at face value and assume it measures how AI performs on jobs in general, you are assuming those 44 occupations represent the remaining 81% of employment (or ~124.5 million jobs).

The 19.2% of employment covered by GDPval also skews toward higher-wage occupations. The BLS provides wage estimates at the occupation level, so I’m comparing mean wages by occupation. When I weight by employment, the median worker in a GDPval occupation is at the 82nd percentile of wages. That’s an occupational mean wage of around $98,300, compared to $52,400 for the workforce as a whole on the same measure. Some of this is due to how occupations were selected. By selecting occupations that contribute most to total wages and compensation, you select higher-wage occupations. This is why I focus on the percentage of employment covered rather than wages.

![Dot plot of the employment-weighted median of occupational mean wages: $52,400 across all US wage and salary jobs, against $98,300 for jobs in GDPval's 44 occupations, which is the 82nd percentile.](/images/gdpval/wage_position.png)

GDPval didn’t pick occupations for their size, but a wage bill is employment times wage, so its rule still favors big occupations. Forty-four occupations picked at random from the 831 detailed occupations in the BLS data would cover about 5% of employment.

![Histogram of 200,000 random picks of 44 occupations, which cover about 5% of US wage and salary jobs on average. None reaches GDPval's 19.2%.](/images/gdpval/random_draw_baseline.png)

Another way to look at this is to only compare the 44 occupations to occupations whose primary sector is one of GDPval’s nine sectors. Even so, the frame covers only 31.1% of that population. It moves by only about 2 percentage points when I reassign occupations that sit near a sector boundary. My Government sector leaves out public schools, though, and counting them would lower it further. The median worker in an occupation covered by GDPval is still at the 73rd percentile of wages in those sectors. So it’s not just that GDPval has high GDP sectors compared to the rest of the economy. The occupation rule adds its own tilt.

## The exposure question, and a test stacked against me

This project started with a different question: does GDPval’s frame sit higher on measures of AI exposure than the average worker? If it did, part of the score would come from OpenAI’s chosen frame. While designing the test, I found that none of the exposure measures I could get was independent of the data GDPval used to pick its occupations, so coverage became the main result, and exposure became a secondary test.

I pre-registered my analysis before analyzing any exposure data. Here is why. Exposure is hard to measure, and it’s easy to see what you want to see. The AI Occupational Exposure index (AIOE) of Felten, Raj, and Seamans (2021) is one of the most popular academic exposure measures. It uses O\*NET ability scores. GDPval uses a digital filter based on O\*NET tasks. They both use O\*NET. If a frame chosen with an O\*NET filter scores high on an exposure measure that also uses O\*NET, I could be measuring actual exposure, or I could be measuring shared O\*NET data. So I decided ahead of time that if AIOE showed a skew, I would report it but could not claim it reflected real exposure. If I did not see a skew with AIOE, I would have strong evidence against my hypothesis because AIOE is the measure most likely to show one. In other words, the test could count against my hypothesis, but it could never confirm it.

There is a skew. GDPval’s frame has an employment-weighted median of +0.95 AIOE compared to the workforce median of +0.03. The median worker GDPval covers is at the 69th percentile of the national exposure distribution. Ignoring employment, GDPval’s occupations also rank higher on AIOE than the other 735 scored occupations. Pick one of each at random, and the GDPval occupation scores higher 73% of the time (rank test, p < 0.001). This is the scenario my pre-registration said I would not be able to interpret. GDPval’s frame was chosen using O\*NET, and it got a high score on a metric created using O\*NET. It could be that these occupations are more exposed, or it could be O\*NET talking to itself. I have no way of knowing. I planned to use another exposure measure as a robustness check. Webb’s (2020) exposure measure is based on patents. Unfortunately, this measure comes with 1990 census codes. The chain of public crosswalks I used to reach current codes leaves 45% of US employment without a score. Webb’s measure also uses O\*NET task descriptions to match against patents. Due to the 45% of employment left without a score and the overlap with O\*NET, we can’t use this as a check. I pre-registered that if the crosswalk lost too many occupations, I would not use it. So I didn’t.

Other papers have also found problems with exposure metrics. Individual exposure measures predict occupational unemployment risk poorly, though combining them explains another 18% of the variance (Frank, Ahn, and Moro, 2025). Exposure scores generated by LLMs can vary by up to 3.6x in mean exposure and have as little as 57% agreement, depending on the model used (Yin, Vu, and Persico, 2026). A recent review found that newer AI-specific exposure measures tend to rate higher-wage jobs as more exposed (del Rio-Chanona et al., 2025). That is where GDPval’s wage-bill rule selects its occupations from. So my finding is that the skew is there, but I can’t tell whether it reflects real exposure or shared O\*NET data.

## What benchmarks should report

This doesn’t mean GDPval is a bad benchmark. It includes real occupations and tasks that are graded thoughtfully. Having a benchmark that covers a subset of what you want to measure is fine. Epoch AI made the qualitative version of this point in February: benchmarks like GDPval are useful but “don’t live up to their names,” because there are “many more sources of GDP than captured by GDPval” (Brand and Burnham, 2026). What I can add is the number, which turns that point into something a benchmark can report.

Others have tried to quantify what benchmarks test. Wang et al. (2026) found that many agent benchmarks focus on programming tasks, while most human work and economic value happens elsewhere. Hua et al. (2026) suggest that benchmark creators name the work activities they test, using a list of 18 activities drawn from O\*NET, so results can be reported by activity across occupations. We should also count workers. Activity and occupation counts don’t account for how many people work in those occupations. Employment share does.

The ML community is already having this conversation around construct validity. Bean et al. (2025) had 29 expert reviewers go through 445 LLM benchmark papers. They found common flaws in how benchmarks are built and scored, flaws that weaken the claims drawn from them. Only 16% of the papers used statistical tests or uncertainty estimates when comparing models. Freiesleben and Zezulka (2025) argue that a benchmark score, on its own, at best measures performance on that dataset and learning problem, and that any broader claim needs stated assumptions.

Survey researchers have codified this. The American Association for Public Opinion Research asks survey creators to specify their sampling frame and “any segment of the target population that is not covered,” as well as how they calculated their weights (AAPOR, 2021). Without rules like these, even survey researchers skip this. A 2011 review of 117 self-administered survey studies in health research found that only 11% discussed sample representativeness. The authors concluded that there was “limited guidance and no consensus” on reporting for survey research (Bennett et al., 2011). There is no standard for benchmarks to report on the economic coverage of their tasks. I don’t believe they will start on their own.

I have one suggestion. A simple one at that. If you are creating a benchmark that you believe is economically relevant, please report two additional statistics with your score: the percentage of US employment that your frame covers, and where the median worker in your frame falls in the wage distribution. If your benchmark already uses a federal occupation classification like GDPval does, all you need is the national BLS file and a crosswalk to those codes. I have provided [my work](https://github.com/kmazurek95/benchmark-exposure-skew) here. For GDPval, those numbers are 19.2% and the 82nd percentile. I think it’s impressive that a model can score 85% on a fifth of our workforce, and many of those workers make good money. I’m not trying to take that away from anyone. But that’s not the same as scoring 85% on the US economy. Most people will assume it is if you don’t provide those two numbers.

## Sources

Patwardhan, T., Dias, R., Proehl, E., et al. (2025). [GDPval: Evaluating AI Model Performance on Real-World Economically Valuable Tasks](https://arxiv.org/abs/2510.04374). arXiv:2510.04374; ICLR 2026.

OpenAI (2025a, September 25). [Measuring the performance of our models on real-world tasks](https://openai.com/index/gdpval/).

OpenAI (2025b, December 11). [Introducing GPT-5.2](https://openai.com/index/introducing-gpt-5-2/).

OpenAI (2026, March 5). [Introducing GPT-5.4](https://openai.com/index/introducing-gpt-5-4/).

OpenAI (2026, April 23). [Introducing GPT-5.5](https://openai.com/index/introducing-gpt-5-5/).

OpenAI (2026, July 9). [GPT-5.6: Frontier intelligence that scales with your ambition](https://openai.com/index/gpt-5-6/).

Zeff, M. (2025, September 25). [OpenAI says GPT-5 stacks up to humans in a wide range of jobs](https://techcrunch.com/2025/09/25/openai-says-gpt-5-stacks-up-to-humans-in-a-wide-range-of-jobs). TechCrunch.

Brand, F., and Burnham, G. (2026, February 13). [What do “economic value” benchmarks tell us?](https://epoch.ai/publications/what-do-economic-value-benchmarks-tell-us) Epoch AI.

Wang, Z. Z., Vijayvargiya, S., Chen, A., et al. (2026). [How Well Does Agent Development Reflect Real-World Work?](https://arxiv.org/abs/2603.01203) arXiv:2603.01203.

Wan, A., Hatgis-Kessell, S., Aguirre, T., Liang, P., and Bommasani, R. (2026). [Economic Evaluations of Language Models](https://arxiv.org/abs/2607.19375). arXiv:2607.19375.

Hua, Y., Na, H., Ayubcha, C., and Lian, L. (2026). [Designing Benchmarks for Knowledge Work](https://arxiv.org/abs/2605.23262). arXiv:2605.23262.

Felten, E., Raj, M., and Seamans, R. (2021). [Occupational, industry, and geographic exposure to artificial intelligence: A novel dataset and its potential uses](https://doi.org/10.1002/smj.3286). Strategic Management Journal, 42(12), 2195-2217.

Webb, M. (2020). [The Impact of Artificial Intelligence on the Labor Market](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3482150). Working paper, SSRN 3482150.

Frank, M. R., Ahn, Y.-Y., and Moro, E. (2025). [AI exposure predicts unemployment risk: A new approach to technology-driven job loss](https://doi.org/10.1093/pnasnexus/pgaf107). PNAS Nexus, 4(4), pgaf107.

Yin, M., Vu, H., and Persico, C. (2026). [How (un)Stable Are LLM Occupational Exposure Scores? Evidence from Multi-Model Replication](https://doi.org/10.3386/w35110). NBER Working Paper 35110.

del Rio-Chanona, R. M., Ernst, E., Merola, R., Samaan, D., and Teutloff, O. (2025). [AI and jobs. A review of theory, estimates, and evidence](https://arxiv.org/abs/2509.15265). arXiv:2509.15265.

Bean, A. M., Kearns, R. O., Romanou, A., et al. (2025). [Measuring what Matters: Construct Validity in Large Language Model Benchmarks](https://arxiv.org/abs/2511.04703). NeurIPS 2025 Datasets and Benchmarks Track.

Freiesleben, T., and Zezulka, S. (2025). [The Benchmarking Epistemology: Construct Validity for Evaluating Machine Learning Models](https://arxiv.org/abs/2510.23191). arXiv:2510.23191.

Bennett, C., Khangura, S., Brehaut, J. C., Graham, I. D., Moher, D., Potter, B. K., and Grimshaw, J. M. (2011). [Reporting guidelines for survey research: An analysis of published guidance and reporting practices](https://doi.org/10.1371/journal.pmed.1001069). PLoS Medicine, 8(8), e1001069.

AAPOR (2021). [Transparency Initiative Disclosure Elements](https://aapor.org/wp-content/uploads/2023/01/TI-Attachment-C.pdf) (revised April 2021).

de Leeuw, E. D., Hox, J. J., and Dillman, D. A. (Eds.) (2008). International Handbook of Survey Methodology. Lawrence Erlbaum Associates. Chapter 1, “The cornerstones of survey research.”

Dillman, D. A., Smyth, J. D., and Christian, L. M. (2014). Internet, Phone, Mail, and Mixed-Mode Surveys: The Tailored Design Method (4th ed.). Wiley.

U.S. Bureau of Labor Statistics, [Occupational Employment and Wage Statistics](https://www.bls.gov/oes/tables.htm), May 2024 national estimates.

O\*NET-SOC 2019 taxonomy, [O\*NET Resource Center](https://www.onetcenter.org/taxonomy.html).

U.S. Bureau of Labor Statistics, [Standard Occupational Classification](https://www.bls.gov/soc/2018/home.htm), 2018 edition and crosswalks.

Full analysis, pre-registration and code: [github.com/kmazurek95/benchmark-exposure-skew](https://github.com/kmazurek95/benchmark-exposure-skew).

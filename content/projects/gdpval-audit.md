---
title: "A Sampling-Frame Audit of OpenAI's GDPval Benchmark"
type: "Benchmark Audit / AI Evaluation"
summary: "A pre-registered audit of what OpenAI's GDPval benchmark samples. Its 44 occupations cover 19.2% of US wage and salary jobs and sit high on the pay scale. The paper reports neither number."
date: 2026-10-02
weight: 1
home: "featured"
repo: "https://github.com/kmazurek95/benchmark-exposure-skew"
essay: "/writing/essays/the-other-81-percent/"
image: "/images/gdpval/coverage_thumbnail.png"
stats:
  - "44 occupations"
  - "19.2% of wage and salary jobs"
  - "Random baseline: about 5%"
  - "Pre-registered"
tags: ["AI-evaluation", "benchmarks", "coverage", "labor-markets", "pre-registration"]
---

## The Question

Every survey samples from a frame, the list of people or units it can actually reach. A benchmark also has a frame. GDPval, OpenAI's benchmark for "real-world economically valuable tasks" (Patwardhan et al., 2025), takes its frame from 44 occupations. OpenAI chose all sectors that accounted for more than 5% of GDP, then, within each sector, the predominantly digital occupations that contribute most to total wages and compensation.

The paper does not say what share of American workers are in those 44 occupations, or where they sit in the wage distribution. This audit measures both.

## What I Did

I mapped each occupation to its 2018 SOC code and checked every code against the O\*NET-SOC database. Forty-three occupations map to a single code; the other, Buyers and Purchasing Agents, is a broad group, so I checked its three detailed codes. I then merged this with the May 2024 BLS occupational employment and wage estimates that GDPval used. As a sanity check, the employment-weighted mean wage across the economy comes out to $67,909, against the BLS estimate of $67,920.

For a baseline, I drew 44 occupations at random from the 831 detailed occupations in the BLS data, 200,000 times. I also compared the frame against only the occupations whose primary sector is one of GDPval's nine.

The analysis was pre-registered before I analyzed any exposure data, including how I would read every possible result of the secondary exposure test.

## Findings

{{< finding label="The frame covers about a fifth of US jobs" >}}
GDPval's 44 occupations account for 29.7 million of the 154.2 million wage and salary jobs BLS counts in the US: **19.2%** of employment.
{{< /finding >}}

- **Against random occupations.** Forty-four occupations picked at random would cover about 5% of employment, and none of the 200,000 draws reaches 19.2%. GDPval didn't pick occupations for their size, but a wage bill is employment times wage, so its rule still favors big occupations. The draws are a descriptive baseline, not a hypothesis test.
- **Within GDPval's own sectors.** Against only the occupations whose primary sector is one of the nine, the frame covers 31.1% (random draws average 8.6%). Reassigning occupations near a sector boundary moves this by about 2 percentage points, and counting public schools in Government would lower it.
- **Wages.** Weighted by employment, the median GDPval job sits at the 82nd percentile of occupational mean wages: about $98,300, against $52,400 for all wage and salary jobs on the same measure. Part of this follows from the selection rule, since choosing occupations by wage bill picks higher-wage occupations. That is why coverage is the headline.
- **Exposure.** GDPval's frame scores higher on the AI Occupational Exposure index (AIOE), but the pre-registration said this result could not be read as real exposure: AIOE and GDPval's occupation filter both come from O\*NET. Webb's patent-based measure, planned as a check, leaves 45% of employment without a score after crosswalking, so by the pre-registered rule I didn't use it.

## Methodology Notes

The paper says its 44 occupations "collectively earn $3T annually." Using May 2024 wages I get $2.99T, about 29% of all wages in the BLS data, earned by 19% of the workforce. Every number on this page reproduces from the code in the repository.

The audit does not claim to have discovered GDPval's sampling rule; OpenAI documents it. It is descriptive: it shows what the frame contains and says nothing about what AI will do to jobs.

## Links

- [The Other 81 Percent](/writing/essays/the-other-81-percent/): the essay on these findings, also on [Substack](https://kmazurek95.substack.com/p/the-other-81-percent)
- [GitHub Repository](https://github.com/kmazurek95/benchmark-exposure-skew): the pipeline and its outputs
- [Findings](https://github.com/kmazurek95/benchmark-exposure-skew/blob/main/FINDINGS.md): results and their limits
- [Pre-registration](https://github.com/kmazurek95/benchmark-exposure-skew/blob/main/pre_registration.md): the claim, measures and decision rule, committed before the exposure analysis

Data: BLS Occupational Employment and Wage Statistics, May 2024; O\*NET-SOC 2019. Source paper: Patwardhan et al. (2025), "GDPval: Evaluating AI Model Performance on Real-World Economically Valuable Tasks," [arXiv:2510.04374](https://arxiv.org/abs/2510.04374).

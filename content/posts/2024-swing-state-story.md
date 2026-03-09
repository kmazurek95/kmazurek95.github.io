---
title: "31% of the 2024 Swing Was a State Story, Not a County Story"
date: 2026-03-09
summary: "Modeling 3,152 counties nested in 49 states reveals that nearly a third of the 2024 partisan swing variation lives at the state level. What that means for how we interpret the election."
tags: ["elections", "2024", "multilevel-modeling", "electoral-geography"]
type: "Research Note"
---

The dominant post-2024 narrative focuses on county-level demographics: Hispanic voters shifted right, college towns held, rural areas deepened. These are real patterns. But they miss a structural feature of the swing that only becomes visible with multilevel modeling.

## The ICC Finding

When I modeled the 2020-2024 two-party vote swing across 3,152 counties nested in 49 states, the intraclass correlation came back at 0.305. That means 30.5% of the variation in how much counties swung sits at the state level, not the county level.

Put differently: if you picked two counties from the same state, they would swing more similarly to each other than two random counties from different states. State-level forces -- media environments, campaign resource allocation, gubernatorial politics, state policy context -- explain nearly a third of the county-level story.

This does not make county demographics irrelevant. Hispanic population share was the single strongest predictor, and the education gradient remained significant everywhere. But it means that accounts focusing only on "who lives in this county" are missing a substantial chunk of the variance.

## Education Varies, But Why?

The education gradient -- counties with more college graduates swung less Republican -- is one of the most stable patterns in American elections. In this analysis, the random slope for college share was highly significant (likelihood ratio test p < 10^-16), meaning the strength of the education effect varies substantially across states.

The natural hypothesis is that state economic conditions mediate this: maybe education matters more in states where the economy is struggling. But the cross-level interaction between college share and state unemployment change was null (p = 0.48). Whatever is driving the state-by-state variation in education's effect, it is not state-level economic change.

This is an open question worth pursuing. Candidate explanations include state media market structure, differential campaign spending patterns, and variation in local party infrastructure. Each would require different data to test.

## What This Means for Analysis

Two implications for anyone analyzing the 2024 results:

First, state-level context matters more than most commentary acknowledges. When someone says "Hispanic voters shifted right," the follow-up question should be "in which states, and why does it differ?" The state-level ICC suggests these are not uniform national trends -- they are filtered through state-specific political environments.

Second, honest null findings are informative. The education-by-unemployment interaction did not reach significance. That is a finding, not a failure. It narrows the search space for what actually explains the state-level variation.

The full analysis, interactive dashboard, and policy brief are available in the [project repository](https://github.com/kmazurek95/us-election-county-swing).

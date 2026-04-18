---
title: "Six weeks of helium"
subtitle: "The semiconductor supply chain is running on a buffer that chemistry and shipping logistics cap at 45 days"
date: 2026-03-20
type: "Essay"
summary: "The Hormuz shock and the Ras Laffan shutdown have the chip industry operating on a helium buffer with a physical deadline. The Layer 2 supply chain constraints bind faster than the Layer 1 political economy constraints, and the political consequence is AI infrastructure consolidation."
tags: ["Geopolitics", "Policy", "Political Economy"]
weight: 3
---

On April 16, 2026, Fatih Birol, director of the International Energy Agency, told reporters that Europe has about six weeks of jet fuel remaining if the Strait of Hormuz stays closed (Fox News, April 16, 2026). The jet fuel figure is what made the headlines. It is not the only six-week number worth paying attention to.

The global semiconductor industry is operating, right now, on a helium buffer that chemistry and shipping logistics together cap at roughly 45 days (The Diplomat, April 2026). The buffer has been drawing down since Qatar's Ras Laffan Industrial City went offline on March 2. That shutdown removed roughly a third of global helium supply from the market. The strait that carries what remains has been effectively closed to Western commercial shipping since early March. As of today, Ras Laffan has not restarted. The shipping picture improved this morning when Iran declared Hormuz open for the remaining period of the ceasefire, but the statement is conditional, mines are believed to still be present in the channel, and a single announcement does not rebuild five weeks of lost shipments.

The chip industry's public statements do not reflect the chemistry of the situation. They should.

## The buffer

Helium is stored as a cryogenic liquid at minus 268.9 degrees Celsius, roughly three degrees above absolute zero. It is held in specialized containers engineered to minimize heat ingress, but no container is perfectly insulated. The liquid gradually boils off. Industry practice treats 35 to 48 days as the workable storage window for a given shipment before the loss rate eats meaningful value from the contents (Oregon Group, April 2026).

That 45-day figure is the binding physical constraint on the downstream supply chain. It is not an inventory policy. It is a cap on how long a fab can sit between deliveries before the product it paid for has literally evaporated.

Under normal routing, container transit from the Persian Gulf to South Korea takes approximately one month. Asian fabs had inventory from pre-crisis shipments through approximately early April 2026 (J2 Sourcing, April 2026). That window is closing in real time. Cape of Good Hope rerouting adds roughly 3,500 nautical miles per voyage and about $1 million in additional fuel cost per shipment, assuming Ras Laffan restarts tomorrow and the rerouted helium is flowing from the Gulf through the Southern Atlantic. Neither condition is currently met.

Samsung and SK Hynix, which together produce roughly two thirds of the world's memory chips, source nearly 65 percent of their helium from Qatar (Rare Earth Exchanges, March 2026). Taiwan, whose TSMC produces roughly 90 percent of the world's most advanced logic chips, sources 69 percent of its helium from Gulf Cooperation Council states. SK Hynix has stated that it has long secured diverse supply chains and sufficient inventory, and that there is almost no chance of impact (*The American Prospect*, April 2026). TSMC has said it does not currently anticipate a notable impact and is monitoring the situation.

Both statements are consistent with current production. Neither is consistent with eight weeks of continued disruption.

## The stack

Helium is not the only constraint tightening simultaneously.

South Korea sources approximately 90 percent of its bromine imports from Israel (Tom's Hardware, March 2026). Bromine is used in circuit formation. Israel is party to the ongoing conflict. China's 2025 gallium export controls were in place before the war began and remain in place. Gallium is a compounding constraint on advanced semiconductor manufacturing. TSMC's CoWoS advanced packaging capacity, which is the binding constraint on Nvidia Blackwell production, was fully sold out through mid-2026 before Ras Laffan went offline (The Diplomat, April 2026). Seagate and Western Digital have reported that their 2026 nearline hard drive production is fully allocated, with prices for high-capacity drives up 20 to 50 percent since mid-2025 (J2 Sourcing, April 2026). Ninety-five percent of Western Digital's 2026 high-capacity output is locked to enterprise and hyperscaler contracts. The remaining five percent is available to everyone else.

The semiconductor supply chain is not one binding constraint. It is a stack of them. Helium is the most acute because of the chemistry, but it is not solitary. Each constraint has a different resolution timeline. Bromine depends on the war. Gallium depends on trade diplomacy with China. CoWoS depends on TSMC's capital expenditure cycle, which is measured in years. High-capacity HDDs depend on helium, which closes the loop.

Semiconductor share of global helium consumption grew from roughly 6 percent in 2015 to an estimated 21 to 25 percent in 2025, driven by EUV lithography and AI-fueled demand for high-performance chips (Rare Earth Exchanges, March 2026). Forty-two new fabrication facilities are scheduled to come online by the end of 2026 under the CHIPS Act and equivalent programs worldwide. The demand curve in this sector does not accommodate a supply shock. It was already steep before the crisis.

## The extraction end

The acute phase has a slower companion. Primary helium development at Helium One's Rukwa concession in Tanzania, Pulsar Helium's Topaz project in Minnesota, and a handful of other sites is real but early-stage. Development timelines for these projects run years, not months. Even if every primary helium project currently announced were fast-tracked to production tomorrow, none of them would meaningfully offset the current shortfall (J2 Sourcing, April 2026).

This is the supply-chain sequencing problem that [earlier work in this series](/writing/essays/the-other-end-of-the-supply-chain/) examined from the extraction end. The communities around Kinambo village and Itumbula are inside a consultation process that the extractive industries literature suggests tends to produce worse outcomes the more compressed the timeline (Ash, 2024; Flemmer and Schilling-Vacaflor, 2016; Jerez et al., 2021). The current acute phase of the helium crisis is the mechanism by which that timeline gets compressed. Demand pressure at the fab level translates directly into urgency at the exploration license level. A shortage crisis in South Korea makes a Tanzanian mining authority less likely to insist on the deliberative pace that consultation actually requires.

The two ends of the supply chain are not separate stories. They are the same story at different time horizons.

## What binds first

A three-layer analytical framework helps here. Layer 1 is AI's material energy footprint and the distributional politics of electricity cost socialization. Layer 2 is the critical mineral and critical gas supply chains that AI hardware and renewable energy technologies share. Layer 3 is the vulnerability of data center physical infrastructure to kinetic attack. The sequencing question, under current conditions, is worth stating explicitly.

Layer 1's distributional dynamics transmit through electricity markets over quarters and years. Rate cases take time. Capacity auctions clear on multi-year cycles. Political backlash organizes at the pace of state legislative sessions. The mechanism is real and measurable, but its operation is slow.

Layer 2, as currently configured, transmits in weeks. The helium buffer runs 45 days. The bromine exposure is bounded by the ceasefire. The CoWoS bottleneck binds in the current production year. The HDD allocation clears in the current contract cycle. When Layer 2 constraints bind, they bind on specific fab production lines, on specific product roadmaps, on specific capital expenditure decisions that have already been announced to investors.

The implication for the AI buildout is straightforward. The constraint that may force the first real deceleration in data center capacity expansion is not the political backlash against electricity rates, though that is real and growing. It is the gas supply to the fabs that produce the accelerators the data centers run. Layer 2 binds first.

This is not a prediction that the AI buildout stops. The largest hyperscalers have enough inventory and enough capital to absorb substantial disruption. Their 2026 data center capital expenditure plans, in the range of $700 billion, have the balance sheet cushion to continue through extended supply chain shocks (*The American Prospect*, April 2026). It is, however, a prediction that the cost of continuing rises sharply, that smaller players and second-tier customers get rationed out, and that the consolidation of AI infrastructure into a handful of firms that can weather the supply stack accelerates.

That consolidation is also a distributional outcome. It is the other side of the political economy argument this work has been making. The concentrated returns that were visible to residential ratepayers as concentrated benefit from their shared grid costs are now also visible as concentrated capacity to absorb supply shocks that smaller enterprises cannot. The AI economy's winners are getting a second moat, funded by the same structural conditions that produced the first.

The clock on the fab is not in the public conversation. It should be. Six weeks of helium is a number that deserves the same attention as six weeks of jet fuel.

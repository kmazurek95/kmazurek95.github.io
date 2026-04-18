# The price of being a target

On April 1, 2026, Iranian missiles struck Batelco headquarters in Hamala, Bahrain. Batelco is Bahrain's largest telecommunications company. Its Hamala complex is also the physical colocation site for Amazon Web Services' ME-SOUTH-1 region, the AWS cloud infrastructure serving the Gulf Cooperation Council market. The strike caused structural damage, power failures, and rendered parts of the complex inoperative (Datacenter Dynamics, April 2026). AWS cloud operations across the Gulf were disrupted. Telegram, one of AWS's largest regional customers, experienced service degradation.

The strike happened one day after Iran's Islamic Revolutionary Guard Corps published a formal list of eighteen US technology firms designated as legitimate military targets. It happened hours after President Trump publicly dismissed the threat as "BB guns" (CNBC, April 1, 2026). The sequencing matters. For the first time in the 2026 Iran war, a named company on a formal threat list was struck inside the window the threat itself specified.

This is no longer a precedent. It is a pattern, and the pattern is being codified in doctrine.

> **[INSERT FIGURE 1 HERE: Timeline of kinetic strikes on hyperscale cloud infrastructure, February 28 to April 2, 2026]**

## The list

The IRGC's April 1 target list, distributed through a Guard-affiliated Telegram channel and carried by Tasnim News Agency, identified eighteen companies: Apple, Boeing, Cisco, Dell, G42, GE, Google, HP, IBM, Intel, JPMorgan Chase, Meta, Microsoft, Nvidia, Oracle, Palantir, Spire Solution, and Tesla (Euronews, April 1, 2026). The stated rationale was retaliatory: for every assassination, an American company would be destroyed. The stated timing was specific. Attacks would begin at 8 p.m. Tehran time on April 1.

The March 1 strikes on AWS facilities in the UAE and Bahrain had already established that commercial cloud infrastructure was within the set of Iranian military targets. What the April 1 list did was narrow the category. It moved the targeting framework from *data centers used by the US military* to a roster of named firms, on a published schedule, with a stated substitution rule between American personnel actions and American corporate facilities.

The rationale Iran has articulated through state media treats AI products as the substantive connector. In its framing of the original March 1 strikes, Iranian state media specifically identified AI systems hosted on AWS, including Anthropic's Claude, as tools the US military uses for intelligence analysis and combat simulations (TechPolicy.Press, March 2026; The Conversation, 2026). The product hosted on the server is, in Iran's stated legal theory, what makes the server a legitimate target. Not the ownership of the facility. Not the cloud provider's corporate identity. The workload.

This is a narrower and more generalizable doctrine than it might first appear. It does not require Iran to identify Department of Defense tenants on a shared platform. It requires only that a widely deployed commercial product is known to have defense applications. Most major AI systems meet that threshold.

## The law

The international humanitarian law literature has not yet caught up. The Tallinn Manual, written to address cyber operations, does not cover kinetic strikes on physical cloud infrastructure (*Journal of Conflict and Security Law*, 2025). The ICRC's "loss of functionality" approach, which argues that attacks producing loss of service qualify as attacks under IHL even without physical destruction, was developed for cyber cases. Applied to missile strikes against colocation facilities carrying civilian workloads, it does not map cleanly.

The distinction problem is severe. A hyperscale cloud region hosts hospital records alongside banking infrastructure alongside advertising platforms alongside government services alongside defense contractor workloads. The disruption to Abu Dhabi Commercial Bank, Emirates NBD, Careem, and Snowflake in the wake of the March 1 AWS strikes illustrates what civilian harm from a dual-use strike looks like in practice (TechPolicy.Press, March 2026). Standard IHL proportionality analysis asks whether the civilian cost of a strike is excessive in relation to the anticipated military advantage. When the advantage is *disruption to an AI product used for war simulations* and the cost is *regional banking services go offline for forty-eight hours*, the analysis is not obvious, and the case law is thin.

The commercial liability picture is clearer, and worse for the tech companies. Under the century-old Cuba Submarine precedent, private sector claims against state belligerents for wartime damages are unlikely to succeed (TechPolicy.Press, March 2026). Standard commercial property and business interruption insurance contracts typically exclude acts of war. Enterprise customers whose workloads were routed through the region, often without their active knowledge, have no straightforward path to recovery.

Sam Winter-Levy, a fellow at the Carnegie Endowment for International Peace, put the shift plainly in an interview with Rest of World. Protecting data centers, he said, is starting to look like protecting top-security government offices (Rest of World, March 2026). That is not a figure of speech. It is an operational description of the defensive posture hyperscalers will need to adopt if the April 1 pattern continues.

## The price

This is where the new Layer 3 reality rejoins Channel 1.

The defensive posture Winter-Levy describes is expensive. Air defense installations, reinforced construction, hardened power and cooling systems, geographic redundancy across multiple regions, specialized war-risk insurance underwritten under contested terms. None of these are new categories. Several were already present for data centers serving regulated industries. What is new is the scale and the distribution.

The scale: the combined installed base of data centers hosting any workload with plausible defense application is a substantial fraction of the global cloud. The distribution: these costs are recovered the way cloud costs have always been recovered, through pricing to customers and through siting decisions that optimize for cheap land, available grid capacity, and low political risk.

In practice, this means two things. First, cloud pricing absorbs the security premium. Customers of AWS, Microsoft Azure, Google Cloud, and Oracle pay more. For enterprise customers, that cost flows through to product prices. For government customers, it flows through to taxpayers. Neither pathway is notably regressive on its own.

Second, and more consequential, siting decisions shift. If hyperscale capacity in the Gulf now carries a materially higher insurance premium, a higher security capital cost, and an acknowledged kinetic risk, then marginal capacity gets sited somewhere else. Somewhere else means, in practice, inland US locations where land is cheap, grid capacity is available, and political risk is constituted differently. It means Virginia, Ohio, Texas, Georgia, Arizona. It means the same geography the ratepayer backlash has been building in for eighteen months.

AWS has, as of this writing, actively advised customers with Middle East workloads to migrate to alternate regions, including regions in the United States (Technology Magazine, April 2026). That guidance is prudent. It is also a concrete mechanism by which the March and April strikes accelerate the Channel 1 transmission this work has documented: data center expansion, grid infrastructure upgrades, cost socialization to ratepayers.

The Monitoring Analytics estimate that PJM data center load growth generated a $23.1 billion cost increase across the last three capacity auctions was calculated against an assumed growth trajectory (Monitoring Analytics, *Annual Report on PJM Markets*, March 2026). That trajectory did not include a scenario in which Gulf capacity relocates to the continental United States under military pressure. If the April 1 pattern continues, the trajectory is steeper than previously modeled. The cost is the same kind of cost it has always been, transmitted through the same regulatory mechanisms, falling on the same populations. It is just larger.

## What the target list actually changes

Three things, briefly.

First, the dual-use commingling problem is no longer an IHL seminar hypothetical. It is an operational reality that tech companies, insurance underwriters, and state departments of defense are negotiating in real time. The legal scholarship will catch up. The infrastructure decisions are already being made.

Second, AI products have become specific enough that state adversaries name them. The legal theory Iran has articulated, whatever one thinks of its legitimacy under international law, treats the workload as the targeting criterion. That theory, if generalized by other state actors, implies that the AI product market and the defense market are connected in ways the commercial AI market has not fully priced in.

Third, and this is the argument that belongs in a distributional analysis: the costs of militarizing cloud infrastructure do not stay in the defense budget. They flow through cloud pricing, through siting decisions, and through the ratepayer socialization mechanisms that have already produced the energy cost channel documented in earlier work. The Two Channels framework needs a small addition. Channel 1 has a new upstream driver. The AI economy's physical infrastructure is now carrying a military security premium, and the mechanism for paying that premium runs through the same residential utility bills that were already rising.

None of this is a prediction about whether the April 8 ceasefire holds, or whether a second round of US-Iran talks produces a durable settlement. The structural point is independent of the diplomatic timeline. The target list exists. The April 1 strike demonstrated willingness to execute against it. The defensive response is underway. The costs of that response are being absorbed by the same pricing and siting architecture that produced the distributional problem this work has been documenting.

The AI cost that wasn't in the debate has acquired another component. It is not only the electricity bill. It is the electricity bill plus the security premium on the infrastructure the electricity powers. Both are paid by people who did not choose to host them.

---

*Kaleb Mazurek studies the distributional politics of AI infrastructure, energy security, and geopolitical risk. He holds a research master's in Political Science from the University of Amsterdam.*

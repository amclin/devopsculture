---
title: Hit By a Bus Factor
layout: kpi
author: Anthony McLin
---
Breaking down silos and sharing knowledge across a team improves the understanding of the codebase by the entire team, and accelerates the ability for the team to react to changes or outages. Having bottlenecks where only one team member understands a portion of the code results in risky scenarios where the team is held up from being able to delivery quickly. This is the [Hit By A Bus Factor](https://en.wikipedia.org/wiki/Bus_factor). How many of your team members are indespensible to the project? That is, if they were hit by a bus, would work come to a stop?

## Formula
The higher the HBAB Factor, the better. The ideal HBaB Factor is the size of the entire team, implying that the only way work would be blocked from completion is if the entire team was incapacitated. The value can be derived from the [Assignees over the lifespan of a ticket](assignees-over-lifespan-of-ticket.html).
* A: Maturity Score for [Assignees over the lifespan of a ticket](assignees-over-lifespan-of-ticket.html)
* T: Number of members on team

<img src="https://latex.codecogs.com/gif.latex?H&space;=&space;T&space;*&space;(1&space;-&space;\frac{A}{5})" title="H = T * (1 - \frac{A}{5})" />

## Maturity Score
To normalize this to a 0-5 scale, simply multiply by 5/7.

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{5}{7}&space;*&space;H" title="M = \frac{5}{7} * H" />

## Improving
Improvements in the Hit By A Bus Factor (HBaB) can be achieved by:
1. Reducing complexity
  1. Simplifying architectures
  2. Reducing language footprints
  3. Modularization
  4. Automating specialized but repetitive tasks
2. Documenting all processes (and keeping that documentation up to date)
3. Encouraging cross-training

## See Also
1. Directly proportionate to [Assignees over the lifespan of a ticket](assignees-over-lifespan-of-ticket.html)
2. Improvements will correlate to improvements in [Collective Ownership](collective-ownership.html)
---
title: Westrum Cultural Survey Index
layout: kpi
author: Anthony McLin
---
The 2014 State of DevOps report revealed that for IT, job satisfaction is the single most important predictor of profitability, market share, and productivity. [Ron Westrum developed a model to measure job satisfaction](https://qualitysafety.bmj.com/content/13/suppl_2/ii22), and this [directly applies to DevOps](https://continuousdelivery.com/implementing/culture/).

This is a simple survey which can be performed periodically to establish trends in the organization. Note that the numbers should not be used to focus on individuals, and over-assessment must be avoided for the data to have meaning. Try for a quarterly schedule, and aggregate the numbers across projects or teams to get a feel for the general pulse. There are 6 simple questions. On a scale of 7 (agree) to 1 (disagree), rate the following:

1. On my team, information is actively sought.
2. On my team, failures are learning opportunities, and messengers of them are not punished.
3. On my team, responsibilities are shared.
4. On my team, cross-functional collaboration is encouraged and rewarded.
5. On my team, failure caused enquiry.
6. On my team, new ideas are welcomed.

## Forumla
Scoring this is simply a matter of averaging the values from the responses.

<img src="https://latex.codecogs.com/gif.latex?S&space;=&space;\frac{A_{1}&space;&plus;&space;A_{2}&space;&plus;&space;...&plus;&space;A_{6}}{6}" title="S = \frac{A_{1} + A_{2} + ...+ A_{7}}{6}" />

## Maturity Score
If you want to normalize this to a 0-5 scale, simply multiply by 5/7.

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{5}{7}&space;*&space;S" title="M = \frac{5}{7} * S" />

## Improving
This should be a tool for a general pulse, so that trends can be observed, and areas where teams need more cultural support can be identified. It is an intentionally imprecise metric, and designed to collect general mood data, not a targetted tool for asessing individual job performance. Therefore, it is very important to:

1. Keep this survey anonymous. If team members don't answer honestly, there's little value in the responses.
2. Do not over-measure this survey. Once per quarter is the recommended maximum frequency.
3. **Do not use this to justify punitive actions.** This assessent only provides value if teams feel they can provide honest answers. 
4. **Do not overemphasize this as a team goal.** Overemphasis on positive outcomes can be just as detrimental as punitive emphasis, as it can lead to skewed results.
5. If you have large enough teams, or enough data over time, apply data science practices to see if you can identify outliers in the data that can indicate particular areas of concern for particular teams, or disruptive events.
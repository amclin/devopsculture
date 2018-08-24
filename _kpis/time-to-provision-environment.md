---
title: Time to Provision New Environment
layout: default
---
# Time to Provision New Environment
As technologists we've spent decades getting good at developing and delivering efficiencies, reducing labor costs, and implementing automation. So it's no surprise that the part of DevOps we do best is automating our own tools. However, we often drop the ball on the parts of the pipeline that lie outside the software - the "hard" decisions that humans need to make around licensing, billing, scaling costs, etc.

For teams to experiment and drive organizational agility, they often will need to rollout new hardware so they can test different features or options in parallel to the main code delivery stream. This will inevitably result in unnecessary bottlnecks if these need to be manually provisioned. The obvious first step is to script everything, used dynamic provisioning tools like virtual machines and containers, and put everything behind a few button clicks.

When we measure how quickly it takes to spin up a new environment, we cannot simply measure the time from clicking the button to the environment being live. We also need to include any environment verification, and we cannot forget the the largest bottleneck, the manual human steps that go into deciding to approve and provision the environment:
* Software licensing
* Setting up billing rules
* Negotiating budgets
* Request approvals

## Formula
Time to Provision a New Environment must be calculated end-to-end, starting with the request being logged, and ending with completion of environment readiness verification and notification to the requestor that their new environment is ready. A good score should be measured in a handful of hours, not days or weeks.

T<sub>start</sub>: Timestamp of the request
T<sub>verified</sub>: Timestamp of completion notification

<img src="https://latex.codecogs.com/gif.latex?T&space;=&space;H_{prod}&space;-&space;H_{start}" title="T = T_{prod} - T_{start}" />

## Maturity Score
For executive dashboards, Time to Provision an Environment can be distilled to a simple score, from 0 to 5, 5 being the maximum positive score, representing 1 hour or less for an environment to be provisioned end-to-end.

* T<sub>ideal</sub> = 1 hour
* T<sub>max</sub> = 144 hours: Bottom cutoff timely provisioning
* M<sub>min</sub> = 0: Minimum maturity score
* M<sub>max</sub> = 5: Maximum maturity score

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{M_{max}&space;-&space;M_{min}}{T_{max}&space;-&space;T_{ideal}}(T&space;-&space;T_{max})" title="M = \frac{M_{max} - M_{min}}{T_{max} - T_{ideal}}(T - T_{max})" />

## Improving
1. Identify manual decisions and approvals. Remove them where possible.
2. Design scoring solutions that can allow decisions to be automated.
3. Use monitoring and reporting data to automatically cleanup unused environments to aleviate the worry of cost overruns.
4. For truly complex approvals, consider using Deep Learning APIs and AI strategies to replace the human bottleneck.

---
title: Collective Code Ownership
layout: default
---
# Collective Code Ownership
A team should be small enough that everyone on the team feels responsible achieving the team's collective commitments. When the team feels a collective sense of ownership, they are more likely to assist each other proactively to achieve those goals. This in turn helps distribute knowledge and expertise across theam, mitigating the [Hit By a Bus](hit-by-a-bus-factor.md) problem, and simultaneously reducing churn caused by bouncing tickets across too many team members.

## Formula
This KPI is more difficult to calculate, as it depends on your project structure. First you need to look at how your team classifies operational areas that they are responsbile for. For the purposes of this document, we'll call these operational areas "Components". Once the components are identified you can generate two different calculations to get insights into Collective Code Ownership.

### Component Participation
For each component, calculate the number of people who have worked on that component. This is similar to the [Assignees Over the Lifespan of a Ticket](assignees-over-lifespan-of-ticket.md), but only people who take an active role in owning the ticket are included. This means only contributors or assignees can be considered.

* A: Number of assignees on a ticket
* B: Number of code contributors on a ticket (not including those already counted)
* N: Total number of tickets in the component
* T: Total team size

Divide the number of owners by the team size, and then average out for all tickets in the component to get the Collective Code Ownership Ratio for the given component.

<img src="https://latex.codecogs.com/gif.latex?R&space;=&space;\frac{A_{1}&space;&plus;&space;C_{1}&space;&plus;&space;A_{2}&space;&plus;&space;C_{2}&space;&plus;&space;A_{3}&space;&plus;&space;C_{3}&space;&plus;&space;...&space;&plus;&space;A_{N}&space;&plus;&space;C_{N}}{N&space;*&space;T}" title="R = \frac{A_{1} + C_{1} + A_{2} + C_{2} + A_{3} + C_{3} + ... + A_{N} + C_{N}}{N * T}" />

### Individual Participation
Also consider collective code ownership by looking at individual team members and how many components they actively participate in. For each individual, calculate how many components they were involved with:
* C: Number of components where the individual made code commits against a ticket
* C<sub>t</sub>: Total number of components the team is responsible for
* A: Number of components where the individual was assignee on a ticket, but did not make code commits on that ticket

<img src="https://latex.codecogs.com/gif.latex?P&space;=&space;\frac{C&space;&plus;&space;A}{C_{t}}" title="P = \frac{C + A}{C_{t}}" />

## Maturity Score
To determine the team's overall score, you need to blend together both the Component Participation and the Individual Participation measures.

To determine an overall 0-5 maturity score across the entire team and all components, you need to know the weighted score for each of the components. In addition to calcuating the score for each component, also calculate the weight by determining the percentage of total tickets are represented by that component.

<img src="https://latex.codecogs.com/gif.latex?W_{c}&space;=&space;\frac{T_{c}}{T_{t}}" title="W_{c} = \frac{T_{c}}{T_{t}}" />

Then blend the weighted average of components with the average individual participation:
* N: Number of Components
* C: Collective Code Ownership Ratio for each component
* W: Calculated Weight of each component
* P: Calculated Individual Participation of each team member
* T: Total team size

<img src="https://latex.codecogs.com/gif.latex?M&space;=5&space;*&space;\frac{[(W_{1}&space;*&space;C_{1})&space;&plus;&space;(W_{2}&space;*&space;C_{2})&space;&plus;&space;...&space;&plus;&space;(W_{N}&space;*&space;C_{N})&space;]&space;&plus;&space;(\frac{P_{1}&space;&plus;&space;P{2}&space;&plus;&space;...&space;&plus;&space;P_{T}}{T})}{2}" title="M =5 * \frac{[(W_{1} * C_{1}) + (W_{2} * C_{2}) + ... + (W_{N} * C_{N}) ] + (\frac{P_{1} + P{2} + ... + P_{T}}{T})}{2}" />


## Improving
1. Look for outliers in the individual component scores and do further analysis.
   1. Is the component lacking the involvement of team members?
   2. Within a component do the tickets normally go through the same set of hands every time?
2. Review team members
   1. Train up team members on components they are not frequently participating in
   2. Look for opportunities to spread knowledge
3. Look for components that require external dependencies to deliver. Can they be reassigned or redesigned to decouple cross-team interdependencies?
4. Limit team size. If the team is too large, isolated subgroups are likely to form around particular components. Split teams if they grow too large.
5. Limit the number of initiatives active at once. Context switching devolves into pockets of team isloation.

## See Also
1. [Hit By a Bus Factor](hit-by-a-bus-factor.md)
2. Consider Collective Ownership in conjunction with [Assignees Over the Lifespan of a Ticket](assignees-over-lifespan-of-ticket.md). The goal of high collective ownership should be paired with the goal of as few assignees over the lifespan of the ticket as possible.
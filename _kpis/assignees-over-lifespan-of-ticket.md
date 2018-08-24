---
title: Number of Assignees Over Lifespan of Ticket
layout: default
---
# Number of Assignees Over Lifespan of Ticket
If a ticket bounces around between a lot of people, that's a good indication that there may be problems with process, understanding, team coordination, or communication challenges. The fewer the people necessary to route and complete a ticket, the more certain we can be that the team is taking ownership of work and reducing unnecessary context switching.

> Never have a meeting where two pizzas couldn't feed the entire group.

Jeff Bezos famously coined the two pizza rule to describe a maximum team size of around 6-8 people. Agile recommendations specify about the same (7 +/- 2), and there are sociological studies that indicate a team size of 7 is ideal for decision making, or a team size of 5 for satisfaction. Though a blended study finds that the [magic number for efficient decision making lands at 4.6](https://sheilamargolis.com/2011/01/24/what-is-the-optimal-group-size-for-decision-making/).

## Formula
The total number of assignees can be determined through simple addition:
* N<sub>a</sub>: Number of assignees over lifespan of ticket
* N<sub>c</sub>: Number of code contributors on a ticket (not including those already counted)
* N<sub>d</sub>: Number of people required to get ticket to production after the ticket is closed (not including those already counted)
* N<sub>r</sub> = {1 | 0} : Add 1 if the ticket is manually reported and is never assigned back to the reporter. Leave 0 if ticket creation is automated, or if the reporter is already in N<sub>a</sub>.
* N<sub>m</sub>: Number of distinct commenters on a ticket (not including those already counted)

<img src="https://latex.codecogs.com/gif.latex?N&space;=&space;N_{r}&space;&plus;&space;N_{a}&space;&plus;&space;N_{c}&space;&plus;&space;N_{d}&space;&plus;&space;N_{m}" title="N = N_{r} + N_{a} + N_{c} + N_{d} + N_{m}" />

Note that commentors on tickets are included in the score. Ideally the team should be able to deliver without additional outside inputs. If there is a Product Owner, they should be bringing the business insights and stakeholder interviews to the process. End-user input should be captured through surveys, usability testing, analytics, and other similar methods for sourcing data the team can leverage. This isn't to say that outside comments are a bad thing, but they should be captured and reported in a actionable way, rather than simply injecting people into the process that aren't part of the team.

## Maturity Score
For executive dashboards, Maturity in assignees over the lifespan of a ticket can be conslidated to a simple aggregated score, from 0 to 5, 5 being the maximum positive score. The values should be capped at those limits.

If bug ticket capture and logging are totally automated, N<sub>r</sub> should be 0. Likewise, if Continuous Integration and Continuous Deployment are in place, N<sub>d</sub> should be 0. If we take into consideration the related [Hit By a Bus Factor](hit-by-a-bus-factor.md) and [Collective Ownership](collective-ownership.md) concerns, then the ideal number of assignees is around 3. So we use that to determine the max score on our scale of 5. If our maximum ideal team size is 9, then we can use that to determine a minimum score of 0.

* T<sub>ideal</sub>: Minimum expected number of people touching a ticket
* T<sub>max</sub>: Cutoff for max number of people touching a ticket
* M<sub>min</sub> = 0: Minimum maturity score
* M<sub>max</sub> = 5: Maximum maturity score

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{M_{max}&space;-&space;M_{min}}{T_{max}&space;-&space;T_{ideal}}(N&space;-&space;T_{max})" title="M = \frac{M_{max} - M_{min}}{T_{max} - T_{ideal}}(N - T_{max})" />

## Improving
1. Look for ways to automate triage steps on bug tickets, so they get to the right person with fewer steps.
2. Try adopting techniques to do [bug triage as a team](https://softwareengineering.stackexchange.com/questions/293339/when-to-have-bug-triage-meetings-in-scrum-process) so that everyone is aware of the ticket and it can get to the right person.
3. Manage your flow by reducing the number of tickets in progress at once. Often teams bounce tickets around excessively based on capacity.
4. Introduce Test Driven Development, so clear technical specs are produced before introducing functional code. This will reduce the back and forth caused by unclear requirements or testing assumptions.
5. Automate unit testing.
6. Automate QA validation.
7. Keep team sizes small.
8. Organize teams to be self sufficient.
9. Reduce interdependencies between teams.

## See Also
* [Hit By a Bus Factor](hit-by-a-bus-factor.md)
* [Collective Ownership](collective-ownership.md)
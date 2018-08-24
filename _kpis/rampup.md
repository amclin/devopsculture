---
title: Rampup Speed
layout: default
---
# Rampup Speed
> "You must learn from the mistakes of others. You can't possibly live long enough to make them all yourself."
>
> -- <cite>Sam Levenson</cite>

As a team matures and develops a strong DevOps culture, it's valuable to spread the knowledge and habits to other teams, to scale that success. However, a team's success could be an artifact purely of the people on it being that magic mix of personalities that work well together. Is there an indicator we can use to measure how well a team is able to convey its collective success? We could quantifiably measure documentation output - but that's an easy score to game, and there's no way to tell if documentation provides any meaningful value, or if the team is just going through the motions in producing it. We could attempt to measure whether other teams leverage the product being produced, but that's highly dependent on particular business needs of the organziation and the particular product of the team. But perhaps we can objectively measure within the team how well knowledge is transfered by evaluating how quickly new team members are able to ramp up.

A fast rampup time for new team members indirectly measures several valuable traits. The team most likely:
1. is good at coaching new members.
2. has good documentation that is up to date.
3. has automation in place for setting up development requirements.
4. likely organizationally self-sufficient.
5. minimizes external code dependencies.
6. has a good architecutre with well-defined coding standards.

If a team is able to get a new developer productive in a short time, then it is proof that the team exemplifies agility and mature DevOps practices.

## Formula
The most straightforward way to measure Rampup Speed is to compare a new team member's start date to the date their first change hits production. With a project-based ticketing system that has open APIs, this should be straightforward:

D<sub>start</sub>: Day that the individual's account is provisioned, or they're given access to the team's ticketing system.
D<sub>prod</sub>: Date of first *production* release that contains work contributed by the individual.

<img src="https://latex.codecogs.com/gif.latex?R&space;=&space;D_{prod}&space;-&space;D_{start}" title="R = D_{prod} - D_{start}" />

## Maturity Score
For executive dashboards, Maturity in Rampup Spped can be conslidated to a simple aggregated score, from 0 to 5, 5 being the maximum positive score, representing 1 day or less for a new developer to get working tested code into production.

* D<sub>ideal</sub> = 1 day
* D<sub>max</sub> = 30 days: Bottom cutoff for poor rampup time
* M<sub>min</sub> = 0: Minimum maturity score
* M<sub>max</sub> = 5: Maximum maturity score

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{M_{max}&space;-&space;M_{min}}{D_{max}&space;-&space;D_{ideal}}(D&space;-&space;D_{max})" title="M = \frac{M_{max} - M_{min}}{D_{max} - D_{ideal}}(D - D_{max})" />

## Improving
1. A team with strong [Collective Code Ownership](collective-ownership.md) will be more likely to be good at coaching new team members.
2. Emphasize quality (rather than quantity) in documentation.
3. Automate the developer setup process.
4. Frequently test the developer setup process to ensure it's up to date.
5. Consolidate authentication accounts and automate provisioning access to systems.
6. Look for external dependencies.
7. Consider team rotations (with caution!)
8. Have regular "open houses" to showcase the team's processes, tools, and product.
9. Automate everything.

## See Also
1. Rampup Speed has underlying commonalities with [Time From Idea to Production](time-from-idea-to-production.md)
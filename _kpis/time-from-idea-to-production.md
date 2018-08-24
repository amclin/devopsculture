---
title: Time From Idea to Production
layout: kpi
author: Anthony McLin
---
Agility, rather than efficiency, is critical for digital business transformation. An organization needs to be able to pivot quickly to changing customer needs and demands. Technologists are used to solving for efficiencies, making their work, or the organizations' pipelines faster and less labor-intensive. But we often over-optimize in the technology areas that are easy to solve, forgetting about the technology-light pipelines that exist before and after the developer's work. If we refocus success to be a measurment of the end-to-end time, then we'll find ways to eliminate other non-obvious bottlenecks, and be able to deliver work to production faster. By making the entire end-to-end team responsible for this metric, crossfunctional teams targeted to specific business goals should naturally begin to form, breaking down traditional departmental silos. (if encouraged of course!)

This is most successfull if the entire idea pipeline is captured in JIRA or other ticket tracking system, including the initial concept ideation work performed by Product Owners, designers, or business teams.

## Formula
Ttime from Idea to Production is quite simple to calculate - Simply put, it's the number of days it takes an idea to get from ticket creation to production deployment:

D<sub>start</sub>: Creation date of the idea ticket
D<sub>prod</sub>: Date of *production* deployment

<img src="https://latex.codecogs.com/gif.latex?D&space;=&space;D_{prod}&space;-&space;D_{start}" title="D = D_{prod} - D_{start}" />

## Maturity Score
For executive dashboards, Time From Idea to Production can be conslidated to a simple aggregated score, from 0 to 5, 5 being the maximum positive score, representing 1 day or less for a team to brainstorm an idea and get something working tested and live in production:

* D<sub>ideal</sub> = 1 day
* D<sub>max</sub> = 30 days: Bottom cutoff for idea to production timeline
* M<sub>min</sub> = 0: Minimum maturity score
* M<sub>max</sub> = 5: Maximum maturity score

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{M_{max}&space;-&space;M_{min}}{D_{max}&space;-&space;D_{ideal}}(D&space;-&space;D_{max})" title="M = \frac{M_{max} - M_{min}}{D_{max} - D_{ideal}}(D - D_{max})" />

## Improving
1. **The most success will come orgnaizing as cross-functional teams** dedicated to the specific product and goal. When a designer, product owner, developer, and tester are all in the same room working on one common objective without outside distraction, [the magic of a startup can be replicated](http://forresterevents.net/video/2018/dt/9-0845-0920-mohammad.html).
2. **Empower** the team to design and develop their own solutions. It can be incredibly difficult to go hands-off and allow a team to self-direct to achieve clearly stated business goals, but that freedom of decision making is key to rapid agillity.
3. Compare long tickets with short tickets to identify bottlenecks, and then remove them.
4. Break down initiatives into smaller deliverables.
5. Continuously reassess the [Minimum Lovable Product](http://labs.sogeti.com/the-minimum-lovable-product/)
6. Automate everything. Set automation tasks as the highest priority work with perhaps the exception of feature delivery.
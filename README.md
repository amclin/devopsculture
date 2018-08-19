# devopsculture

1. Purpose
  1. Overview
  2. Structure
2. [KPIs](#kpis)
3. [Proposed KPIs and Contributing](kpis-proposed.md)
4. [Further Resources](#resources)

## Purpose
As Nicole Forgresn so adroitly explains, [Metrics Shape Your Culture](https://vimeo.com/173607646). Once you start measuring something, and make it a metric of success, people will naturally start figuring out how to game the systems.**This isn't a bad thing!** If you set your metrics up so that gaming the system results in the desired outcome, then the metrics are a good thing.

To this end, we can establish metrics that will help drive the cultural outcomes we wish to see on our teams. We have more than enough tools to measure efficiencies and delivery, but yet we're lacking in applying the same rigors of measurement and assessment to the most underappreciated and critical facet of how we work as technologists: **team culture**.

This project serves as a collaboration point to collect new metrics and measurement tools that are designed to measure culture.

### Structure
Each KPI below is explained in how it should affect cultural change when adopted, how to calculate it, and an assessment scale for use in reporting dashboards.
1. **Description** - An introduction to the KPI and how it will provide business value
2. **Formula** - How the KPI is calculated
3. **Maturity** - An index-based model for abstracting the KPI into a score that's measurable over time in trending dashboards
4. **Recommendations** - Tips and suggestions for how to encourage improvements

## KPIs <a id="kpis"></a>

### Time From Idea to Production
Agility, rather than efficiency, is critical for digital business transformation. An organization needs to be able to pivot quickly to changing customer needs and demands. Technologists are used to solving for efficiencies, making their work, or the organizations' pipelines faster and less labor-intensive. But we often over-optimize in the technology areas that are easy to solve, forgetting about the technology-light pipelines that exist before and after the developer's work. If we refocus success to be a measurment of the end-to-end time, then we'll find ways to eliminate other non-obvious bottlenecks, and be able to deliver work to production faster. By making the entire end-to-end team responsible for this metric, crossfunctional teams targeted to specific business goals should naturally begin to form, breaking down traditional departmental silos. (if encouraged of course!)

This is most successfull if the entire idea pipeline is captured in JIRA or other ticket tracking system, including the initial concept ideation work performed by Product Owners or business teams.

#### Formula
* Suggested, under further assesment: *
* A = 5 * 19 / (end date - start date) *

#### Maturity
**0 - 5**
Score | Range
______|_______
5 | 1 day or less
4 | 1 week
3 | 1 month
2 | 2 month
1 | 3 months (1 quarter)
< 1 | > 3 months

#### Improving

### Number of Assignees Over Lifespan of Ticket
If a ticket bounces around between a lot of people, that's a good indication that there may be problems with process, understanding, team coordination, or communication challenges. The fewer the people necessary to route and complete a ticket, the more certain we can be that the team is taking ownership of work and reducing unnecessary context switching.

#### Formula
#### Maturity
#### Improving

#### Suggestions for improving this score
1. Look for ways to automate triage steps on bug tickets, so they get to the right person with fewer steps.
2. Try adopting techniques to do [bug triage as a team](https://softwareengineering.stackexchange.com/questions/293339/when-to-have-bug-triage-meetings-in-scrum-process) so that everyone is aware of the ticket and it can get to the right person.
3. Manage your flow by reducing the number of tickets in progress at once. Often teams bounce tickets around excessively based on capacity.
4. Introduce Test Driven Development, so clear technical specs are produced before introducing functional code.
5. Automate unit testing.
6. Automate QA validation.

### Westrum Cultural Survey Index
The 2014 State of DevOps report revealed that for IT, job satisfaction is the single most important predictor of profitability, market share, and productivity. [Ron Westrum developed a model to measure job satisfaction](https://qualitysafety.bmj.com/content/13/suppl_2/ii22), and this [directly applies to DevOps](https://continuousdelivery.com/implementing/culture/).

This is a simple survey which can be performed periodically to establish trends in the organization. Note that the numbers should not be used to focus on individuals, and over-assessment must be avoided for the data to have meaning. Try for a quarterly schedule, and aggregate the numbers across projects or teams to get a feel for the general pulse. There are 6 simple questions. On a scale of 7 (agree) to 1 (disagree), rate the following:

A. On my team, information is actively sought.
B. On my team, failures are learning opportunities, and messengers of them are not punished.
C. On my team, responsibilities are shared.
D. On my team, cross-functional collaboration is encouraged and rewarded.
E. On my team, failure caused enquiry.
F. On my team, new ideas are welcomed.

#### Forumla
C = (A + B + C... ) / 6

#### Scoring
*Max:* 7
*Min:* 1

#### Suggestions for Improving
This should be a tool for a general pulse, so that trends can be observed, and areas where teams need more cultural support can be identified. It is an intentionally imprecise metric, and designed to collect general mood data, not a targetted tool for asessing individual job performance. Therefore, it is very important to:

1. Do not over-measure this survey. Once per quarter is the recommended maximum frequency.
2. **Do not use this to justify punitive actions.** This assessent only provides value if teams feel they can provide honest answers. 
3. **Do not overemphasize this as a team goal.** Overemphasis on positive outcomes can be just as detrimental as punitive emphasis, as it can lead to skewed
4. If you have large enough teams, or enough data over time, apply data science practices to see if you can identify outliers in the data that can indicate particular areas of concern for particular teams, or disruptive events.

### Rampup/Onboarding Index
#### Formula
#### Maturity
#### Improving

### Time to Provision New Environment
#### Formula
#### Maturity
#### Improving

### Agility Index
An executive overview score of all the various parts.
#### Formula
#### Maturity
#### Improving

### Release Size<a id="release-size"></a>
One of the principles of Agile, DevOps, and Extreme Programming is to favor continuous integration and continuous deployment. To avoid monolithic pileups that are disruptive both the the software as well as the team, we should be practicing small, fast, *Lean* releases, ideally through Continuous Delivery. Once way to measure this is to check release size. We can measure the size of the release as a ratio of the number of lines changed in a release over the the total lines of code in the project.

#### Formula
S: Release Size
L: Lines Changed Since Last Release
T: Total Lines of Code

**S = L / T**

#### Maturity
Over time, maturity in this can be measured on a scale of 1 to 5, as a rolling average over the last 10 releases.

### Code Refactoring<a id="refactoring"></a>
An agile team is receptive to change. And a good indication of this is that the team is improving the quality of their code over time. This should manifest through continuous refactoring. We can objectively measure code refactoring by looking for code change where unit tests do not require modification, and the unit tests continue to pass. That indicates that the code

To do this we need to aggregate several data points:
1. Code Coverage - Without significant coverage for the unit tests, it is difficult to confirm that the code changes leave original functional behavior intact.
2. Amount of Code Changed - Successful refactoring of a file or method will likely result in significant code change of that file. (Note that this likely will contradict the goals measured in [Release Size](#release-size).)
3. Amount of Unit Tests Changed - To prove that refactoring is successful and non-breaking, unit tests should not require modifications.

#### Formula

#### Maturity

### Hit By A Bus Factor<a id="#hit-by-a-bus"></a>
Breaking down silos and sharing knowledge across a team improves the understanding of the codebase by the entire team, and accelerates the ability for the team to react to changes or outages. Having bottlenecks where only one team member understands a portion of the code results in risky scenarios where the team is held up from being able to delivery quickly. This is the [Hit By A Bus Factor](https://en.wikipedia.org/wiki/Bus_factor). How many of your team members are indespensible to the project? That is, if they were hit by a bus, would work come to a stop?

#### Formula
#### Maturity
The ideal HBaB Factor is the size of the entire team, implying that the only way work would be blocked from completion is if the entire team was unavailable.

### Collective Code Ownership
#### Formula
#### Maturity
#### Improvement


### Improvement
Improvements in the Hit By A Bus Factor (HBaB) can be achieved by:
1. Reducing complexity
  1. Simplifying architectures
  2. Reducing language footprints
  3. Modularization
  4. Automating specialized but repetitive tasks
2. Documenting all processes (and keeping that documentation up to date)
3. Encouraging cross-training

### Coding Standards
#### Formula
#### Maturity
#### Improvement

## Further Resources<a id="resources"></a>
1. Forsgren, Nicole. *How Metrics Shape Your Culture* https://vimeo.com/173607646
2. Humble, Jez. *Continuous Delivery* https://continuousdelivery.com/
3. *Extreme Programming: Values, Prinicples, and Practices* https://www.altexsoft.com/blog/business/extreme-programming-values-principles-and-practices/
# Proposed KPIs
The following KPIs were suggested by my cohort of fellow students particpating in SapientRazorfish's [CMTOu](https://www.whatsnextisnow.com/)

If you have ideas for further KPIs that would result in a positive impact on organizational culture, then please, [Fork this on github](https://github.com/amclin/devopsculture/fork), edit this document, and issue a pull request to bring it back into the main repo. Please include your name and link to your GitHub profile using this format:

```
## Name of Suggested KPI<a id="shortname"></a>
**Proposed By:** [Your Name](http://example.com)

Text of proposed KPI, how to measure it, calculations, outcomes, etc.
```

As these ideas are reviewed and formalized, they'll get moved into the [main list of KPIs.](README.md#kpis)

## Coding Standards
How well does the team follow coding standards?

## Ticket State Churn
How much churn is there as a ticket bounces back and forth between states?

## Cycle time from Idea to DOR
**Proposed By:** Ninad Patil

How it would be calculated - Data will be collected from JIRA. It will be governed through JIRA workflow based on ticket status. Data will be collected at 2 points, first when the story was added in JIRA and 2nd when the story status was updated to 'Requirements closed'.
Frequency of measurement - Done monthly for all stories included as part of the release
What scale it would use (min/max, percentage, etc) - Avg. # of days it takes for a story in the backlog to move from Idea to DOR.
## Defect Injection Rate (DIR)
**Proposed By:** Ninad Patil

How it would be calculated - Indicates the injection rate of defects in our software delivery lifecycle and is a cumulative of the # of defects identified across all forms of testing; manual, automated, accessibility, performance & security.
Frequency of measurement - Done monthly for every release
What scale it would use (min/max, percentage, etc) - % as a unit of how many total defects were introduced across all stories per Release.
## Automated Test Coverage
**Proposed By:** Ninad Patil

How it would be calculated - Calculated based on # of test scenarios against failed scenarios across both functional & regression tests. The data is collected under OpenTest framework which we are using to conduct automation tests. The framework will be integrated with Speedy 2.0 to export data and generate dashboards to track progress & quality of Delivery.
Frequency of measurement - Done at a Sprint level (every 2 weeks), and monthly for every release (a release for us is work conducted under 2 sprints)
What scale it would use (min/max, percentage, etc) - % as a unit to measure pass vs. fail

## Feedback Culture
**Proposed By:** [Holger Hellinger](https://github.com/polent)

Calculated by Surveys done. This was frequently done on projects in the last years but somehow does not happen on current projects. It was done every 6-12 months and was called project health check. It asked teams questions around different topics and helped getting a project team mood oversight. 
 
You can ask questions frequently and give them rankings. For example, 1-5 for
0. not applicable
Not meeting expectations
2. partially meeting expectations
3. meeting expectations
4. exceeding expectations
 
Out of this you generate averages, and this then can represent %. These then result in color ratings. 
green, amber, red. 
 
With that you get a good oversight and visual impression and can also create charts if needed. 
 
Metrics or questions to ask are Feedback Culture. You could ask questions like 
 
* Is your feedback heard and recognized?
* Do the Project leads ask for feedback?
* Are there actions taken after your input? 
* and so on.....
 
## Person value
**Proposed By:** [Holger Hellinger](https://github.com/polent)
 
* Do you see yourself a needful as a team member?
* Can you be replaced within a week?
* Do you think that your work is honored enough? 
* Are you paid in a way that matches your value providing to the team? 
 
## Diversity Questions
**Proposed By:** [Holger Hellinger](https://github.com/polent)
 
* Are you team mates handled equally?
* If you feel harassed, can you openly communicate this in your team?
* Do you feel respected?


## Team temperature
**Proposed By:** [Gavin Estey](https://www.linkedin.com/in/gavinestey/)

With large distributed teams it's hard to get an overall idea of how everyone is feeling, the feedback you get is often from the most vocal. I would borrow an idea of feedback from some customer service interactions--are things positive/neutral/negative?

a) How it would be calculated: email where team members would have to click on a  😀 / 😐 / 😰 icon
b) Frequency of measurement: weekly
c) What scale it would use: Average of +1/0/-1 scores

We want to try to avoid a downward trend as the project progresses where things start off positive and trend towards a death-march by the end. Need to maintain that culture of positivity throughout and work on fixing bad processes that detract from it.

## Ratio of bug fixing to development
**Proposed By:** [Gavin Estey](https://www.linkedin.com/in/gavinestey/)

Ideally this is as low as possible--the team should be creating value, not fixing problems--but measuring it might be controversial. You need to track hours against tickets.

a) How it would be calculated: to move a ticket to dev-complete, you need to enter an estimate for the number of hours spent working on it 
b) Frequency of measurement: ad hoc, but most likely a summary per-sprint would be useful
c) What scale it would use: a percentage

If we can track how much time we work on bugs instead of features maybe we can use the cost of this to justify improvements that reduce the number of bugs in the first place. It's a tough metric, we have to introduce a slight negative--tracking hours--to try to understand the tax of previous short-term decisions. It would be interesting to look at features that had a high ratio against those that didn't and try to identify the differences so that improvements to processes can be found.

## Time to dev-complete / Time to live
**Proposed By:** [Gavin Estey](https://www.linkedin.com/in/gavinestey/)

This is really two, but they are linked and calculated in the same way. How long did it take to get a story done and then how long did it take to get it into production. With continuous deployment we can optimize the latter.

a) How it would be calculated: track the time tickets spent in certain states
b) Frequency of measurement: continuous as tickets are closed
c) What scale it would use: number of hours

The delay from dev-complete to getting it live is work-in-progress that's preventing us from extracting value from the investment in that work. We can improve our delivery to get it into production faster. The delay getting to dev-complete in the first place is a different matter, we can't necessarily get developers to work faster, but it might be a sign that tasks are not being decomposed in a granular enough way. We want to maintain a steady value and it not get worse.

## Experiment Velocity
**Proposed By:** [John Moerer](https://www.linkedin.com/in/johnmoerer/)

Calculated: Create a new "Experiment" object type in Jira to capture experiments that the team devises. These would be story-pointed and prioritized into the sprint backlog along with other work so that an experiment-specific velocity per sprint could be calculated.
Frequency: Once per sprint
Scale: Experiment points / sprint. This may differ between sprint teams so it should not be used to compare/judge teams against each other. Instead, it would be useful in charting the progress of a specific sprint team in increasing the mix of experiments in each sprint.
Successful Outcome: sprint teams are self-motivated to increase experimentation over time

## Leadership Support Index
**Proposed By:** [John Moerer](https://www.linkedin.com/in/johnmoerer/)

Calculated: Anonymous pulse-check survey of each individual in the organization asking them to rate on a scale of 1-10 how much support they feel they get from their leadership to experiment, fail and learn.
Frequency: Once per quarter, with results shared across the organization
Scale: Simple subjective rating between 1-10. Averaged over the full organization, and per product team
Successful Outcome: Teams will feel that they have a voice to express if management words and actions don't align. Management/leadership will have accountability to support a culture of learning and experimentation.

## KPI Postmorten Followthrough
**Proposed By:** [John Moerer](https://www.linkedin.com/in/johnmoerer/)

Calculated: Number of action items from last retrospective completed / Number of action items from last retrospective identified.
Frequency: Once per sprint
Scale: Simple completion percentage per agile team per sprint
Successful Outcome: Encourage identification of actionable learnings in each retrospective, and provide some incentive to put those learnings into action to continuously improve team performance.


## Measure Meam Time to Repair (MTTR)
**Proposed By:** [Eswara K Palakollu](https://www.linkedin.com/in/eswara-kumar-palakollu-25613b3/)

Calculated: Measure MTTR effectively and calcualte benefits of improving MTTR and continuous improvement mindset.
Frequency: Calculated continuously
Scale: Measure in production and leverage Chaos Monkey
Successful Outcome: Preferring MTTR over MTBF will help organisations to build continous learning and continuous improvement mindset. It will positively affect business outcomes with continuous deployments to production.

## Measure cost of delay to help product owners to prioritise tasks
**Proposed By:** [Eswara K Palakollu](https://www.linkedin.com/in/eswara-kumar-palakollu-25613b3/)

Calculated: Measure cost of delay of features due to slow route to live processes post DOD.
Frequency: Every sprit for every JIRA item
Scale: Predict sales based on past sales data or based on projected data every sprint
Successful Outcome: Cost of delay is not often calculated and features completed sit in test environments for months before hitting production. Predicting the cost of delay will help priortise product owners and system owners to take necesary actions to realise the business value quickly.

## Calculate benefits realised against prediction
**Proposed By:** [Eswara K Palakollu](https://www.linkedin.com/in/eswara-kumar-palakollu-25613b3/)

Calculated: Calculate benefits at a sizable feature level will help business to take right decisions.
Frequency: Every two weeks or live dashboards based on criticality of feature
Scale: for every feature or epic
Successful Outcome: It will help business stakeholders to visualise the benefits and monitor the benefits delivered by each of the features. It will help people to adopt data driven mindset and brings accountability.

---
title: Release Size
layout: kpi
author: Anthony McLin
---
One of the principles of Agile, DevOps, and Extreme Programming is to favor continuous integration and continuous deployment. To avoid monolithic pileups that are disruptive both the the software as well as the team, we should be practicing small, fast, *Lean* releases, ideally through Continuous Delivery. Once way to measure this is to check release size. We can measure the size of the release as a ratio of the number of lines changed in a release over the the total lines of code in the project. The smaller the amount of change in the release, then the more frequently we can reliably release.

## Formula
The release size index is scored on a weighted scale from 0 - 5. The theoretical maximum score of 5 would indicate no lines changed in the release. A release where everything has changed would score 0.

**Release Size Score** can be calculated as the percentage of changed lines in the release.

<img src="https://latex.codecogs.com/gif.latex?S&space;=&space;\frac{L_{changed}}{L_{total}}" title="S = \frac{L_{changed}}{L_{total}}" />

Since this number is a ratio based on the size of your codebase, watch out for gaming this metric by adding significant static code over time. When looking at trending data, this should always be considered in the context of increasing or decreasing size of the total codebase.

## Maturity Score
Naturally if a project total codebase is very large, this number will be quite small. Therefore a scaling factor should be used if comparing projects of different sizes. What matters more is how this number changes over time within a project.

Release Size Score can be tracked as distinct values release to release, but the data will not be particularily useful if your releases vary significantly in size. Instead, consider tracking a rolling average of the last subset of releases to get a better view into trending behaviors.

* S: Percentage of changed lines
* S<sub>ideal</sub> = 0.001: Minimum percentage of changed lines
* S<sub>max</sub>= .01: Cutoff for maximum percentage of changed lines
* M<sub>min</sub> = 0: Minimum maturity score
* M<sub>max</sub> = 5: Maximum maturity score

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;(\frac{M_{max}&space;-&space;M_{min}}{S_{max}&space;-&space;S_{min}})(S&space;-&space;S_{max})" title="M = (\frac{M_{max} - M_{min}}{S_{max} - S_{min}})(S - S_{max})" />

So if we established that for a project 1% is the highest amount of change we want in a release, and 0.001% is the smallest we can achieve (1 line out of 10,000), the formula would look like:

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;(\frac{0&space;-&space;5}{0.01&space;-&space;0.001})(S&space;-&space;0.01)" title="M = (\frac{0 - 5}{0.01 - 0.001})(S - 0.01)" />

## Improving
1. Shorten development cycles. The shorter the duration, the smaller the total amount of work.
2. Move from a monothic architecture to microservices architectures where pieces can be deployed independently.
3. Abstract layers to decouple presentaion tier from services and business logic. APIs should be deployable independently of the API subscribers.
4. Adopt the [Steel Thread Concept](http://www.agildata.com/keep-it-lean-you-arent-ready-for-scrum/) for defining acceptance criteria and breaking down features into manageable buckets.
5. Implement end-to-end Continuous Delivery so that code changes can go to Production as soon as they've passed testing and been accepted.

## See Also
* [Code Refactoring](code-refactoring.html)




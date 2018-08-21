---
title: Release Size Score
layout: default
---
# Release Size Score
One of the principles of Agile, DevOps, and Extreme Programming is to favor continuous integration and continuous deployment. To avoid monolithic pileups that are disruptive both the the software as well as the team, we should be practicing small, fast, *Lean* releases, ideally through Continuous Delivery. Once way to measure this is to check release size. We can measure the size of the release as a ratio of the number of lines changed in a release over the the total lines of code in the project. The smaller the amount of change in the release, then the more frequently we can reliably release.

## Formula
The release size index is scored on a weighted scale from 0 - 5. The theoretical maximum score of 5 would indicate no lines changed in the release. A release where everything has changed would score 0.

**Release Size Score** can be calculated as percentage of unchanged lines in the release, multipled by **5**

<img src="https://latex.codecogs.com/gif.latex?Size&space;Score&space;=&space;5&space;*&space;(&space;1&space;-&space;\frac{L_{Changed}}{L_{Total}}&space;)" title="Size Score = 0.2 * ( 1 - \frac{L_{Changed}}{L_{Total}} )" />

## Maturity
Release Size Score can be tracked as distinct values release to release, but the data will not be particularily useful if your releases vary significantly in size. Instead, consider tracking a rolling average of the last subset of releases to get a better view into trending behaviors.

Since this number is a ratio based on the size of your codebase, watch out for gaming this metric by adding significant static code over time. When looking at trending data, this should always be considered in the context of increasing or decreasing size of the total codebase.

## Improving





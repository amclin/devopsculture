---
title: Release Size
layout: default
---
# Release Size
One of the principles of Agile, DevOps, and Extreme Programming is to favor continuous integration and continuous deployment. To avoid monolithic pileups that are disruptive both the the software as well as the team, we should be practicing small, fast, *Lean* releases, ideally through Continuous Delivery. Once way to measure this is to check release size. We can measure the size of the release as a ratio of the number of lines changed in a release over the the total lines of code in the project.

## Formula
S: Release Size
L: Lines Changed Since Last Release
T: Total Lines of Code

**S = L / T**

## Maturity
Over time, maturity in this can be measured on a scale of 1 to 5, as a rolling average over the last 10 releases.
## Improving
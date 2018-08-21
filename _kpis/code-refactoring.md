---
title: Code Refactoring
layout: default
---
# Code Refactoring
An agile team is receptive to change. And a good indication of this is that the team is improving the quality of their code over time. This should manifest through continuous refactoring. We can objectively measure code refactoring by looking for code change where unit tests do not require modification, and the unit tests continue to pass. That indicates that the code

To do this we need to aggregate several data points:
1. Code Coverage - Without significant coverage for the unit tests, it is difficult to confirm that the code changes leave original functional behavior intact.
2. Amount of Code Changed - Successful refactoring of a file or method will likely result in significant code change of that file. (Note that this likely will contradict the goals measured in [Release Size](#release-size).)
3. Amount of Unit Tests Changed - To prove that refactoring is successful and non-breaking, unit tests should not require modifications.

## Formula
## Maturity
## Improving
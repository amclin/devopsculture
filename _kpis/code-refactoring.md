---
title: Code Refactoring Ratio
layout: default
---
# Code Refactoring
An agile team is receptive to change. And a good indication of this is that the team is improving the quality of their code over time. This should manifest through continuous refactoring. We can objectively measure code refactoring by looking for code change where unit tests do not require modification, and the unit tests continue to pass. That indicates that the code

To do this we need to aggregate several data points:
1. Code Coverage - Without significant coverage for the unit tests, it is difficult to confirm that the code changes leave original functional behavior intact.
2. Amount of Code Changed - Successful refactoring of a file or method will likely result in significant code change of that file. (Note that this likely will contradict the goals measured in [Release Size](#release-size).)
3. Amount of Unit Tests Changed - To prove that refactoring is successful and non-breaking, unit tests should not require modifications.

## Formula
* C<sub>delta</sub>: Number of lines of code changed *excluding* unit tests
* T<sub>delta</sub>: Number of lines of code changed in the unit tests

Ratio of code changes to test changes:
<img src="https://latex.codecogs.com/gif.latex?R&space;=&space;\frac{C_{\Delta&space;}}{T_{\Delta}}" title="R = \frac{C_{\Delta }}{T_{\Delta}}" />

## Maturity Score
To simply the metric to a 0-5 score that can be monitored over time, we need to take a few more data points into consideration.

* R<sub>max</sub> = 20: Ideally refactoring should have no test changes, so a ratio of 20:1 is chosen.
* R<sub>min</sub> = 1: An equal number of code changes to test changes indicates a strong likelyhood the code has significant behavioral changes.
* M<sub>min</sub> = 0: Minimum maturity score
* M<sub>max</sub> = 5: Maximum maturity score

<img src="https://latex.codecogs.com/gif.latex?M&space;=&space;\frac{&space;M_{max}&space;-&space;M_{min}&space;}{R&space;-&space;R_{min}}(R&space;-&space;R_{max})" title="M = \frac{ M_{max} - M_{min} }{R - R_{min}}(R - R_{max})" />

### TODO: Future Refinement
1. [#1](https://github.com/amclin/devopsculture/issues/1): Maturity Scores calculated with Refactoring Ratios under 0 have nonintuitive results.
2. [#1](https://github.com/amclin/devopsculture/issues/1): No matter how big a code change, if the tests don't change, the Refactoring Ratio stays `undefined`
3. [#2](https://github.com/amclin/devopsculture/issues/2): Improving code coverage by adding unit tests without code changes will result in a counterintuitively lowered Maturity Score.

## Improving
Using a reporting tool like Clover or Istanbul, make sure that your code coverage not only reaches all files and methods, but that all branches that code can take are covered. In addition, make sure that exception scenarios and unexpected data inputs are being tested.

Work to improve overall code coverage in unit tests. With higher total code coverage, the impact of changing one or two tests will have smaller effect for Code Refactoring Ratio than if code coverage is limited.

Work to test the *behaviors and outputs* of methods, and not what the methods do internally. The internals of any method should be considered a black box. By focusing on testing the outputs, we ensure that the internals of changeable, but that the method is transparently providing the same interface to anything that uses it.
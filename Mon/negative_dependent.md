# [Negative Dependent Stable Polynomial](http://suvrit.de/teach/nips18tut.html)

Slides can be downloaded here [Part1](https://media.neurips.cc/Conferences/NIPS2018/Slides/negDepTut_part1.pdf) and [Part2](https://media.neurips.cc/Conferences/NIPS2018/Slides/negDepTut_part2.pdf)

Recording is [here](https://www.facebook.com/nipsfoundation/videos/1116042135230913/)

## What is negative dependent?

Once event1 happens, the chance of event2 happens decreases dramatically.

P(S1 and S2) << P(S1)P(S2)

P(S1 | S2) << P(S1)

Applications: Recommendation system, Compressing data

The process is also called Determinantal Point Process (DPP). There are quite a bit of good intro in the "Introduction to ML" by Kulesza & Taskar

## Negative Dependency and its Mathematical representation

This can be represents as a vector. The event can be represented as a vector in
space. The joined prob is then the area of the diamond shape constructed by
those two vectors.

u(S) proprosion to vol of vectors
u(S) proportion to the det of vectors

First proposed by "Fermion Processes".

Strongly Raleigh for a polynomial.


A very good reference of this topic is by Alex Kulesza and Ben Taskar [here](https://arxiv.org/abs/1207.6083.pdf)
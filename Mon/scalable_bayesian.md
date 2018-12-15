# Scalable Bayesian talk (Dunson)

Slide can be downloaded [here](https://media.neurips.cc/Conferences/NIPS2018/Slides/ScalableBayes_dunsonNIPS2018.pdf)

Recording is [here](https://www.youtube.com/watch?v=0HXpnG_WnlI)

- MCMC is scalable. Some algorithm is scalable. There are also algorithms that can be approximated etc.
- There are two parts of the talk, the first one is "big-n" problem (number of records are a lot)
- The second part is high dimensionality (high-p) problem.

Here is the list of algorithms that can deal with the scalability:

* Embarrassingly paralleled (EP) MCMC: MCMCs in parallel with different subsets of data
* Approximated MCMC: Use the approximation theory during the MCMC process to speed up the process.
* Conditioned-Bayes (cBayes) method, discussed extensively later in the talk. The benefit of this process is it is very robust.
* Hybrid algorithm: fast estimation of the parameters. Then use those as the starting point ti do further MCMC using the subset of dataset.

## EP MCMC

**TODO**: insert the picture here about the study with Alibaba

Average weighting combination of all posterior to get the final posterior for
the whole dataset.

The method used to averaging all posterior is called WASP (Wassertein Distance
between the posterior centers) The detail paper can be found
[here](https://arxiv.org/pdf/1508.05880.pdf).

The second method to do the averaging is to use: Simple & Fast Posterior
Interval Estimation (PIE) method, This method is built upon the Wassertein
distance. _confirm?_ is to utilize the Wassertein distance to calculate the
quantile/percentile of the target variable (or function results of the target
variable). The do a simple average on top of that. The detail paper can be
found [here](https://arxiv.org/abs/1605.04029) Also called "bags of little
bootstraps"

## aMCMC (approximation MCMC)

[Approximating
MCMC](https://en.wikipedia.org/wiki/Approximate_Bayesian_computation) is
another way of making MCMC faster and scalable. But keep in mind that
approximation may diverge.

## C-Bayes (Robustness under big n)

In traditional MCMC, we always assume that posterior model is correct, given sufficient data. In a real MCMC case, this may not be true. 

Given an example of bimodal mixed Gaussian distribution as "true" distribution,
add a random perturbation to it and then use aMCMC to calculate the posterior
distribution.

Picture of mixed Gaussian distributions here.

J. Miller and D. Dunson propose a coarsening-Bayes method. This method is shown to be more stable under bigger scale of data conditions.

The ideal is to tweak the Bayesian paradigm a little bit. Instead of a
posterior of the distribution, we are looking at the posterior's Wassertein
distance smaller than a cut-off.

## Big "p" problem (high dimensional data issue)

### Variable Selection Problem

y <- generic variance x_j

There are two ways of doing Var Select:

* independent screening (using p-value, can be iterated such as
  forward/backward selection)
* Penalty terms
  * L2 penalty
  * L1 LASSO: L1 LASSO is equivalent to Bayesian method of setting parameter
    prior to N(0, sigma)

The problem of L1 LASSO is it only gives a point estimate. Also, normal prior
may not be the best prior to look for. The better priors are:

* horse-shoe
* Generalized double Pareto
* Dirchlet-Laplace

They all give more control towards 0 than boundaries (_confirm?_)

Dunson also has a [Bayesian Shrinkage Prior](https://arxiv.org/abs/1705.00841)
proposed during the tutorial. This paper is authored by one of his previous
students.

Summary of variable selection problem above: (not trustworth?)

* What is our problem is not sparse? The real solution may be a lot of more
  complex than using just part of variables there? Should we blindly trust the
  model we selected using Bayesian approach?
* Prior is too strong, too informative?

## Applications:

### DNA methylation problem

[This](https://github.com/lockEF/BayesianScreening) study is to identity the
location of a gene (or a group of genes) that causes certain cancel when
methylized. This is a typical big "p" problem.

### Brain Connection

High Creativity person has a well connected left and right hemisphere.
[Press](https://www.psychologytoday.com/ca/blog/the-athletes-way/201702/highly-creative-people-have-well-connected-brain-hemispheres) and the [paper](https://projecteuclid.org/euclid.ba/1479179031)

Also a "big p" problem. This one is a little different. This is a general
Bayesian procedure for inference and testing of group differences in the
network structure.


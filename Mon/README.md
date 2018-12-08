# Monday (Dec 3rd) Tutorial Day

## Scalable Bayesian talk (Dunson)

- MCMC is scalable. Some algorithm is scalable. There are also algorithms that can be approximated etc.
- There are two parts of the talk, the first one is "big-n" problem (number of records are a lot)
- The second part is high dimensionality (high-p) problem.

Here is the list of algorithms that can deal with the scalability:

* Embarrassingly paralleled (EP) MCMC: MCMCs in parallel with different subsets of data
* Approximated MCMC: Use the approximation theory during the MCMC process to speed up the process.
* Conditioned-Bayes (cBayes) method, discussed extensively later in the talk. The benefit of this process is it is very robust.
* Hybrid algorithm: fast estimation of the parameters. Then use those as the starting point ti do further MCMC using the subset of dataset.

**TODO**: insert the picture here about the study with Alibaba

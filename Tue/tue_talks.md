# Talks

## On Neuronal Capacity

Paper is [here](http://papers.nips.cc/paper/by-source-2018-3826). We define the
capacity of a learning machine to be the logarithm of the number (or volume) of
the functions it can implement. We review known results, and derive new
results, estimating the capacity of several neuronal models: linear and
polynomial threshold gates, linear and polynomial threshold gates with
constrained weights (binary weights, positive weights), and ReLU neurons. We
also derive capacity estimates and bounds for fully recurrent networks and
layered feedforward networks.

Notes:

* The capacity of the target function(s) is the volume of this function (or the
  size of all hypothesis that it can test)

* In a simple case (simple threshold neuron), the capacity is bounded at N^2,
  where N is the number of variables.

* In RNN network, the capacity is N^3.
* This theory would be useful to compare between network structures.

Reference: Arxiv [paper](https://arxiv.org/abs/1803.10868)

## Learning Overparameterized Neural Networks via Stochastic Gradient Descent on Structured Data (Rapid Session)

Basically, this paper presents a theoretical view of why larger NN
(over-parameterized) network helps the optimization problem. The explanation is
on a 2-level NN on a clustered data.

Neural networks have many successful applications, while much less theoretical
understanding has been gained. Towards bridging this gap, we study the problem
of learning a two-layer overparameterized ReLU neural network for multi-class
classification via stochastic gradient descent (SGD) from random
initialization. In the overparameterized setting, when the data comes from
mixtures of well-separated distributions, we prove that SGD learns a network
with a small generalization error, albeit the network has enough capacity to
fit arbitrary labels. Furthermore, the analysis provides interesting insights
into several aspects of learning neural networks and can be verified based on
empirical studies on synthetic data and on the MNIST dataset.

Paper is [here](http://papers.nips.cc/paper/by-source-2018-4999) and the presentation slide is [here](https://nips.cc/media/Slides/nips/2018/220cd(04-10-05)-04-10-20-12563-Learning_Overpa.pdf)

## Bayesian Model-Agnostic Meta Learning (Rapid Presentation)

Paper can be downloaded [here](http://papers.nips.cc/paper/by-source-2018-3652)
and the slide is
[here](https://nips.cc/media/Slides/nips/2018/220e(04-15-30)-04-15-40-12594-Bayesian_Model-.pdf).
Recording can be found
[here](https://www.facebook.com/nipsfoundation/videos/265425524142328/) around
13min.


## Neural Ordinary Differential Equations (Award Winning Oral)

Paper can be found [here](http://papers.nips.cc/paper/by-source-2018-3310).
Recoding can be found
[here](https://www.facebook.com/nipsfoundation/videos/265425524142328/) around
24min.


Reference: [MIT Technology Review](https://www.technologyreview.com/s/612561/a-radical-new-neural-network-design-could-overcome-big-challenges-in-ai/)



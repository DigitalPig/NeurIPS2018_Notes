# Deep Learning and its applications in Materials and Molecules

Workshop [Agenda](http://quantum-machine.org/workshops/nips2018/)

## Boltzmann Generators

Paper can be found [here](https://arxiv.org/abs/1812.01729).

The main idea is how to sample the molecular structure? We use to use molecular
dynamic but that is sometimes very hard to sample non-equilibrium states like
transition state.

In this research, we know what the final energy distribution looks like but we want to sample the structure. What we did is to start with Gaussian distribution,


## Tensor Field Network

Paper is published [here](https://arxiv.org/abs/1802.08219).

The main idea here is 1) how do you let the CNN learn the molecular structure?
2) how do you let the NN to understand that a simple rotation of molecule is
equivalent?

To solve the first question, the authors use the same method as SchNet. Chemical structure is converted into points.

To solve the second question, the authors use the tensor field with information
of the structure like position of the atoms, type of atoms etc.
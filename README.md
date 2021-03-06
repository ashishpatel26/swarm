# **Optimization Methods for Engineers** - Particle Swarm Optimization, Nelder-Mead [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/haeggee/swarm/master)
This repository includes sample applications and use cases of optimization methods, mainly particle swarm optimization. It was created as part of the course 'Optimization Methods for Engineers' at ETH Zürich. Go to https://mybinder.org/v2/gh/haeggee/swarm/master to play around with the notebooks yourself!

#### Part 1: Analysing optimizers on typical test functions for optimization
##### **Test functions (Rastrigin, McCormick, Easom):**
1. Optimization with PSO:
    * Optimization
    * Plot cost history
    * Visualization in 2D
    * Visualization in 3D 
    * Analysis of good choice of hyperparameters 
    
    
2. Comparison with Nelder Mead:
    * Performance
    * Convergence rate
    * Complexity

##### **Discussion:**
1. Strengths
2. Weaknesses

#### Part 2: Analysing PSO, NM for neural network training
Neural networks are a way of parametrizing non-linear functions. Usually, the training of a neural network is done via different variants of gradient descent, i.e. trying to find a good choice of weights by minimizing the loss function.

What we do here in this notebook is another approach: instead of using a gradient based method that does the fitting of the network, we want to apply the particle swarm optimization and Nelder Mead algorithms to find a good choice of weights. Our application is classical binary classification. The discussion includes:
* Our own implementation of a neural net, forward propagation and loss function
* An interactive example and visualization for binary classification, where one can choose different hyperparameters
* Usability and performance of these optimizers for neural net training


## Developing

All notebooks depend on and use Matplotlib, NumPy, PySwarms, Sklearn, and SciPy. The Python version used is 3.8. See [`requirements.txt`](https://github.com/haeggee/swarm/blob/master/requirements.txt).

Please consider the rule to always push your changes to the notebook only **AFTER** restarting the kernel and executing all cells starting from the first to ensure a working notebook.

## Bonus
* **Neural Network:** ~~If time is enough, a nice idea is to implement and fine-tune a certain neural-network for an existing dataset (see https://pyswarms.readthedocs.io/en/latest/examples/usecases/train_neural_network.html as a reference)~~ **Implemented!** TODO-list can be found in the notebook.
* **Bee algorithm:** Also, it would be cool the test the bees algorithm (https://en.wikipedia.org/wiki/Bees_algorithm), which is a special case of the generic particle swarm idea. To implement this, we would have to write our own optimization loop where we differentiate between the different types of bees when updating the positions (scouts, etc.). To see how to implement our own optimization method, we can refer to https://pyswarms.readthedocs.io/en/latest/examples/tutorials/custom_optimization_loop.html
* **Simulated Annealing** for our problems. We implemented the basic algorithm, but sadly did not find the time to test and use it.

# Credits
Credits belong to:
* The contributors to the PySwarm Toolkit: https://github.com/ljvmiranda921/pyswarms
* Andreas Krause and the Introduction to Machine Learning lecture at ETH. Some code and plot helpers were reused. See https://las.inf.ethz.ch/teaching/introml-s20

# License
All code in this repository is published under the terms of the [MIT License](LICENSE)

© July 2020 [Alexander Haegele](https://github.com/haeggee), [Richard von der Horst](https://github.com/RichardVDH), [Paul Elvinger](https://github.com/elvingerpaul)

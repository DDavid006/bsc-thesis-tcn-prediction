# bsc-thesis-tcn-prediction
Bachelor thesis project on perturbation spread prediction using Temporal Convolutional Networks.

I uploaded a concise version of the code I used to test the TCN's network ability to extrapolate the perturbation spread in an Ising chain beyond the reasonable classical computational limits. 

The motivation behind this thesis is that dynamics of unstable quantum systems (such as our perturbed ground state) become exponentially hard to compute classically due to the increase of entanglement entropy. Therefore this project explores the usage of neural networks, specifically TCN's, to replace classical simulation methods after a certain difficulty threshold and calculate the remaining values based on the earlier dynamics determined using classical methods such as Trotterization. 

It is important to note that a well established solution already exists, linear prediction. This method works reasonably well, but its weakness is that it relies on solving a least squares problem on one correlation function, meaning its precision is limited. A neural network possesses the advantage of learning accross Ising chains with different parameters, thus being able to potentially reach a higher precision. Therefore, linear prediction was used as the benchmark for determining the validity of using TCN's for this task. 

The Notebook pipeline.ipynb goes through everything, from data generation to training to testing. 

I used the Tenpy library created by Dr. Johannes Hauschild and Prof. Frank Pollmann.

The source code for the TCN architecture can be found at https://github.com/locuslab/TCN

For more details on the thesis and tests performed, see my thesis.

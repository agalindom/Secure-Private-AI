# Overview
The repository contains two notebooks that use federated deep learning

# Description
Both notebooks are trained on the MNIST digits dataset

- The first contains a simple federated deep learning model, where the data is distributed between different workers, each of them then trains a different model separately to later send their raw gradients to a secure worker sum them up and send them back to the central server.

- The second also contains a federated deep learning model, but this time when sending the raw gradients to a secure worker, secret sharing and fixed precision are applied, the former encrypts the original values to large integers to ensure that no information is being revealed regarding the raw gradients and the latter, because in the context of federated learning we work with decimal numbers, fixed precision encodes the decimal numbers to integers to then apply secret sharing on them.

# Files
Federated-Learning.ipynb

Secure-Federated.ipynb

# Libraries
  * PyTorch
  * PySyft
  * Numpy

# PySyft Installation
  - For the installation of the package go to https://github.com/OpenMined/PySyft and inside the README file you can find all the steps to successfully install PySyft and also several examples on how to use it. 

# Results
  - For the first notebook, the test accuracy after 30 epochs of training was of **0.928** and for the second one the test accuracy after 40 epochs was of **0.9342**

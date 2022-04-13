# Approximate quantum state initialization

The goal of this project is to study existing techniques of optimal quantum state initilization, and propose a method, which will dramatically reduce the number of 2-qubit gates. This will lead to a smaller ciruit depth, hense less errors, and (which is also important) cost of pay-as-you-go plans of quantum computers. We will exchance accuracy for money!


My idea is to start thinking about vector, matrix, and tensor de different decomposition techniques. The extereme goal is to obtain for a desired state $|\Psi\rangle$: $\bigotimes_{i=0}^{N}|\psi_i\rangle\approx|\Psi\rangle$. Approximation can be done with respect to some criterion, which meets the problem, e.g. cosine similarity, smallest number or affected amplitudes, etc.

In [related works](related.md) we discuss the works which can help us to understand the methods.
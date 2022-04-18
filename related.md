# Relates works

## Optimal initialization

- 2004 - [Synthesis of Quantum Logic Circuits](https://arxiv.org/abs/quant-ph/0406176). The paper I started with. It introduces the `Multiplexor` operator -- unitary block-diagonal matrix. The extreme case of such matrix is an arbitrary diagonal matrix $\Delta$. Preparation of such matrix is a recursive divide-n-conquer process: we can prepare a diagonal matrix from block-diagonal with $2\times2$ blocks, etc. Knowing this algorithm we can ititialize arbitrary $|\psi\rangle$: prepare equal superposition with Hadamard gates, and then apply $\Delta$. Like this: $|\psi\rangle=\Delta\times\frac{1}{\sqrt{2^N}}\mathbf{1}=\Delta\times H^{\otimes N}\times|0\rangle=diag(\psi)\times H^{\otimes N}\times|0\rangle$. This method is implemented in [Qiskit's initialize()](https://qiskit.org/documentation/stubs/qiskit.circuit.QuantumCircuit.initialize.html). This paper also adds and important idea, that operators $CNOT(a, b)$ and $CNOT(c, b)$ commute, thus we can swap their places; and 2 conseqent equal $CNOT$'s cancel out. For the proposed algorithm this helps to reduce number of $CNOT$'s: $CNOT(a, b)-CNOT(c, b)-CNOT(a, b)$ gate sequence (which appears when a state vector has 2 equal consequent values) is equivalent to just $CNOT(c, b)$.
```
@article{shende2006synthesis,
  title={Synthesis of quantum-logic circuits},
  author={Shende, Vivek V and Bullock, Stephen S and Markov, Igor L},
  journal={IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems},
  volume={25},
  number={6},
  pages={1000--1010},
  year={2006},
  publisher={IEEE}
}
```

- 2001 - [Efficient scheme for initializing a quantum register with an arbitrary superposed state](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.64.014303)
- 2004 - [Optimal quantum circuit synthesis from controlled-unitary gates](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.69.042309)
- 2004 - [Transformation of quantum states using uniformly controlled rotations](https://arxiv.org/abs/quant-ph/0407010)
- 2008 - [Quantum Circuit Simplification and Level Compaction](https://ieeexplore.ieee.org/abstract/document/4378213)
- 2010 - [Synthesis of quantum circuits for linear nearest neighbor architectures](https://link.springer.com/article/10.1007/s11128-010-0201-2)
- 2013 - [A Meet-in-the-Middle Algorithm for Fast Synthesis of Depth-Optimal Quantum Circuits](https://ieeexplore.ieee.org/abstract/document/6516700)
- 2014 - [Efficient synthesis of quantum circuits implementing clifford group operations](https://ieeexplore.ieee.org/abstract/document/6742938)
- 2016 - [Parallelizing quantum circuit synthesis](https://iopscience.iop.org/article/10.1088/2058-9565/1/1/015003/meta)
- 2020 - [A divide-and-conquer algorithm for quantum state preparation](https://arxiv.org/abs/2008.01511)
- 2021 - [Deterministic, scalable, and entanglement efficient initialization of arbitrary quantum states](https://arxiv.org/abs/2110.13454)
- 2021 - [Configurable sublinear circuits for quantum state preparation](https://arxiv.org/abs/2108.10182)
- 2021 - [Entanglement as a complexity measure for quantum state preparation](https://arxiv.org/abs/2111.03132)

## Circuit compression

- 2020 [Graph-theoretic Simplification of Quantum Circuits with the ZX-calculus](https://quantum-journal.org/papers/q-2020-06-04-279/)
```
@article{2020, 
    title={Graph-theoretic Simplification of Quantum Circuits with the ZX-calculus}, 
    volume={4}, ISSN={2521-327X}, 
    url={http://dx.doi.org/10.22331/q-2020-06-04-279}, DOI={10.22331/q-2020-06-04-279}, 
    journal={Quantum}, 
    publisher={Verein zur Forderung des Open Access Publizierens in den Quantenwissenschaften}, 
    author={Duncan, Ross and Kissinger, Aleks and Perdrix, Simon and van de Wetering, John}, 
    year={2020}, 
    month={Jun}, 
    pages={279} 
}
```
- https://www.quantinuum.com/developers/tket
- 2020 - [ZX-calculus for the working quantum computer scientist](https://arxiv.org/abs/2012.13966)
```
@misc{https://doi.org/10.48550/arxiv.2012.13966,
  doi = {10.48550/ARXIV.2012.13966},
  url = {https://arxiv.org/abs/2012.13966},
  author = {van de Wetering, John},
  keywords = {Quantum Physics (quant-ph), FOS: Physical sciences, FOS: Physical sciences},
  title = {ZX-calculus for the working quantum computer scientist},
  publisher = {arXiv},
  year = {2020},  
  copyright = {arXiv.org perpetual, non-exclusive license}
}
```
- https://zxcalculus.com/


## Decomposition
My idea is to start thinking about vector, matrix, and tensor de different decomposition techniques. The extereme goal is to obtain for a desired state $|\Psi\rangle$: $\bigotimes_{i=0}^{N}|\psi_i\rangle\approx|\Psi\rangle$. Approximation can be done with respect to some criterion, which meets the problem, e.g. cosine similarity, smallest number or affected amplitudes, etc. 

- 2010 - [Hierarchical Singular Value Decomposition of Tensors](https://epubs.siam.org/doi/abs/10.1137/090764189). 
```
@article{doi:10.1137/090764189,
author = {Grasedyck, Lars},
title = {Hierarchical Singular Value Decomposition of Tensors},
journal = {SIAM Journal on Matrix Analysis and Applications},
volume = {31},
number = {4},
pages = {2029-2054},
year = {2010},
doi = {10.1137/090764189},
URL = {https://doi.org/10.1137/090764189}
}
```
- Proposed authors: *Ivan Oseledets, Alexander Novikov, Roman Schutski, Maxim, Rahuba, Valentin Khrulkov.*
- [Python reference](https://stackoverflow.com/questions/66753122/specific-tensor-decomposition)
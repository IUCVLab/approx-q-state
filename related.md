# Relates works

## Recommended papers
<details>
<summary>papers proposed by Skoltech (to sort)</summary>

- 2020 - [Randomized algorithms for fast computation of low rank tensor ring model](https://iopscience.iop.org/article/10.1088/2632-2153/abad87/meta)
  <details>
  <summary>bibtex</summary>

  ```
  @article{Ahmadi_Asl_2020,
    doi = {10.1088/2632-2153/abad87},
    url = {https://doi.org/10.1088/2632-2153/abad87},
    year = 2020,
    month = {dec},
    publisher = {{IOP} Publishing},
    volume = {2},
    number = {1},
    pages = {011001},
    author = {Salman Ahmadi-Asl and Andrzej Cichocki and Anh Huy Phan and Maame G Asante-Mensah and Mirfarid Musavian Ghazani and Toshihisa Tanaka and Ivan Oseledets},
    title = {Randomized algorithms for fast computation of low rank tensor ring model},
    journal = {Machine Learning: Science and Technology}
  }
  ```
  </details>

- 2022 - [How to Train Unstable Looped Tensor Network](https://arxiv.org/abs/2203.02617)

- 2022 - [TTOpt: A Maximum Volume Quantized Tensor Train-based Optimization and its Application to Reinforcement Learning](https://arxiv.org/abs/2205.00293)
  <details>
  <summary>bibtex</summary>

  ```
  @misc{TTOps,
    doi = {10.48550/ARXIV.2205.00293},
    url = {https://arxiv.org/abs/2205.00293},
    author = {Sozykin, Konstantin and Chertkov, Andrei and Schutski, Roman and Phan, Anh-Huy and Cichocki, Andrzej and Oseledets, Ivan},
    keywords = {Machine Learning (cs.LG), Neural and Evolutionary Computing (cs.NE), Optimization and Control (math.OC), FOS: Computer and information sciences, FOS: Computer and information sciences, FOS: Mathematics, FOS: Mathematics},
  ```
  </details>


</details>


## Optimal initialization

- 2004 - [Synthesis of Quantum Logic Circuits](https://arxiv.org/abs/quant-ph/0406176). The paper I started with. It introduces the `Multiplexor` operator -- unitary block-diagonal matrix. The extreme case of such matrix is an arbitrary diagonal matrix $\Delta$. Preparation of such matrix is a recursive divide-n-conquer process: we can prepare a diagonal matrix from block-diagonal with $2\times2$ blocks, etc. Knowing this algorithm we can ititialize arbitrary $|\psi\rangle$: prepare equal superposition with Hadamard gates, and then apply $\Delta$. Like this: $|\psi\rangle=\Delta\times\frac{1}{\sqrt{2^N}}\mathbf{1}=\Delta\times H^{\otimes N}\times|0\rangle=diag(\psi)\times H^{\otimes N}\times|0\rangle$. This method is implemented in [Qiskit's initialize()](https://qiskit.org/documentation/stubs/qiskit.circuit.QuantumCircuit.initialize.html). This paper also adds and important idea, that operators $CNOT(a, b)$ and $CNOT(c, b)$ commute, thus we can swap their places; and 2 conseqent equal $CNOT$'s cancel out. For the proposed algorithm this helps to reduce number of $CNOT$'s: $CNOT(a, b)-CNOT(c, b)-CNOT(a, b)$ gate sequence (which appears when a state vector has 2 equal consequent values) is equivalent to just $CNOT(c, b)$.
  <details>
  <summary>bibtex</summary>

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
  </details>

<details><summary>Not read yet</summary>

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
- 2022 - [QUEST: systematically approximating Quantum circuits for higher output fidelity](https://dl.acm.org/doi/10.1145/3503222.3507739)
- 2022 - [Best Approximate Quantum Compiling Problems](https://dl.acm.org/doi/10.1145/3505181)
</details>

## Circuit compression

<details><summary> Not read yet </summary>

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

</details>

## On Decomposition
The idea is to start thinking about vector, matrix, and tensor decomposition techniques. The extereme goal is to obtain for a desired state $|\Psi\rangle$: $\bigotimes_{i=0}^{N}|\psi_i\rangle\approx|\Psi\rangle$. Approximation can be done with respect to **some criterion**, which meets the problem, e.g. cosine similarity, smallest number or affected amplitudes, etc. Today Tensor Decompositions propose a numerous methods, which we can study accoss the problem of gate minimization and noise introduction.

- 2009 - [Typicality in random matrix product states](https://arxiv.org/abs/0908.3877).
This paper links 2 concepts: [matrix product states](https://en.wikipedia.org/wiki/Matrix_product_state) (which is how physics call TT, this shows that all **legal quantum states** can be prepated with a *sequence of unitary transformations packed in tensors*), and **typicality**. Typicality is the thing which is a physical implementation on [concentration of measure phenomenon](https://en.wikipedia.org/wiki/Concentration_of_measure). What they show - there is typicality observed with even linear growth of a single particle space dimensionality ($\chi$. In other words, there is an interesting structure found in valid quantum states which can have and observation in statistical physics. What I learned from here (maybe wrong). If there is independency, tensor matrices of one "site" (i.e. corresponding to 1 qubit) will be equal. (See page 1 phrase: *For homogeneous MPS the set $\{A^1[s],A^2[s], ... , A^D[s]\}$ is the same for all sites $s$*).
  <details>
  <summary>bibtex</summary>

  ```
  @article{PhysRevA.81.032336,
  title = {Typicality in random matrix product states},
  author = {Garnerone, Silvano and de Oliveira, Thiago R. and Zanardi, Paolo},
  journal = {Phys. Rev. A},
  volume = {81},
  issue = {3},
  pages = {032336},
  numpages = {8},
  year = {2010},
  month = {Mar},
  publisher = {American Physical Society},
  doi = {10.1103/PhysRevA.81.032336},
  url = {https://link.aps.org/doi/10.1103/PhysRevA.81.032336}
  }
  ```
  </details>

- 2010 - [Statistical properties of random matrix product states](https://arxiv.org/abs/1003.5253). Another paper of the same team which studied better numerical properties of the same object: randomily generated matrices to restore a big unitary. Again typicality (concentration-of-measure) meets MPS for modelling complex objects of statistical physics. Additional observations: I already faced concentration-of-measure in my NSW experiments, where higher dimension vectors crouded around class boundary. In simple words CoM is when a multidimensional function tend to be almost constant in value if parameter changes. E.g. random point pair distance on a multidimensional sphere is almost always $\frac{\pi}{2}$.
  <details>
  <summary>bibtex</summary>

  ```
  @article{PhysRevA.82.052312,
    title = {Statistical properties of random matrix product states},
    author = {Garnerone, Silvano and de Oliveira, Thiago R. and Haas, Stephan and Zanardi, Paolo},
    journal = {Phys. Rev. A},
    volume = {82},
    issue = {5},
    pages = {052312},
    numpages = {11},
    year = {2010},
    month = {Nov},
    publisher = {American Physical Society},
    doi = {10.1103/PhysRevA.82.052312},
    url = {https://link.aps.org/doi/10.1103/PhysRevA.82.052312}
  }
  ```

  </details>

- 2012 - [Matrix Product States, Random Matrix Theory and the Principle of Maximum Entropy](https://arxiv.org/abs/1201.6324). The work is kind of another general view on "can we use MPS for more efficient simulations". Here they explore maximum Entropy principle, which states that in nature the most probable dustributions are those which maximize entropy (in this paper von Neuman's entropy). Major theorem of the paper proves that if $D\geq N^5$ then whatever we generate with RMPS is almost indistiguishable from straighforward behavior (max entropy is equal observation of states denoted as $\mathbf{1}/d^l$). Also from this paper I learned (figure 1) what is spin chain. And local interations are important, as they are enough (which we observe when implement very distant CNOT). And in the end, again, emphasis is on "with MPS we generate maximum entropy, thus this is natural".
  <details>
  <summary>bibtex</summary>

  ```
  @article{2013, 
    title={Matrix Product States, Random Matrix Theory and the Principle of Maximum Entropy}, 
    volume={320}, 
    ISSN={1432-0916}, 
    url={http://dx.doi.org/10.1007/s00220-013-1718-x}, 
    DOI={10.1007/s00220-013-1718-x}, 
    number={3}, 
    journal={Communications in Mathematical Physics}, 
    publisher={Springer Science and Business Media LLC},  
    author={Collins, Beno??t and Gonz??lez-Guill??n, Carlos E. and P??rez-Garc??a, David}, year={2013}, month={May}, 
    pages={663???677} }
  ```
  </details>


- 2010 - [Hierarchical Singular Value Decomposition of Tensors](https://epubs.siam.org/doi/abs/10.1137/090764189). Tensor can be considered as a multivariate function on a grid, this is what the paper start from. Each grid dimension is called a *mode*. Few dimensions grouped together - *mode cluster*. Let us start with [Tucker decomposition](https://en.wikipedia.org/wiki/Tucker_decomposition). It decomposes a tensor into a set of matrices $M_i$ (same as the munber of modes) and one (small) core tensor $C$: $A=(M_1, M_2, ..., M_d)\circ C$. It generalizes to [HOSVD](https://en.wikipedia.org/wiki/Higher-order_singular_value_decomposition). The core idea of the paper is **matricization** -- rolling the tensor into 2 dimensions, where it can be processed with matrix operations. Matricization is done in 2 ways. First, with a "singleton" (single mode in a set) -- one tensor dimension (mode) is chosen, others are flattened into the second dimension. Second - one *mode cluster* becomes a dimension, while its complement becomes another. Having a matrix, we can do (1) multiplication (2) SVD. Doing an SVD for a binary hierarchy of the mode clusters (starting from the full set and up to singletons) is the core idea of the methods. Single step looks like this: we prepare a matrix $A^{(t)}$ (sigleton matricization) for a tensor $A$ and do an $SVD(A^{(t)})=U\Sigma V^T$. We reduce $U$ up to the rank, or even further. If we do it for each mode, we will end up with $d$ matrices $U^{(R)}_i$. And then we can use $T=(U^{(R)T}_1, U^{(R)T}_2, ..., U^{(R)T}_d)\circ A$ to reduce size, and $\tilde{A} = (U^{(R)}_1, U^{(R)}_2, ..., U^{(R)}_d)\circ T$ to restore it back. Basically, we remain with the same number of modes (variables) between $A$ and core tensor $T$, but we reduce the grid size. The remaining part of the paper is devoted to a better approximation method. The shown reduction technique is used as a starting point, but further it is improved with some magic.

  <details>
  <summary>bibtex</summary>

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
  </details>

- 2015 - [Alternating Least Squares Tensor Completion in The TT-Format](https://arxiv.org/abs/1509.00311).
  <details>
  <summary>bibtex</summary>

  ```
  @misc{ALSTT,
    doi = {10.48550/ARXIV.1509.00311},
    url = {https://arxiv.org/abs/1509.00311},
    author = {Grasedyck, Lars and Kluge, Melanie and Kr??mer, Sebastian},
    keywords = {Numerical Analysis (math.NA), FOS: Mathematics, FOS: Mathematics, 15A69, 65F99},
    title = {Alternating Least Squares Tensor Completion in The TT-Format},
    publisher = {arXiv},
    year = {2015}, 
    copyright = {arXiv.org perpetual, non-exclusive license}
  }
  ```
  </details>

- 2022 - [Approximated quantum-state preparation with entanglement dependent complexity](https://arxiv.org/abs/2111.03132).  The most disappoiniting paper ever. This paper actually implements almost all ideas I just wanted to explore. To be short, they propose to control the fidelity loss by accurately finding the least entangled subsystems and cutting them with SVD. Mathematically this is equivaluent to my proposed excercises with Tucker decomposition. Still, there are some learning outcomes (and one place for improvement). They use their initialization on [this method (Plesch, 2010)](https://arxiv.org/abs/1003.5760) which is asymptotically exponential, but a little better in constants compared to the one in Qiskit. They address the problem of measuring the entanglement, which include: *"Schmidt rank"* -- the number of non-0 Schmidt coefficients in decomposition. And *"measure of entanglement [(def)](https://arxiv.org/abs/quant-ph/0103155)"* which is basically the $L_2$ distance to the best fully disentangled approximation (product state). Authors take this idea to build a tree, where each branching corresponds to the optimal qubits bi-partitioning with respect to this "measure of entanglement". So, traversing the tree we can obtain the best theoretical approximation **with a controlled loss**, and save some CNOTs. Finally they show, that they do better in practice with these approximation, than with accurate initialization. Weak place here -- exponentially hard problem of optimal qubit bi-partitioning. They tried to address it with greedy method, but the method was not that successful. 

  **Other takeways**: 
  
  [This method (page 2)](https://arxiv.org/abs/quant-ph/0307219) uses black magic math to find optimal product state approximation with *nonlinear eigen-problem*. In [this paper](https://www.mdpi.com/1099-4300/17/7/5063/htm) authors use tensor decomposition for approximation, in particular PARAFAC ([Parallel Factor Decomposition](http://mlsp.cs.cmu.edu/courses/fall2013/lectures/Parafac.pdf)) to represent a tensor as a sum of rank-1 tensors, but they limit their observations with 4 qubits and 3 qudits. [This paper (2016)](https://arxiv.org/abs/1609.02076) uses Tucker decomposition with ALS (which I plan to use) to estimate (successfully) the entanglement without solving minimization problem. Other methods listed to be compared are based on trainable circuits -- [AAS](https://arxiv.org/abs/2103.13211) and [qGANs](https://www.nature.com/articles/s41534-019-0223-2). 
  
  [Barren plateau](https://www.lanl.gov/discover/news-release-archive/2021/March/0319-barren-plateaus.php) is a flat search space in optimization problems.
  
  [Adiabatic theorem](https://en.wikipedia.org/wiki/Adiabatic_theorem) - slow change in Hamiltonian for a system in te eigenstate will result in corresponding evolution to the eigenstate of the final Hamiltonian. This is not the same for fast Hamiltonian change.

  **Method implementation** - [QCLIB library](https://github.com/qclib/qclib).

  <details>
  <summary>bibtex</summary>

  ```
  @misc{https://doi.org/10.48550/arxiv.2111.03132,
  doi = {10.48550/ARXIV.2111.03132},
  url = {https://arxiv.org/abs/2111.03132},
  author = {Araujo, Israel F. and Blank, Carsten and da Silva, Adenilton J.},
  keywords = {Quantum Physics (quant-ph), Emerging Technologies (cs.ET), FOS: Physical sciences, FOS: Physical sciences, FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Approximated quantum-state preparation with entanglement dependent complexity},
  publisher = {arXiv},
  year = {2021},
  copyright = {arXiv.org perpetual, non-exclusive license}
  }
  ```
  </details>


### Entanglement forging

- 2021 - On **Entanglement Forging**. [Video explainer](https://www.youtube.com/watch?v=vJZRUf1abQs), [Paper](https://arxiv.org/abs/2104.10220), [Press release](https://research.ibm.com/blog/quantum-entanglement-forging), [CODE](https://github.com/qiskit-community/prototype-entanglement-forging).
  <img src="https://dwzke5c1hcizv.cloudfront.net/image?url=https%3A%2F%2Fresearch-website-prod-cms-uploads.s3.us.cloud-object-storage.appdomain.cloud%2Ffig1_2_N_qubit_circuit_9b7a33a9c4.png&w=1920&q=75">
  Citation: "You can also apply entanglement forging to systems **that aren???t weakly entangled**. We just have to do more computation on the classical computer either to determine how best to partition the system, or **to represent the correlation** between the two halves".
  My note: with this explanation, the stronger is the entanglement, the longer will be the sequence with $\lambda_i$. Thus we save qubits, but may potentially increase the depth. Which is OPPOSITE to my idea - keeping the number or qubits and reducing the depth. Proof: *"Moreover, there can be a large overhead cost in the number of these measurements that must be taken"*.

  <u>Trade-off</u>: If researchers **don???t know the best places to cut** ahead of time, they???ll likely need to use classical computational methods to **evaluate various cuts** for the expected cost of reassembly, as well as computational resources that can perform reassembly in the cases where it isn???t cheap.

  **What is the method**. Any entangled system $|\psi\rangle$ can be written down in a form of Schmidt decomposition $|\psi\rangle=\sum _{{i=1}}^{m}\lambda _{i}|a_{i}\rangle\otimes |b_{i}\rangle$. $\lambda$'s are referred as Schmidt coefficients. For the systems which is not entangled at all we have only $\lambda_1$, the others $\lambda_{2+}$ are 0s. For the strongly entangled systems we will observe all $\lambda$'s almost equal. Looking at the picture, one can see, that gates $U$ and $V$ are applied independently to sub-registers, thus the final system can be written as $|\psi\rangle=\sum _{{i=1}}^{m}\lambda _{i}(U|a_{i}\rangle\otimes V|b_{i}\rangle)$ -- Schmidt coefficients are not affected! This we can restore the effect of entanglement by collecting back the sum. Profit? We simulate a halved part of the system intead of the whole, thus we need less qubits. Obviously, weak entanglement is well suited for the method, as you need only a few runs (for a small number of Schmidt coefficients). Note well: Schmidt decomposition can be [done using SVD](https://physics.stackexchange.com/a/251574). Doing Schmidt decompolsition [in python](https://pypi.org/project/pyqentangle/).


### Other

- Proposed authors: *Ivan Oseledets, Alexander Novikov, Roman Schutski, Maxim, Rahuba, Valentin Khrulkov.*
- [Python reference](https://stackoverflow.com/questions/66753122/specific-tensor-decomposition)
- [TT implementation](https://github.com/oseledets/ttpy)

## Measurement error mitigation
- 2022 - [Medium post: How To Tackle IBM's Quantum Open Science Prize](https://pyqml.medium.com/how-to-tackle-ibms-quantum-open-science-prize-e6c7fc594154). Targeting the problem of measurement in a 7-qubit Jakarta system. Says "Let us try Error mitigation with Clifford quantum-circuit data", but nothing else. But stores interesting links below.

- 2022 - [Towardsdatascience post: Quantum Measurement Mitigation With Qiskit](https://towardsdatascience.com/quantum-measurement-mitigation-with-qiskit-bb35b3d28eec). Explaining error mitigation in practice. Step 1 - find a ratio of ideal and noise-free values (if count is 30 in noise-free and 105 in noise - 30/105). That us how we find "modifiers" for each measurement outcome. We use the same modifier for next circuit runs. (My note - this is similar technique explained in IonQ recommendations: remove impossible outcomes, but also it rescales other outputs). As the methods is used with *quantum tomography* - i.e. looking at the Bloch sphere from different angles (X, Y, Z angles, or XX, XY ... for 2qubit, ... - $3^n$ in general), we will generate tomography circuits first. And then restore the state based on their measurements. Indeed this is just changes of measurement basis:

  ```
  from qiskit.ignis.verification.tomography import state_tomography_circuits 
  ... 
  circuits = state_tomography_circuits(qc, [1,3,5]) # 27
  ... 
  state = StateTomographyFitter(results, circuits).fit(method='lstsq') # best point to fit 27 projections
  ```
  Modifiers are then computed per tomography circuit. Interesting tool: `from qiskit.opflow import Zero, One`.

- 2016 - [Error mitigation for short-depth quantum circuits](https://arxiv.org/abs/1612.02058)
  <details>
  <summary>bibtex</summary>

  ```
  @article{PhysRevLett.119.180509,
    title = {Error Mitigation for Short-Depth Quantum Circuits},
    author = {Temme, Kristan and Bravyi, Sergey and Gambetta, Jay M.},
    journal = {Phys. Rev. Lett.},
    volume = {119},
    issue = {18},
    pages = {180509},
    numpages = {5},
    year = {2017},
    month = {Nov},
    publisher = {American Physical Society},
    doi = {10.1103/PhysRevLett.119.180509},
    url = {https://link.aps.org/doi/10.1103/PhysRevLett.119.180509}
  }
  ```
  </details>

- 2018 - [Low-cost error mitigation by symmetry verification](https://arxiv.org/abs/1807.10050)
  <details>
  <summary>bibtex</summary>

  ```
  @article{PhysRevA.98.062339,
    title = {Low-cost error mitigation by symmetry verification},
    author = {Bonet-Monroig, X. and Sagastizabal, R. and Singh, M. and O'Brien, T. E.},
    journal = {Phys. Rev. A},
    volume = {98},
    issue = {6},
    pages = {062339},
    numpages = {10},
    year = {2018},
    month = {Dec},
    publisher = {American Physical Society},
    doi = {10.1103/PhysRevA.98.062339},
    url = {https://link.aps.org/doi/10.1103/PhysRevA.98.062339}
  }
  ```
  </details>

- 2021 - [Error mitigation with Clifford quantum-circuit data](https://arxiv.org/abs/2005.10189)
  <details>
  <summary>bibtex</summary>

  ```
  @article{Czarnik2021errormitigation,
    doi = {10.22331/q-2021-11-26-592},
    url = {https://doi.org/10.22331/q-2021-11-26-592},
    title = {Error mitigation with {C}lifford quantum-circuit data},
    author = {Czarnik, Piotr and Arrasmith, Andrew and Coles, Patrick J. and Cincio, Lukasz},
    journal = {{Quantum}},
    issn = {2521-327X},
    publisher = {{Verein zur F{\"{o}}rderung des Open Access Publizierens in den Quantenwissenschaften}},
    volume = {5},
    pages = {592},
    month = nov,
    year = {2021}
  }
  ```
  </details>
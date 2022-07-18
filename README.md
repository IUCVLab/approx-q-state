# Approximate quantum state initialization

The goal of this project is to study existing techniques of optimal quantum state initilization, and propose a method, which will dramatically reduce the number of 2-qubit gates. This will lead to a smaller ciruit depth, hense less errors, and (which is also important) cost of pay-as-you-go plans of quantum computers. We will exchance accuracy for money!


My idea is to start thinking about vector, matrix, and tensor de different decomposition techniques. The extereme goal is to obtain for a desired state $|\Psi\rangle$: $\bigotimes_{i=0}^{N}|\psi_i\rangle\approx|\Psi\rangle$. Approximation can be done with respect to some criterion, which meets the problem, e.g. cosine similarity, smallest number or affected amplitudes, etc.

In [related works](related.md) we discuss the works which can help us to understand the methods. Basically, a lot of work in this direction was already done.

## Results

Current result includes the study of the Tucker decomposition as the tool to search for low entanglement. I improved the speed of single-qubit entanglement assessment method in terms of speed and memory. Results are:
- [Published here](https://www.researchgate.net/publication/361993275_Tucker_Tensor_Decomposition_of_a_Quantum_State_for_Entanglement_Analysis?_sg%5B0%5D=z9pmpxvs2KVqj1nNZUfS7wk-2x59nC3ZXPn_pD8vpc8Rk9W2XLvzrmC-rfUXfsbJyurI521bnwbFf8qycvRv5ZmF7WiVRLyFGjAi-s5N.-hvYTVzf5wDenuD9Gh0MGwoxaVwU6A38ARA4qWYBBWkm2BahelblroBr7Ivq6y_Uwyw56n7z5GJZp9pdVwNp4A).
- [Experimentally assessed here](playground/10 method speed assessment.ipynb).

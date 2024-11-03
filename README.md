# Enhanced-Deutsch-Jozsa-Algorithm-with-Multi-Qubit-Balanced-Functions
The Deutsch-Jozsa algorithm is a quantum algorithm that can efficiently determine whether a function is constant (same output for all inputs) or balanced (outputs 0 for half of the inputs and 1 for the other half). In classical computing, this determination requires multiple evaluations, but quantum computing can do it in a single run. We'll create the Deutsch-Jozsa circuit to evaluate multi-qubit functions.

This Enhanced Deutsch-Jozsa Algorithm Simulation project in Qiskit demonstrates the power of quantum algorithms to distinguish between constant and balanced functions with high efficiency.

Objective: Use the Deutsch-Jozsa algorithm to determine if a multi-qubit function is constant (same output for all inputs) or balanced (outputs are split evenly between 0 and 1), achieving this in a single evaluation—a feat that requires multiple attempts classically.

Input Preparation: Initialize n input qubits in the |+⟩ state and one ancillary qubit in |−⟩ to store function evaluations.

Oracle Setup: Construct two oracles—one for a constant function, which leaves the ancillary unchanged, and one for a balanced function, which flips the ancillary based on input.

Measurement: Apply a final Hadamard transformation and measure the input qubits. A result of all 0s indicates a constant function, while any non-zero result indicates a   balanced function.

Implementation: The Sampler primitive replaces the deprecated execute function, providing quasi-probability distributions to identify outcomes. The code tests both the constant and balanced oracles, interpreting the results based on observed measurement patterns.

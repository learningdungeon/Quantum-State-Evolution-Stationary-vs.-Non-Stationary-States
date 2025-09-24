# Quantum-State-Evolution-Stationary-vs.-Non-Stationary-States
Fundamental difference between stationary and non-stationary quantum states through simulation using the Qiskit SDK. By simulating the time evolution of a qubit under a Hamiltonian, we observe how the measurement probabilities of a stationary state remain constant, while those of a non-stationary state oscillate over time.  

**Core Concepts
**1. Stationary State:
A stationary state is an eigenstate of the system's Hamiltonian. When a system is in such a state, its observable properties (like the probabilities of measurement in the computational basis) do not change over time.
In this project, we start with the ∣0⟩ state, which is an eigenstate of the Pauli-Z Hamiltonian. Its time evolution is described by:
∣ψ(t)⟩=e 
−iHt
 ∣0⟩=e 
−iλ_0t
 ∣0⟩
where H is the Hamiltonian and λ_0 is its corresponding eigenvalue. As you can see, the state only acquires a global phase, leaving the measurement probabilities unchanged.

**2. Non-Stationary State:**

A non-stationary state is a superposition of two or more eigenstates of the Hamiltonian. When such a state evolves over time, the relative phases of its components change, causing the probabilities of measurement to oscillate.
In this project, we start with the ∣+⟩ state, which is a superposition of ∣0⟩ and ∣1⟩

The time evolution of this state under the Pauli-Z Hamiltonian will cause its measurement probabilities in the X-basis to oscillate.

**Code and Simulation**

The project is structured into three parts:

**Stationary State Simulation:** We initialize a qubit in the ∣0⟩ state and repeatedly apply a time-evolution operator (R_z gate) to simulate the passage of time. We collect the statevector at each step and plot the probabilities of measuring ∣0⟩ and ∣1⟩.

**Non-Stationary State Simulation:** We initialize a qubit in the ∣+⟩ state (by applying a Hadamard gate to ∣0⟩). We then apply the same time-evolution operator. To observe the oscillations, we apply a second Hadamard gate before measuring, which rotates the basis and allows the changing probabilities to be seen in the standard computational basis.

**Visualization:** The probabilities from both simulations are plotted to visually compare the constant nature of the stationary state against the oscillatory behavior of the non-stationary state.

**About the Author**

This project was created by me(Noor), a passionate quantum computing enthusiast and Qiskit advocate.  
This project is part of her ongoing research into quantum noise mitigation strategies and my commitment to the "quantum curriculum for all" project I am mentoring.









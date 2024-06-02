# VQE

## Hamiltonian

### Potential Energy

The potential energy of a system of electrons and nuclei arises from the electrostatic interactions between the charged particles. There are 3 components, electron-electron repulsion, nuclear-nuclear repulsion, and electron-nuclear attraction. Coulomb's law $V = \frac{q_1q_2}{4\pi\epsilon_0 r}$ can be used to calculate their potential energy:

$$ \hat{V} = \underbrace{\sum_{i,j}^{\text{electrons}} \frac{e^2}{4\pi\epsilon_0 |r_i - r_j|}}_{\text{electron-electron repulsion}} + \underbrace{\sum_{i,j}^{\text{nuclei}} \frac{Z_i Z_j e^2}{4\pi\epsilon_0 |R_i - R_j|}}_{\text{nuclear-nuclear repulsion}} - \underbrace{\sum_{i}^{\text{electrons}} \sum_{j}^{\text{nuclei}} \frac{Z_j e^2}{4\pi\epsilon_0 |r_i - R_j|}}_{\text{electron-nuclear attraction}} $$

### Kinetic Energy

Since classically, $T_x = \frac{P_x^2}{2m}$, and the quantum momentum operator $\hat{P}_x = -i\hbar\frac{\partial}{\partial x}$, so

$$ \hat{T}_x = \frac{\hat{P}_x^2}{2m} = -\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2} $$

If the particle is moving in 3 dimensions, then $P = \vec{x}P_x + \vec{y}P_y + \vec{z}P_z$ and the total momentum operator would be

$$ \hat{P} = -i\hbar(\vec{x}\frac{\partial}{\partial x} + \vec{y}\frac{\partial}{\partial y} + \vec{z}\frac{\partial}{\partial z}) = -i\hbar\nabla$$

$$ \therefore \hat{T} = -\frac{\hbar^2}{2m} \nabla^2 $$

The kinetic energy of the system is divided into kinetic energy of the nuclei and the electrons.

$$ \hat{T} = -\sum_{i}^{\text{nuclei}} \frac{\hbar^2}{2m_i} \nabla_i^2 - \sum_{i}^{\text{electrons}} \frac{\hbar^2}{2m_e} \nabla_i^2 $$

### Simplified Molecular Hamiltonian

Several approximations are made to simplify the molecular Hamiltonian:

$$ \hat{H} \approx -\sum_{i}^{\text{electrons}} \frac{1}{2} \nabla_i^2 + \sum_{i,j}^{\text{electrons}} \frac{1}{|r_i - r_j|} - \sum_{i}^{\text{electrons}} \sum_{j}^{\text{nuclei}} \frac{Z_j}{|r_i - R_j|} + C'_n $$

1. **Born-Oppenheimer Approximation**: This approximation assumes that the nuclei are much heavier than the electrons and can be treated as fixed in space. This allows separating the electronic and nuclear motions, effectively removing the kinetic energy term for the nuclei.

2. **Atomic Units**: By using a system of units where certain fundamental constants (such as the Planck constant $\hbar$, the electron mass $m_e$, and the electron charge $e$) are set to 1, the equations can be simplified.

3. **Constant Term**: The term $C'_n$ is a constant that accounts for the nuclear-nuclear repulsion energy, as the positions of the nuclei are considered fixed in this approximation.

The simplified Hamiltonian includes the electronic kinetic energy term, the electron-electron repulsion term, and the electron-nuclear attraction term.

Sure, let me first explain spin-orbital basis functions, and then continue with equations 16, 17, and the Jordan-Wigner transform (equation 18).

## Second Quantization

### Spin-Orbital Basis Functions

In quantum chemistry, wavefunctions are often represented using spin-orbital basis functions, which are products of spatial orbitals and spin functions. These basis functions are used to construct the many-electron wavefunction as a linear combination.

Spin-orbital basis functions are typically denoted as $\psi_p$, $\psi_q$, $\psi_r$, $\psi_s$, and so on. Each spin-orbital function is a product of a spatial orbital $\phi_p(r)$ and a spin function $\alpha(\omega)$ or $\beta(\omega)$, representing the spin up or spin down state, respectively:

$$\psi_p(x) = \phi_p(r) \alpha(\omega)$$
$$\psi_q(x) = \phi_q(r) \beta(\omega)$$

The spatial orbitals $\phi_p(r)$ and $\phi_q(r)$ are typically constructed as linear combinations of atomic orbitals (LCAO) centered on the nuclei. Common basis sets used in quantum chemistry include Slater-type orbitals (STOs) and Gaussian-type orbitals (GTOs).

These spin-orbital basis functions form the basis set in which the molecular orbitals and Hamiltonian are represented.

### One-Electron Part

In quantum chemistry, it is often convenient to express the Hamiltonian and wavefunctions in a second quantized form, which involves creation and annihilation operators acting on spin-orbital basis functions.

In this equation:

$$ \sum_i h_1(x_i) = \sum_{p,q} \langle p | \hat{h}_1 | q \rangle a^\dagger_p a_q $$

- $a^\dagger_p$ and $a_q$ are the creation and annihilation operators, respectively, which create or annihilate an electron in the spin-orbital basis function $ψ_p$ or $ψ_q$.
- $h_{pq} = \langle p | \hat{h}_1 | q \rangle$ represents the one-electron integrals, obtained by integrating the one-electron part of the Hamiltonian ($\hat{h}_1$) over the spin-orbital basis functions $ψ_p$ and $ψ_q$.

This second quantized form provides a compact way to represent the one-electron part of the Hamiltonian, including both the kinetic energy and the electron-nuclear attraction terms, in terms of creation and annihilation operators acting on the spin-orbital basis.

By expressing the Hamiltonian in this form, it becomes easier to perform calculations and manipulations using the tools of second quantization, which are particularly useful in quantum chemistry and condensed matter physics.

### Two-Electron Part

Building on equation 15, which represents the one-electron part of the Hamiltonian in second quantized form, equation 16 introduces the two-electron part:

$$\sum_{i,j} h_2(x_i, x_j) = \sum_{p,q,r,s} \langle pq | \hat{H} | rs \rangle a^\dagger_p a^\dagger_q a_r a_s$$

Here, the two-electron integrals $\langle pq | \hat{H} | rs \rangle$ represent the electron-electron repulsion term, integrated over the spin-orbital basis functions $\psi_p$, $\psi_q$, $\psi_r$, and $\psi_s$.

The creation and annihilation operators $a^\dagger_p$, $a^\dagger_q$, $a_r$, and $a_s$ act on the spin-orbital basis functions to create or annihilate electrons in the corresponding orbitals.

This equation captures the contribution of the electron-electron repulsion term to the Hamiltonian in the second quantized form, allowing for efficient calculations and manipulations.

### Full Molecular Hamiltonian

Equation 17 combines the one-electron and two-electron parts from equations 15 and 16, along with a constant term $h_0$, to give the full molecular Hamiltonian in second quantized form:

$$\hat{H} = \sum_{p,q} h_{pq} a^\dagger_p a_q + \frac{1}{2} \sum_{p,q,r,s} h_{pqrs} a^\dagger_p a^\dagger_q a_r a_s + h_0$$

The first term represents the one-electron part, the second term represents the two-electron part, and $h_0$ is a constant shift factor that accounts for the nuclear-nuclear repulsion energy and any other constant shift needed to align with the desired reference energy.

This equation provides a compact representation of the full molecular Hamiltonian in second quantized form, expressed in terms of creation and annihilation operators acting on the spin-orbital basis functions.

## Simulation

### Jordan-Wigner Transform

The Jordan-Wigner (JW) transform is a mathematical technique used to map the fermionic creation and annihilation operators in second quantization onto a system of spin operators, enabling their representation on a quantum computer using qubit states.

The JW transform maps the fermionic operators as follows:

$$a^\dagger_n \rightarrow \frac{1}{2} \left(\prod_{j=0}^{n-1} -Z_j\right) (X_n - iY_n)$$
$$a_n \rightarrow \frac{1}{2} \left(\prod_{j=0}^{n-1} -Z_j\right) (X_n + iY_n)$$

Here, $X_n$, $Y_n$, and $Z_n$ are the Pauli spin operators acting on the n-th qubit, and the product $\prod_{j=0}^{n-1} -Z_j$ introduces a phase factor to account for the fermionic anti-commutation relations.

The JW transform provides a way to map the fermionic operators onto a system of qubits, enabling the simulation of fermionic systems, such as molecules, on a quantum computer. However, it has some limitations, such as the non-local nature of the operator representations, which can limit scalability for larger systems.

By applying the JW transform to the second quantized Hamiltonian (equation 17), the molecular Hamiltonian can be expressed as a linear combination of tensor products of Pauli operators acting on the qubit states, as shown in equation 22 of the paper for the hydrogen molecule example.

This mapping is a crucial step in performing quantum simulations of molecular systems on quantum computers using algorithms like the Variational Quantum Eigensolver (VQE).

### Slater Determinant

In computational physics and quantum chemistry, the wavefunction of a many-electron system is often expressed as a Slater determinant:

$$\psi(x_1, x_2, \dots, x_n) = \frac{1}{\sqrt{N!}} \begin{vmatrix}
\chi_i(x_1) & \chi_j(x_1) & \dots & \chi_k(x_1) \\
\chi_i(x_2) & \chi_j(x_2) & \dots & \chi_k(x_2) \\
\vdots & \vdots & \ddots & \vdots \\
\chi_i(x_n) & \chi_j(x_n) & \dots & \chi_k(x_n)
\end{vmatrix}$$

Here, $\chi_i$, $\chi_j$, $\chi_k$ are the molecular spin-orbitals, and $x_i$ represents the spatial and spin coordinates of the $i$-th electron. The $1/\sqrt{N!}$ factor is a normalization constant.

The Slater determinant form ensures that the wavefunction is antisymmetric with respect to the interchange of any two electrons, satisfying the Pauli exclusion principle for fermions.

### Occupation Number Representation

While the Slater determinant form is useful for theoretical calculations, it is often more convenient to represent the wavefunction in an occupation number representation for computational purposes:

$$|\psi\rangle = \sum_i C_i |n_1 n_2 \dots n_m\rangle$$

In this representation, $n_i$ is the occupation number (either 0 or 1) indicating whether an electron is present or absent in the $i$-th spin-orbital. The coefficients $C_i$ are the amplitudes of each occupation number configuration.

This occupation number representation provides a compact way to express the many-electron wavefunction as a linear combination of Slater determinants, where each configuration represents a specific occupation pattern of the spin-orbitals.

### Simulating Molecular Systems on Quantum Computers

To simulate molecular systems on quantum computers, we need to map the fermionic operators and wavefunctions onto a system of qubits. This is achieved through techniques like the Jordan-Wigner transform (equation 18), which maps the creation and annihilation operators onto products of Pauli operators acting on qubits.

The Variational Quantum Eigensolver (VQE) algorithm provides a way to leverage this mapping and compute the ground-state energy of a molecular system on a quantum computer.

The key steps in the VQE algorithm are:

1. **Prepare an Ansatz Wavefunction**: We start with an initial trial wavefunction, called an Ansatz, which is a parameterized quantum circuit acting on the qubit register. This Ansatz is designed to be flexible enough to approximate the true ground-state wavefunction of the molecular system.

2. **Encode the Molecular Hamiltonian**: The molecular Hamiltonian, expressed as a linear combination of Pauli operators (e.g., equation 22 for the hydrogen molecule), is encoded onto the quantum computer using appropriate quantum gates.

3. **Measure the Energy Expectation Value**: The quantum computer is used to measure the expectation value of the Hamiltonian with respect to the current Ansatz wavefunction: $\langle\psi(\theta)|\hat{H}|\psi(\theta)\rangle$, where $\theta$ represents the parameters of the Ansatz circuit.

4. **Classical Optimization**: A classical optimization algorithm is used to iteratively update the parameters $\theta$ of the Ansatz circuit, minimizing the energy expectation value measured on the quantum computer. This step is repeated until convergence is achieved.

The key advantage of the VQE algorithm is that it leverages the quantum computer's ability to efficiently represent and manipulate quantum states, while relying on classical optimization techniques to find the optimal parameters for the Ansatz wavefunction.

By variationally minimizing the energy expectation value, the VQE algorithm can approximate the ground-state energy and wavefunction of the molecular system with high accuracy, provided that the Ansatz circuit is expressive enough and the quantum hardware has sufficiently low noise and error rates.

This hybrid quantum-classical approach allows us to tackle computationally challenging problems in quantum chemistry and materials science, paving the way for applications in areas such as drug discovery, catalyst design, and the development of new materials.


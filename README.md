# Quantum Fourier Transform (QFT) Notebook

This repository contains an educational Jupyter notebook exploring the **Quantum Fourier Transform (QFT)**, the quantum analogue of the classical Discrete Fourier Transform (DFT).

---

## Overview

The Quantum Fourier Transform is a key building block in several quantum algorithms, enabling exponential speedups for specific computational problems. This notebook connects classical signal processing concepts with quantum computation, combining mathematical derivations and practical implementation using **Qiskit**.

---

## Contents

* **Introduction**
  From the classical DFT to the Quantum Fourier Transform.

* **Physical Interpretation**
  Understanding the QFT through superposition and rotations on the Bloch sphere, including the intuition of “quantum phase encoding” and Fourier basis states.

* **Mathematical Foundations**

  * Single-qubit case (Hadamard gate equivalence)
  * Extension to n qubits (tensor product structure)
  * Matrix representation of $QFT_N$

* **Circuit Implementation**
  Construction using Hadamard gates and controlled phase rotations ($R_k$ gates).

* **Applications**

  * Shor’s algorithm
  * Quantum phase estimation
  * Period finding problems

* **Code Implementation**
  Qiskit-based implementation of the QFT circuit and visualization of results.

---

## Prerequisites

Install the required dependencies (or use `requirements.txt`):

```bash
pip install qiskit qiskit-aer qiskit-ibm-runtime numpy scipy matplotlib seaborn pandas ipywidgets pylatexenc tqdm "qiskit[visualization]"
```

---

## How to Use

1. Clone this repository.
2. Open `qft_notebook.ipynb` in Jupyter Lab, Jupyter Notebook, or VS Code.
3. Run the notebook sequentially to follow the theoretical development and simulations.

---

## Technologies Used

* Python
* Qiskit (quantum circuit construction and simulation)
* Qiskit Aer (high-performance simulation backend)
* Matplotlib / Seaborn (visualization)

---

## Notes

This project is intended for educational purposes in quantum computing and quantum information theory.

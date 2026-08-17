# Quantum Fourier Transform

An educational and experimental study of the Quantum Fourier Transform (QFT), from its mathematical foundations to ideal, noisy, approximate, simulated, and IBM Quantum executions with Qiskit.

The repository includes English and Italian notebooks, a written report, circuit diagrams, benchmark plots, and reproducible Python dependencies.

## Topics Covered

- the relationship between the classical DFT and the QFT;
- Fourier-basis phase encoding;
- the single-qubit Hadamard case;
- the n-qubit tensor-product formulation;
- matrix representation of QFT;
- manual QFT and inverse-QFT circuit construction;
- approximate QFT through controlled-rotation truncation;
- soundness tests using QFT followed by inverse QFT;
- ideal and noisy Aer simulations;
- comparison with Qiskit's QFT implementation;
- circuit complexity and CPU timing;
- optional execution on IBM Quantum hardware.

## Notebooks

| File | Language | Description |
| --- | --- | --- |
| qft_notebook.ipynb | English | Main theoretical and experimental notebook. |
| qft_notebook_ita.ipynb | Italian | Italian version of the study. |
| QFT_Report.pdf | Italian | Written project report. |

## Requirements

- Python 3;
- Jupyter Notebook, JupyterLab, or VS Code;
- the packages listed in requirements.txt.

Create an isolated environment:

    python3 -m venv .venv
    source .venv/bin/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    pip install jupyter

On Windows PowerShell, activate the environment with:

    .venv\Scripts\Activate.ps1

## Running Locally

Start the English notebook:

    jupyter notebook qft_notebook.ipynb

or the Italian notebook:

    jupyter notebook qft_notebook_ita.ipynb

Run cells in order because later experiments reuse circuits, helper functions, and result tables created earlier.

Aer-based ideal and noisy simulations can be executed without an IBM Quantum account.

## IBM Quantum Execution

The hardware-execution sections use qiskit-ibm-runtime and require valid IBM Quantum credentials. Keep credentials outside version control and load them through environment variables or Qiskit's local account storage.

Do not commit API tokens to .env files or notebook outputs.

Hardware availability, queue times, backend names, and runtime APIs may change. Re-run the transpilation and backend-selection cells against the account currently in use.

## Implemented Experiments

### Correctness

The notebooks compare statevectors and measurement outcomes for:

- manual QFT;
- inverse QFT;
- Qiskit's library implementation;
- QFT followed by inverse QFT.

### Noise

A depolarizing noise model is used with AerSimulator to compare ideal and noisy distributions.

### Approximation

Small controlled-phase rotations can be omitted to reduce circuit depth. The notebooks compare approximation error and resource count as the threshold changes.

### Performance

CPU timings, circuit depth, gate count, and optional QPU execution data are collected to contrast simulation and hardware behaviour.

## Repository Structure

    .
    ├── qft_notebook.ipynb
    ├── qft_notebook_ita.ipynb
    ├── QFT_Report.pdf
    ├── requirements.txt
    └── images/

## Author

**Lorenzo Pasini** — [FurTh3r](https://github.com/FurTh3r)

## License

No license file is currently included in this repository. Unless otherwise stated by the author, all rights are reserved.

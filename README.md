# HSLM Manuscript — Numerical Experiments

This repository contains the computational notebooks used for the HSLM manuscript.

## Files

- `Numerical_Experiments.ipynb` — neural-network nonlinear least-squares experiments comparing Classical Levenberg–Marquardt (LM), Krylov-subspace LM, and HSLM.
- `Plotting_figures.ipynb` — generates the manuscript figures from the numerical experiment summaries.
- `requirements.txt` — Python package requirements.
- `.gitignore` — excludes common local and Jupyter-generated files from version control.

## Environment

Python 3.10 or newer is recommended.

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on macOS/Linux:

```bash
source .venv/bin/activate
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Then open `Numerical_Experiments.ipynb` or `Plotting_figures.ipynb`.

## Randomness

The numerical experiments intentionally use unseeded NumPy randomness. Re-running the notebook can therefore generate different random inputs, noise, initial guesses, and random Hessian probes.

## Computational cost

The numerical experiment notebook uses large training sets and repeated LM/HSLM optimization runs, so a complete execution can be computationally expensive.

# Calderón Inverse Conductivity Reconstruction

This repository contains the notebook used for the numerical experiments in “Generalized Tikhonov-Type Regularization and the Calderón Inverse Conductivity Problem” [1].

The notebook implements a linearized reconstruction method for the Calderón inverse conductivity problem and compares two regularization techniques:

- Classical Tikhonov regularization
- Alternate Tikhonov regularization

The mathematical derivation, reconstruction method, and full discussion of the numerical results are given in [1].

## Notebook

[Calderon_Reconstruction.ipynb](Calderon_Reconstruction.ipynb)

## Numerical Experiment

The notebook generates synthetic boundary measurements for a known conductivity and attempts to reconstruct that conductivity from an initial constant approximation.

The reconstruction produces an ill-posed linear system

\[
Ac \approx r,
\]

which is solved using either classical or alternate Tikhonov regularization.

A parameter sweep is performed over:

- Number of reconstruction iterations
- Damping parameter \(\omega\)
- Classical Tikhonov parameter \(\alpha\)
- Alternate Tikhonov parameters \(\mu\) and \(\delta\)

In total, the notebook performs 666 reconstruction tests: 126 using classical Tikhonov regularization and 540 using alternate Tikhonov regularization. [1]

## Requirements

The notebook uses:

Python 3
NumPy
SciPy
pandas
Matplotlib
IPython
Jupyter Notebook or JupyterLab
openpyxl

The required packages can be installed with:

pip install numpy scipy pandas matplotlib ipython jupyter openpyxl


## Running the Notebook

1. Clone or download this repository.
2. Install the required packages.
3. Open `Calderon_Reconstruction.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells in order.

The full parameter sweep is computationally more expensive than running an individual reconstruction.

## Output

The notebook produces:

* Reconstruction results for all tested parameter combinations
* Summary tables comparing the regularization methods and parameters
* The best classical Tikhonov reconstruction
* The best alternate Tikhonov reconstruction
* A comparison with the true conductivity
* An Excel workbook containing the parameter-sweep results

## Reference

[1] Charlie Morehead, *Generalized Tikhonov-Type Regularization and the Calderón Inverse Conductivity Problem*, 2026.

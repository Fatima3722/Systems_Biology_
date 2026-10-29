# Repressilator: deterministic and stochastic models

Educational simulations inspired by the three-repressor circuit described by Elowitz and Leibler (2000).

| Notebook | Approach |
| --- | --- |
| [Deterministic model](deterministic_model/repressilator_deterministic_.ipynb) | Six coupled ODEs for three mRNAs and their proteins, integrated with SciPy |
| [Stochastic model](stochastic_model/repressilator_stochastic.ipynb) | An illustrative Euler–Maruyama model with state-dependent protein noise |

## Run

Install the dependencies from the repository-root `requirements.txt`, launch JupyterLab, and open the desired notebook. Select **Restart Kernel and Run All Cells**. Use that notebook's directory as the working directory to keep relative figure outputs in its `figures/` folder.

## Model interpretation

The deterministic model uses a cyclic repression term and first-order mRNA/protein decay. The stochastic notebook adds phenomenological noise; it is not a Gillespie simulation or a quantitatively calibrated molecular reaction model. Its random trajectory can differ between runs.

The supplied examples use `alpha=50`, `alpha_0=0.05`, `beta=0.2` and Hill coefficient `n=2`. These describe the examples, not parameter estimation from experimental data. Period and amplitude estimates depend on transient removal, peak detection and simulation settings. Any conversion from model time to minutes needs a consistent nondimensionalisation.

These notebooks explore circuit dynamics. They do not establish experimental agreement or a complete reproduction of the original study.

## Source

Elowitz, M. B., and Leibler, S. (2000). *A synthetic oscillatory network of transcriptional regulators*. Nature, 403, 335–338.

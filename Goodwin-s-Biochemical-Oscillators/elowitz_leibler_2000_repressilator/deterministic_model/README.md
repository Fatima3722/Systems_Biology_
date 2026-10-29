# Deterministic repressilator

[Notebook](repressilator_deterministic_.ipynb) · [Model overview](../README_repressilator_overview.md)

Six ODEs describe three mRNAs and their proteins in a cyclic repression network. The notebook uses `scipy.integrate.solve_ivp`, plots protein trajectories and estimates periods/amplitudes from detected peaks.

Install the repository-root dependencies and open this notebook in JupyterLab. Select **Restart Kernel and Run All Cells**; do not run an `.ipynb` file with `python`. Use this directory as the working directory for relative figure outputs.

Example parameters: `alpha=50`, `alpha_0=0.05`, `beta=0.2`, `n=2`. Generated figures are illustrative simulations, not experimental measurements. Check transients and peak detection before interpreting reported periods.

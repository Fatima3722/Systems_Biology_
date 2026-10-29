# Stochastic repressilator

[Notebook](repressilator_stochastic.ipynb) · [Model overview](../README_repressilator_overview.md)

An illustrative six-component model with state-dependent noise added to protein dynamics and Euler–Maruyama time integration. The notebook plots a simulated trajectory and estimates oscillation statistics.

Install the repository-root dependencies and open this notebook in JupyterLab. Select **Restart Kernel and Run All Cells**; do not run an `.ipynb` file with `python`. Use this directory as the working directory for relative figure outputs.

Example parameters: `alpha=50`, `alpha_0=0.05`, `beta=0.2`, `n=2`, `noise_coeff=0.5`. Random trajectories can vary between runs. This phenomenological noise model is not an exact molecular reaction simulation. Reproducible stochastic comparisons require recording random seeds and examining ensembles and time-step sensitivity.

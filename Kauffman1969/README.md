# Random Boolean genetic networks

[Notebook](Kauffman_Simulations.ipynb) · [Repository setup](../README.md#run-the-notebooks)

Educational simulations inspired by Stuart Kauffman's 1969 work on randomly constructed genetic networks. Binary elements represent simplified gene states; update rules and connectivity determine the resulting state trajectories.

## Run

Follow the repository setup, open `Kauffman_Simulations.ipynb` in JupyterLab and select **Restart Kernel and Run All Cells**. NumPy and Matplotlib are used; NetworkX supports graph visualisation.

## Explore

The notebook includes attractor/cycle exploration, network-size comparisons and perturbation examples. Parameters control network size, connectivity, the number of sampled networks and the number of initial states.

Larger ensembles can be expensive. Sampling only some initial states does not enumerate all attractors. Cycle counts and fitted trends depend on sampling, stopping criteria and random realisations; they should not be presented as universal scaling laws.

## Interpretation

These are simplified computational examples, not measured gene-regulatory networks. Attractor patterns illustrate model behaviour; they do not establish biological cell types, biological robustness or quantitative replication of the original paper. Comparisons with biological quantities need independently sourced data and explicit assumptions.

## Source

Kauffman, S. A. (1969). *Metabolic stability and epigenesis in randomly constructed genetic nets*. Journal of Theoretical Biology, 22(3), 437–467.

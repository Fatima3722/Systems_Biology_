# Metabolic Stability and Epigenesis in Randomly Constructed Genetic Nets

This project provides a Python-based simulation environment for exploring the foundational concepts presented in Stuart A. Kauffman's 1969 paper, "Metabolic Stability and Epigenesis in Randomly Constructed Genetic Nets." It demonstrates how randomly interconnected binary "genes" (Boolean elements) can spontaneously organize into stable, limited behavioral cycles, exhibiting properties relevant to biological complexity and stability.

This work aims to make the abstract concepts of the paper tangible through direct simulation, allowing users to observe the emergent order in these complex systems.

## Getting Started

**Prerequisites:**
*   Python 3.x
*   NumPy (`pip install numpy`)
*   Matplotlib (`pip install matplotlib`)
*   Collections (standard Python library)
*   (Optional for Fig 10b graph visualization: NetworkX - `pip install networkx`)

**Running the Simulations:**
1.  **Clone the repository (if applicable):**
    ```bash
    git clone https://github.com/Fatima3722/Kauffman1969
    cd Kauffman1969
    ```
2.  **Execute the Python Script/Notebook:**
    *   If it's a Jupyter Notebook (`.ipynb`): Open it with Jupyter Lab or Jupyter Notebook and run the cells sequentially.
    *   If it's a Python script (`.py`): Execute it from your terminal: `python kauffman_Simulations.py`

**Adjusting Simulation Parameters (Optional):**
*   Inside the script/notebook, you can typically find and modify parameters such as:
    *   `N_TARGET` (or `N_CURRENT`): Number of genes in a network.
    *   `K_INPUTS`: Number of inputs per gene (typically fixed at 2 or 3).
    *   `NUM_NETWORK_INSTANCES`: How many different random networks to create for statistical averaging.
    *   `NUM_INITIAL_STATES_PER_NET`: How many random starting states to test per network to find attractors.
*   **Note:** Increasing these parameters (especially `N_TARGET` and `NUM_NETWORK_INSTANCES`) will yield results closer to Kauffman's published figures but will significantly increase computation time. Default values are generally set for reasonable demonstration durations.

## Expected Output (Visualizations)

Upon running the script/notebook, you should expect to see a series of plots generated, corresponding to figures from Kauffman's paper. These will typically show:

1.  **Histograms of Cycle Lengths (Fig 3-like):** Distributions highly skewed towards short cycle lengths.
2.  **Median Cycle Length vs. N (Fig 4-like):** Log-log plot showing median cycle length increasing with network size N (approx. N^0.3 to N^0.6).
3.  **Run-in vs. Cycle Length Scatter (Fig 5-like):** A diffuse scatter plot, indicating little correlation.
4.  **Histogram of Attractors per Net (Fig 6-like):** Distribution skewed towards a few attractors per network.
5.  **Median Attractors vs. N (Fig 7-like):** Log-log plot showing median attractors increasing with N (approx. N^0.5).
6.  **Min Distance Between Cycles Scatter (Fig 8-like):** Distances are generally small (e.g., median ~0.05N for N=100).
7.  **Noise Perturbation Transitions (Fig 9-like):** Scatter plots showing that a perturbed network transitions to only a very small number of other attractors.
8.  **Transition Matrix & Markov Chain (Fig 10-like):** A heatmap of transition counts and a graph showing probabilistic transitions between attractors for a sample network.
9.  **K=3 vs. K=2 Cycle Lengths:** K=3 nets exhibiting slightly longer median cycle lengths than K=2 nets.
10. **Biological Comparison Plots (Figs 11b, 12, 13-like):**
    *   Model predictions overlaid on biological data for plant cell cycles, general cell replication times vs. gene number, and cell type diversity vs. gene number. The model trends should generally align with biological trends (e.g., scaling as N^0.5).

**Output Format:**
*   Plots will typically be displayed directly if run in a Jupyter Notebook, or potentially saved as image files if the script is configured to do so.
*   Some summary statistics (medians, means, fitted slopes, etc.) might be printed to the console or within the notebook output cells.

## Key Findings & Insights from Replication

This replication computationally confirms the core assertions of Kauffman's 1969 paper:

*    Randomly connected networks inherently self-organize into highly ordered and stable patterns of activity (attractors).
*    Despite the vast number of possible states, these networks exhibit a surprisingly small and predictable repertoire of behaviors (attractors).
*    The dynamic behavior is robust to minor perturbations (noise), with networks usually returning to their original attractor or transitioning to a very limited set of alternatives.
*    The model's properties, such as how the number of attractors or cycle lengths scale with network size, show striking parallels to fundamental biological observations (e.g., number of cell types or cell division times scaling with genome size), suggesting these networks capture generic properties of biological control systems.

## Original Paper Reference

Kauffman, S. A. (1969). Metabolic stability and epigenesis in randomly constructed genetic nets. *Journal of Theoretical Biology*, 22(3), 437-467. (e.g., DOI: `10.1016/0022-5193(69)90015-0`)



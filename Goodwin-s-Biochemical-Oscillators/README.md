# Goodwin's Biochemical Oscillators

This project provides a Python-based simulation environment for exploring the foundational concepts presented in Brian C. Goodwin's 1965 paper, "Oscillatory Behavior in Enzymatic Control Processes." It demonstrates how simple negative feedback loops in gene regulation can lead to sustained oscillations (rhythms) in cellular components, and how interactions between these oscillatory units can produce complex temporal patterns.

This work aims to make the theoretical models of the paper tangible through direct simulation, allowing users to observe the dynamic behavior of these early models of biological rhythms.

## Features & Demonstrations

This simulator implements Goodwin's mathematical models for biochemical oscillators and showcases several key phenomena and figures from the paper:

*   **Core 2-Variable Oscillator Model (Equations 1):**
    *   *Concept:* A gene produces mRNA (X), which produces a protein (Y). Protein Y represses the gene, creating a negative feedback loop.
    *   *Simulates:* Paper's Figures 2 & 3.

*   **Interacting 2-Variable Oscillators (Equations 2):**
    *   *Concept:* Two independent oscillator systems (X1,Y1 and X2,Y2) are coupled, meaning the output of one can influence the other.
    *   *Simulates:* Paper's Figures 5 through 12, demonstrating non-interaction, entrainment, beats, and subharmonic resonance.

*   **3-Variable Limit Cycle Oscillator (Equations 3):**
    *   *Concept:* A model with mRNA (X), an intermediate (Y), and a final enzyme/repressor (Z), where Z represses X. Includes first-order degradation for all species, designed for robust oscillations.
    *   *Simulates:* Paper's Figures 13 (time-course), 14 (phase portrait), and 15 (feedback inhibition interpretation).

## Getting Started

### Prerequisites
*   Python 3.6 or higher.
*   Required Python packages: `numpy`, `scipy`, `matplotlib`.
*   Jupyter Notebook/Lab and `ipykernel` (if using the `.ipynb` version of the code).

### Running the Simulations
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Fatima3722/Goodwin-s-Biochemical-Oscillators.git
    cd Goodwin-s-Biochemical-Oscillators
    ```
2.  **(Recommended)** Create and activate a Python virtual environment:
    ```bash
    python -m venv venv_goodwin
    source venv_goodwin/bin/activate  # On Windows: venv_goodwin\Scripts\activate
    ```
3.  **Install dependencies** (ensure `requirements.txt` is present in the project root):
    ```bash
    pip install -r requirements.txt
    ```
    (`requirements.txt` should list `numpy`, `scipy`, `matplotlib`, `jupyterlab` (or `notebook`), `ipykernel`)

4.  **Execute the simulation script/notebook:**
    *   If using a Jupyter Notebook (e.g., `Goodwin_Simulations.ipynb`):
        ```bash
        jupyter lab  # or jupyter notebook
        ```
        Then open the notebook file and run the cells.
    *   If using a single Python script (e.g., `goodwin_simulations.py`):
        ```bash
        python goodwin_simulations.py
        ```
    **Note:** The script generates plots sequentially. **You will likely need to close each plot window for the script to proceed to the next.**

## Expected Output

Upon running the simulation script/notebook, you should observe the following:

1.  **Console Messages:**
    *   Status updates from the ODE solver for each simulation run (e.g., "Solver status: 0" indicates success).

2.  **Sequential Plot Display & Saved Figures:**
    *   A series of plots will be displayed one by one. Close each plot to allow the next to generate.
   
    *   **For Figures 2 & 3 (Single Oscillator - Eq. 1):**
        *   Time-course plots showing rhythmic oscillations of mRNA (X) and Protein (Y).
        *   Fig. 2: Sustained, larger amplitude oscillations (when protein degradation `beta=0`).
        *   Fig. 3: Smaller, nearly sinusoidal oscillations when starting near the steady state.

    *   **For Figures 5-12 (Interacting Oscillators - Eq. 2):**
        *   Time-course plots of Protein Y1 and Y2 concentrations.
        *   Fig. 5: Independent (uncoupled) oscillations with distinct frequencies.
        *   Fig. 6: Entrainment – Y1 and Y2 synchronize to a common frequency.
        *   Fig. 7: Beats – amplitude modulation in one of the oscillators.
        *   Figs. 8 & 9: Subharmonic resonance – Y1 and Y2 lock into a shared, slower rhythm, often with increased amplitudes and specific phase differences.
        *   Fig. 10: Corresponding mRNA (X1, X2) behavior during subharmonic resonance, potentially showing different patterns than the proteins.
        *   Figs. 11 & 12: Further examples of subharmonic resonance with different parameter sets, showing variations in the low-order subharmonic.

    *   **For Figures 13, 14, & 15 (3-Variable Model - Eq. 3):**
        *   **Fig. 13 (Time Course):** A plot showing concentrations of X, Y, and Z over time. **Using the paper's listed parameters and strict first-order X-decay (Eq. 3), this simulation will show X, Y, and Z converging to stable steady-state values after an initial transient, *not* sustained oscillations.**
        *   **Fig. 14 (Phase Portrait):** A plot of Y vs. Z. Consistent with the Fig. 13 outcome, the trajectory will spiral or move towards a single fixed point, representing the steady state. No closed loop (limit cycle) will be formed.
        *   **Fig. 15 (Feedback Inhibition Interpretation):** A plot of X (as "Enzyme") and Z/100 (as "End-product"). This will also show non-oscillatory, flat lines after the system reaches its steady state.

## Key Findings & Insights 
*   Simple negative feedback in biochemical pathways (Eq. 1) can indeed produce sustained oscillations.
*   Interactions between oscillators (Eq. 2) lead to diverse, organized temporal patterns like entrainment, beats, and subharmonic resonance, crucial for cellular coordination.
*    The dynamic behavior of these non-linear systems is highly dependent on specific parameter values.
*   The 3-variable model (Eq. 3), when simulated with the paper's explicitly listed parameters for Figure 13 and adhering to first-order decay for all species, **converges to a stable steady state.** This contrasts with the oscillatory behavior visually depicted in the paper's Figures 13, 14, and 15, suggesting the visuals might stem from a model variant (e.g., zero-order X decay) or different, unstated parameters.

## Reference

Goodwin, B. C. (1965). Oscillatory behavior in enzymatic control processes. *Advances in Enzyme Regulation, 3*, 425-438.

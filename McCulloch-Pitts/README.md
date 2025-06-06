# McCulloch-Pitts Paper

This project provides a Python-based simulation environment for exploring the foundational concepts presented in Warren McCulloch and Walter Pitts' seminal 1943 paper, "A Logical Calculus of the Ideas Immanent in Nervous Activity." It demonstrates how simple, binary threshold neurons can perform logical computations, exhibit memory through recurrent connections (circles), and replicate complex neural phenomena through network architecture.

This work aims to make the abstract concepts of the paper tangible through direct simulation, allowing users to observe the behavior of these early neural networks.

## Features & Demonstrations

This simulator implements the McCulloch-Pitts neuron model and showcases several key theorems and figures from the paper:

1.  **Core Neuron Model:**
    *   All-or-none firing.
    *   Fixed threshold for activation.
    *   Excitatory and absolute inhibitory inputs.
    *   Unit synaptic delay.
2.  **Basic Logical Operations (Theorems 1 & 2):**
    *   **DELAY/IDENTITY** (Fig 1a): `N2(t) .≡. N1(t-1)`
    *   **OR** (Fig 1b): `N3(t) .≡. N1(t-1) ∨ N2(t-1)`
    *   **AND** (Fig 1c): `N3(t) .≡. N1(t-1) . N2(t-1)`
    *   **AND NOT** (Fig 1d): `N3(t) .≡. N1(t-1) . ~N2(t-1)`
3.  **Complex Temporal Propositional Expressions (TPEs):**
    *   **"Heat from Transient Cooling" Illusion (Fig 1e):** Demonstrates how a specific sequence of sensory inputs can lead to a counter-intuitive perception due to network structure.
4.  **Equivalence Theorems (Demonstrating flexibility of the model):**
    *   **Theorem 4: Relative vs. Absolute Inhibition (Inspired by Fig 1f):** Shows how a neuron appearing to have a modulated threshold (relative inhibition) can be constructed using only M-P neurons with fixed thresholds and absolute inhibition.
    *   **Theorem 5: Extinction / Refractory Periods (Inspired by Fig 1g):** Utilizes feedback circuits to model activity-dependent reduction in neuronal excitability for a defined period (M steps).
    *   **Theorem 6: Temporal Summation by Spatial Summation (Fig 1h):** Illustrates how a sequence of inputs arriving over time can be converted by network architecture into simultaneous (spatial) inputs for summation at a target neuron.
    *   **Theorem 7: Alterable Synapses by Circles (Inspired by Fig 1i):** Demonstrates how reverberating circuits (latches) can implement a form of memory, where the network's response to an input is altered after a specific "pairing" event, mimicking a change in synaptic efficacy.


## Getting Started

### Prerequisites

*   Python 3.6 or higher.
*   No external Python libraries are required for the core simulation logic.

### Running the Simulations

1.  Clone the repository:
    ```bash
    git clone https://github.com/Fatima3722/McCulloch-Pitts
    cd McCulloch-Pitts
    ```
2.  Execute the Python script:
    ```bash
    python mcculloch_pitts_simulatons.ipynb
    ```
3.  The script will run through all pre-defined simulation scenarios sequentially. The output for each scenario will be printed to the console, including:
    *   A title indicating the concept/theorem being demonstrated.
    *   A time-step history table showing the state (0 or 1) of relevant neurons.

## Understanding the Output

Each simulation scenario will produce a table like this:

Time | N1 | N2
0 | 1 | 0
1 | 0 | 1
2 | 1 | 0
3 | 0 | 1
4 | 0 | 0
5 | 0 | 0


*   **Time:** The discrete time step of the simulation.
*   **Neuron Columns (e.g., N1, N2, N_Target):** The state (1 for firing, 0 for not firing) of the specified neuron at that time step.
*   The states at `Time t` are used to calculate the states for `Time t+1`, reflecting the synaptic delay. Input neurons are typically set at the beginning of a time step.

## Key Findings & Insights from Replication

This replication visually and computationally confirms the core assertions of McCulloch and Pitts:

*   **Neurons as Logic Units:** Simple binary neurons can indeed form the basis of logical computation.
*   **Computational Power of Architecture:** The structure and connectivity of the neural network are paramount in determining its function. Complex behaviors and even memory-like phenomena (as seen in Theorem 7) can emerge from fixed-component networks with appropriate feedback loops (circles).
*   **Temporal Dynamics:** The model explicitly handles time through synaptic delays, allowing for the processing of sequences and temporal patterns.
*   **Foundation for AI:** These principles laid crucial groundwork for the development of artificial neural networks and computational theories of mind.


## Acknowledgements

Based on the groundbreaking work of Warren S. McCulloch and Walter Pitts (1943), "A Logical Calculus of the Ideas Immanent in Nervous Activity."

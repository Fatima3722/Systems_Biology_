# McCulloch–Pitts threshold networks

[Notebook](McCulloch_Pitts_Simulations.ipynb) · [Repository setup](../README.md#run-the-notebooks)

Educational discrete-time simulations inspired by McCulloch and Pitts' logical neuron model. Each unit has a binary state, a threshold and excitatory/inhibitory inputs.

## Run

Follow the repository setup, open `McCulloch_Pitts_Simulations.ipynb` in JupyterLab and select **Restart Kernel and Run All Cells**. The core network logic uses standard Python; Jupyter is needed to execute the notebook interactively.

## Model and output

The code calculates each neuron's next state from the current states of its inputs, then updates network states. An active inhibitory input prevents firing; otherwise the excitatory input count is compared with the threshold.

The notebook contains logic-gate and temporal/feedback examples. Printed histories show binary neuron states at successive time steps. Follow the input schedule alongside those histories when interpreting delays and feedback.

## Scope

These examples illustrate logical computation with idealised units. They are not biophysical neuron models or experimental neuroscience results. Demonstrating selected circuits does not constitute a proof of every theorem in the original paper.

## Source

McCulloch, W. S., and Pitts, W. (1943). *A logical calculus of the ideas immanent in nervous activity*.

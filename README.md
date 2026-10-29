# Systems biology: computational models

Python notebooks exploring how feedback, network structure and stochasticity shape biological dynamics. These are educational implementations inspired by classic papers, with model explanations and simulation outputs.

## Explore the projects

| Project | Biological or computational question | Implementation |
| --- | --- | --- |
| [Goodwin models](Goodwin-s-Biochemical-Oscillators/README.md) | How do negative feedback and coupling affect biochemical dynamics? | Differential-equation simulations and time-course/phase plots |
| [Repressilator](elowitz_leibler_2000_repressilator/README_repressilator_overview.md) | How does a three-repressor circuit behave with and without added noise? | [Deterministic ODE notebook](elowitz_leibler_2000_repressilator/deterministic_model/repressilator_deterministic_.ipynb) and [stochastic notebook](elowitz_leibler_2000_repressilator/stochastic_model/repressilator_stochastic.ipynb) |
| [Boolean genetic networks](Kauffman1969/README.md) | How do network connectivity and initial states affect attractors? | Random Boolean networks, cycle detection and perturbation examples |
| [McCulloch–Pitts networks](McCulloch-Pitts/README.md) | How can binary threshold units implement logic and temporal processing? | Discrete-time excitatory/inhibitory networks |

## Run the notebooks

```bash
git clone https://github.com/Fatima3722/Systems_Biology_.git
cd Systems_Biology_
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

On Windows, activate with `.venv\Scripts\activate`. Open a notebook from the table, then select **Restart Kernel and Run All Cells**. Launch each repressilator notebook with its own folder as the working directory if you want its relative figure paths to stay within that project.

## Scope and interpretation

These notebooks demonstrate selected models and parameter choices; they are not new experimental findings or complete, quantitatively validated reproductions of the source papers. Saved outputs are examples, not a substitute for independent reruns. Random-network and stochastic results can vary between runs.

The Goodwin notebook includes a three-variable case documented as approaching a steady state for its implemented equations and parameters. This alone does not establish an error in the original paper. The stochastic repressilator is an illustrative noise-augmented model, not an exact molecular reaction simulation.

The repressilator also appears inside the Goodwin folder as a legacy duplicate. Use the top-level repressilator links above as the main entry points.

## Related work

[Gene-regulatory network motifs](https://github.com/Fatima3722/Uri_Alon_System_Biology) · [Bioinformatics portfolio](https://github.com/Fatima3722/Bioinformatics_Projects)

Original model credit belongs to the authors cited in each project.

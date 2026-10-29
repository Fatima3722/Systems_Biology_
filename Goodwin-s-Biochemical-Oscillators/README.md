# Goodwin biochemical feedback models

[Notebook](Goodwin_Simulations.ipynb) · [Repository setup](../README.md#run-the-notebooks)

Educational differential-equation simulations inspired by Goodwin's biochemical control models. The notebook explores single feedback systems, coupled systems and a three-variable model through time courses and phase plots.

## Run

Follow the repository setup, then open `Goodwin_Simulations.ipynb` in JupyterLab and select **Restart Kernel and Run All Cells**. This is a notebook, not a standalone Python script.

## What to examine

- How feedback and degradation terms affect the time evolution.
- How changing coupling and initial conditions changes the relationship between two systems.
- Whether oscillations persist after transients, rather than judging from a short time window alone.

The existing notebook documents a three-variable parameter case that approaches a steady state. Treat this as an observation about the implemented equations and parameters. A discrepancy with a published figure requires checking equation transcription, parameter conventions, initial conditions and solver convergence before drawing conclusions about the original paper.

## Scope

This is an educational model exploration. Quantitative agreement with all original figures, sustained oscillations across parameter choices and biological predictions have not been independently established by this documentation update.

## Source

Goodwin, B. C. (1965). *Oscillatory behavior in enzymatic control processes*. Advances in Enzyme Regulation, 3, 425–438.

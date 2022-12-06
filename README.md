# Data supporting *Double-diffusive transport in multicomponent vertical convection*

![](https://zenodo.org/badge/DOI/10.5281/zenodo.7404867.svg)

This repository contains post-processing Jupyter notebooks used to construct figures from the manuscript.
The manuscript has been accepted for publication in *Physical Review Fluids* and is available on arXiv at https://arxiv.org/abs/2207.09230

The files provided are as follows

- `collect_profiles.ipynb`
    - This notebook creates the datasets stored in `base_profiles.csv` and `ref_profiles.csv` from the simulation output. This simulation output (consisting of time series of 1D profiles for various statistical quantities) is freely available on the 4TU ResearchData repository at https://doi.org/10.4121/21679772. Without this data, this notebook will fail to run.
- `base_profiles.csv` and `ref_profiles.csv`
    - These CSV formatted datasets are the output from the `collect_profiles` notebook. They contain time averaged profiles of a range of statistical quantities used by the remaining notebooks.
- `afidtools`
    - This directory contains a small Python package containing helper functions for accessing and manipulating the simulation output.
- `fig2_active_passive.ipynb`
    - Reconstructs figure 2 using the data provided. Compares simulations where temperature is a passive scalar with those where temperature contributes to the buoyancy.
- `fig4_5_6_fluxes_BLs_and_diffusivity.ipynb`
    - Reconstructs figures 4, 5, and 6 from the data provided. These present data about the global fluxes, boundary layer widths, and turbulent diffusivities.
- `fig8_melt_rate_dependence.ipynb`
    - Reconstructs figure 8, highlighting the theoretical dependence of melt rate on the heat-to-salt flux ratio.
- `fig9_variance_budgets.ipynb`
    - Reconstructs the appendix figure (9), describing the budgets for the evolution of temperature variance
- `sec3A_linear_nonlinear.ipynb`
    - This final notebook discusses the potential errors associated with using a linear equation of state as compared to the nonlinear equation of state provided by the `gsw` toolbox.

### Prerequisites
To run these notebooks successfully, you need a recent version of Python, along with a Jupyter installation, and the packages listed in `requirements.txt`.
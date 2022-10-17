# Data supporting *Double-diffusive transport in multicomponent vertical convection*

This repository contains post-processing Jupyter notebooks used to construct figures from the manuscript.
The files provided are as follows

- `collect_profiles.ipynb`
    - This notebook creates the datasets stored in `base_profiles.csv` and `ref_profiles.csv` from the simulation output. Before publication of the manuscript, this simulation output (consisting of time series of 1D profiles for various statistical quantities) will be freely available on the 4TU ResearchData repository. Without this data, this notebook will fail to run.
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
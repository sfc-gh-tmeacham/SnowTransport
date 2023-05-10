# SnowTransport

CSV and Excel File uploader for Snowflake

## To Install

### Faster Solver (OPTIONAL) 
Use libmamba for a much faster solver

https://conda.github.io/conda-libmamba-solver/getting-started/

First, make sure you are running conda 4.12.0 or higher:
```
conda update -n base conda
```

Then install conda-libmamba-solver:
```
conda install -n base conda-libmamba-solver
```

Use the following command to always use libmamba as your default solver:

```
conda config --set solver libmamba
```
If you are unsure what configuration is being used by conda, you can inspect it with 
```
conda config --show-sources.
```


If you need to revert the default configuration back to classic solver, you can:

Run 
```
conda config  --set solver classic (to do your choice explicit).
```
Run 
```
conda config --remove-key solver to delete the solver: libmamba line from your .condarc file.
```

Verify config
```
conda config --show-sources.
```


## Required

Use these commands to create and activate the conda environment based on the specifications in the Yaml file:
```
conda env create --file snowtransport_env.yml
conda activate snowtransport_env
```
To run this streamlit app
```
streamlit run app.py
```
Use this command to list the environments you have:
```
conda info --envs
```

Use this command to remove the environment:
```
conda env remove --name snowtransport_env
```

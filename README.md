# SnowTransport

CSV and Excel File uploader for Snowflake from TKO 2022. 

## To Install

### Faster Solver (OPTIONAL) 
Use libmamba for a much faster solver: https://conda.github.io/conda-libmamba-solver/getting-started/

1. First, make sure you are running conda 4.12.0 or higher: `conda update -n base conda`

2. Then install conda-libmamba-solver: `conda install -n base conda-libmamba-solver` 

3. Use the following command to always use libmamba as your default solver: `conda config --set solver libmamba`

4. If you are unsure what configuration is being used by conda, you can inspect it with: `conda config --show-sources`

From now on, Conda should use the faster solver.

### Revert to Classic Solver

1. If you need to revert the default configuration back to classic solver run:
    `conda config  --set solver classic` to make your choice explicit.

2. Run `conda config --remove-key solver` to delete the solver: libmamba line from your .condarc file.

3. Verify config `conda config --show-sources` 


## Required to run SnowTransport

Use these commands to create and activate the conda environment based on the specifications in the Yaml file:
```
conda env create --file snowtransport_env.yml
conda activate snowtransport_env
```
To run this streamlit app
```
streamlit run app.py
```

#### Tips
Use this command to list the environments you have: `conda info --envs`

Use this command to remove the environment: `conda env remove --name snowtransport_env`

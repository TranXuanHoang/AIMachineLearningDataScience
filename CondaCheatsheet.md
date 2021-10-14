# Conda (Anaconda/Miniconda) Cheatsheet

## Create and remove environments

```powershell
# Create an environment <env_name> then install 3rd-party libraries (dependencies)
# This will create an environment and install all dependencies inside
#   macOS: /Users/your.username/anaconda3/envs/<env_name>
#   Windows: C:\Users\your.username\Anaconda3\envs\<env_name>
# or
#   macOS: /Users/your.username/miniconda3/envs/<env_name>
#   Windows: C:\Users\your.username\Miniconda3\envs\<env_name>
conda create --name <env_name> <dependency 1> <dependency 1> ... <dependency n>

# Remove an environment <env_name>
conda env remove --name <env_name>
```

```powershell
# Create an environment in a specific local directory
conda create --prefix <path/to/the/environment/directory> <dependency 1> <dependency 1> ... <dependency n>

# Remove an environment created in a specific local directory
conda env remove --prefix <path/to/the/environment/directory>

# Note that <path/to/the/environment/directory> in both 2 above commands
# can be absolute or relative

# E.g., Create an environment `env` inside the directory where the terminal
# is currently active and right after that
# install 'jupyter', 'pandas', 'numpy', 'matplotlib', and 'scikit-learn'
conda create --prefix ./env jupyter pandas numpy matplotlib scikit-learn

# Then remove it
conda env remove --prefix ./env
```

## Export environments

For more detail, see [this page](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#exporting-an-environment-file-across-platforms).

```powershell
# Export environment with dependencies you specifically chose
conda env export --from-history -p <path/to/env/dir> -f <output_env_file.yml>

# Export environment with all installed dependencies
conda env export -p <path/to/env/dir> -f <output_env_file.yml>

# Shorthand command (run after activating the env we want to export)
conda env export > environment.yml

# E.g., Export dependencies of the environment installed in './env'
# and output dependencies list to 'envorinment.yaml' file
conda env export --from-history -p ./env -f environment.yml
```

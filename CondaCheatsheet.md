# Conda (Anaconda/Miniconda) Cheatsheet

## Create and remove environments

```powershell
# Create an environment <env_name> then install 3rd-party libraries (dependencies)
# This will create an environment and install all dependencies inside
#   macOS: /Users/your.username/opt/Anaconda3/envs/<env_name>
#   Windows: C:\Users\your.username\Anaconda3\envs
# or
#   Windows: C:\Users\your.username\Miniconda3\envs
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

# Basics of Data Science Environment Setup

## Setup Environment

```powershell
# Create an environment whose name is 'basics' and right after that
# install 'jupyter', 'pandas', 'numpy', 'matplotlib', and 'scikit-learn'
conda create --name basics jupyter pandas numpy matplotlib scikit-learn

# Create an environment `env` inside the directory where the terminal is currently active
# and right after that
# install 'jupyter', 'pandas', 'numpy', 'matplotlib', and 'scikit-learn'
conda create --prefix ./env jupyter pandas numpy matplotlib scikit-learn

# Install Seaborn
conda install -c anaconda seaborn

# Install spaCy and its trained pipelines (English and Japanese)
# https://spacy.io/usage
# Should run the installation against a specific 'environment'
# (See the next section for how to activate an environment with conda)
conda install -c conda-forge spacy
python -m spacy download en_core_web_trf
python -m spacy download ja_core_news_lg

# Install Bokeh for creating interactive visualizations for modern web browsers
conda install -c bokeh bokeh

# Install Plotly and Cufflinks (to link Plotly and Pandas)
conda install -c conda-forge plotly
pip install cufflinks

# Install Plotly Dash and Jupyter Dash to support
# Jupyter Notebooks / JupyterLab as development environment
# using Dash and Plotly
conda install -c conda-forge dash
conda install -c conda-forge jupyter-dash

# Install JupyterLab
conda install -c conda-forge jupyterlab
```

## Start Jupyter Notebooks

```shell
# We need to run conda using the 'Anaconda Prompt'

# Change directory using Anaconda Prompt (Windows)
cd C:/Users/hoang.tran/Desktop/Home/Workplace/AIMachineLearningDataScience/00-basics/

# Activate local environment
conda activate </Absolute/Path/to/AIMachineLearningDataScience/00-basics/env>

# Or just simply type in
conda activate ./env

jupyter notebook
```

## Start JupyterLab

```powershell
# cd into the directory where env was created,
# then activate virtual environment
conda activate ./env

# Start JupyterLab
jupyter-lab
```

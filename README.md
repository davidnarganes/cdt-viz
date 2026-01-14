
# CDT Visualisation Workshop

Examples of visualisation practices for scientific communication and Python visualisation libraries.

## Notebooks

1. Zou et al. (2023) - GPT-4 Performance Drift
2. Gemini vs GPT-4 - Benchmark Comparison
3. Holmes et al. - COVID-19 ROC Curve
4. Kim et al. (2023) - Enzyme Classification Validation

## Setup (Pure `uv`)

We use [uv](https://github.com/astral-sh/uv) for lightning-fast setup.

### 1. Install uv
If you don't have `uv` installed, get it here:


```

# MacOS / Linux install command

curl -LsSf [https://astral.sh/uv/install.sh](https://astral.sh/uv/install.sh) | sh

```

### 2. Clone & Sync


```

# Clone the repository

git clone [https://github.com/davidnarganes/cdt-viz.git](https://www.google.com/search?q=https://github.com/davidnarganes/cdt-viz.git)
cd cdt-viz

# Creates the virtual environment and installs all locked dependencies from uv.lock

uv sync

```

### 3. Run
You can launch Jupyter directly through `uv` without manually activating the environment:


```

# Run Jupyter Notebook inside the managed environment

uv run jupyter notebook

```

## Maintenance: Cleaning Notebooks

To keep the repository clean, we strip output metadata and images before committing.

Manual Clean:


```

# Strip output from all notebooks in the notebooks folder

uv run nbstripout notebooks/*.ipynb

```

Automatic Setup (Git Hook):
To automatically clean notebooks every time you `git commit`:


```

# Install the git hook so you don't have to remember to clean manually

uv run nbstripout --install

```
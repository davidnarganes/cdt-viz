# CDT Visualisation Workshop

## Overview
Examples of visualisation practices for scientific communication and Python visualisation libraries.

---

## Notebooks

- Zou et al. (2023) — GPT-4 Performance Drift
- Gemini vs GPT-4 — Benchmark Comparison
- Holmes et al. — COVID-19 ROC Curve
- Kim et al. (2023) — Enzyme Classification Validation

---

## Setup (Pure `uv`)

We use `uv` for lightning-fast, reproducible environment setup.

### 1. Install `uv`

If you do not already have `uv` installed:

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh
````

---

### 2. Clone & Sync

```bash
# Clone the repository
git clone https://github.com/davidnarganes/cdt-viz.git
cd cdt-viz

# Create the virtual environment and install locked dependencies
uv sync
```

---

### 3. Run

Launch Jupyter directly inside the managed environment (no manual activation required):

```bash
uv run jupyter notebook
```

---

## Maintenance: Cleaning Notebooks

To keep the repository clean and reviewable, all output metadata and embedded images are stripped before committing.

### Manual Cleaning

```bash
# Strip output from all notebooks in the notebooks directory
uv run nbstripout notebooks/*.ipynb
```

### Automatic Setup (Git Hook)

Install a Git hook to clean notebooks automatically on every commit:

```bash
uv run nbstripout --install
```
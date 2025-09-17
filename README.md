# model-ai-methods

Methods package for AI governance research: evolutionary game theory, agent-based modeling, and network analysis tools.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [Running the Notebook](#running-the-notebook)
- [Makefile Targets](#makefile-targets)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This repository contains the `model-ai-methods` package, a Python library providing research methods for AI governance analysis. The package includes:

- **Evolutionary Game Theory**: Fixation rate calculations, transition matrices, and stationary distributions
- **Agent-Based Modeling**: Multi-agent simulation framework for policy analysis
- **Network Analysis**: Graph-based modeling utilities
- **DSAIR Models**: Game-theoretic models for AI safety and regulation
- **Statistical Tools**: Bootstrapping, regression analysis, and data processing utilities
- **Visualization**: Plotting tools for research results

Example notebooks demonstrate applications to AI governance research problems.

## Setup

To set up the environment and install the necessary dependencies, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/PaoloBova/model-ai-methods.git
    cd model-ai-methods
    ```

2. **Install using Poetry** (recommended):
    ```bash
    poetry install
    poetry shell
    ```

    Or **create environment manually**:
    ```bash
    make env
    mamba activate model-ai-methods
    make deps
    ```

## Usage

### Python Package

After installation, import the package in Python:

```python
from model_ai.methods import egt
from model_ai.methods.models import payoffs
from model_ai.methods.utils import plot_utils

# Example: Create DSAIR model
models = payoffs.build_DSAIR(s=[1.1, 1.5, 2.0], p=[0.1, 0.5, 0.9])
```

### Running Example Notebooks

1. **Start Jupyter Lab**:
    ```bash
    make lab
    ```

2. **Open example notebooks**:
    Navigate to the `examples/` directory and open one of the analysis notebooks:
    - `10_analysis_dsair.ipynb` - DSAIR model analysis
    - `11_analysis_regulator_markets.ipynb` - Regulatory market analysis

## Makefile Targets

The Makefile includes several targets to help with setup and running the project:

- `env`: Creates the mamba environment with the specified Python version.
- `deps`: Installs the dependencies listed in `requirements.txt`.
- `lab`: Runs Jupyter Lab within the environment.
- `clean`: Removes the mamba environment.

Example usage:
```bash
make env       # Create the environment
make deps      # Install dependencies
make lab       # Run Jupyter Lab
make clean     # Clean the environment
```

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.


# Interpretability and Continual Learning Experiments

This repository contains multiple Jupyter notebooks recreating results from key research papers as well as implementing additional experiments. The focus is on interpretability, continual learning, and model performance comparison. Below are details about the included files and their functionality:

## File Descriptions

### 1. `Interpretability(XY).ipynb`
- **Purpose:** Recreates results from a paper focused on interpretability.
- **Description:**
  - This notebook demonstrates how models derive interpretable equations from data.
  - A toy dataset is created using a simple 2-variable equation: `x * y`.
  - The results closely match the interpretability results presented in the referenced paper.

### 2. `continual_learning.ipynb`
- **Purpose:** Recreates results from the KAN paper on continual learning.
- **Description:**
  - This notebook highlights the limitations of standard Multi-Layer Perceptrons (MLPs), which forget previously learned data and cannot learn continuously.
  - It also demonstrates how KAN (Knowledge Aware Neural Network) addresses this issue effectively.

### 3. `kanMNIST.ipynb`
- **Purpose:** Implements experiments using the KAN model on the MNIST dataset.
- **Description:**
  - EfficientKAN is utilized for training and testing on MNIST.
  - Modifications include:
    - Changing the optimizer to `AdamW`.
    - Adding early stopping to prevent overfitting.
  - This experiment was not part of the original KAN paper and represents additional work and tweaks.

### 4. `mlpMNIST.ipynb`
- **Purpose:** Compares the performance of an MLP on MNIST with that of KAN.
- **Description:**
  - Uses the same experimental setup as `kanMNIST.ipynb`, but replaces KAN with a standard MLP.
  - Results allow direct comparison between the two models to evaluate their differences.

### 5. `testingKAN.ipynb`
- **Purpose:** Recreates the GRID extension experiment from the KAN paper.
- **Description:**
  - The results from this notebook are consistent with those reported in the paper, validating the robustness of KAN in GRID-based experiments.

## Requirements
To run the notebooks in this repository, the following dependencies are required:
- Python (>=3.8)
- PyTorch
- NumPy
- Matplotlib
- scikit-learn
- pykan (Install using `pip install pykan`)

Additional libraries may be required based on the notebooks. Refer to the respective notebooks for their import statements.

## Usage
Each notebook is standalone and can be executed independently. Ensure that the necessary datasets and dependencies are available.

### Example Execution
Open any notebook using Jupyter and run the cells sequentially. For example:
```bash
jupyter notebook Interpretability(XY).ipynb

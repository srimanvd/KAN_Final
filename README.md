# Interpretability and Continual Learning Experiments

This repository contains multiple Jupyter notebooks recreating results from key research papers as well as implementing additional experiments. The focus is on interpretability, continual learning, and model performance comparison. Below are details about the included files and their functionality:

## File Descriptions

### 1. `Interpretability(XY).ipynb`
- **Purpose:** Recreates results from a paper focused on interpretability.
- **Description:**
  - This notebook demonstrates how models derive interpretable equations from data.
  - A toy dataset is created using a simple 2-variable equation: `x * y`.
  - The results closely match the interpretability results presented in the referenced paper.

### 2. `continualLearning.ipynb`
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

## Modifications and Improvements
This repository includes additional changes and improvements beyond what was originally presented in the referenced papers:

### EfficientKAN
- Utilized EfficientKAN for training and testing on the MNIST dataset, which optimizes the performance and resource utilization of the KAN model.

### Optimizer Change
- Replaced the standard optimizer with `AdamW` in `kanMNIST.ipynb` to achieve better convergence during training.

### Early Stopping
- Introduced early stopping in `kanMNIST.ipynb` to prevent overfitting and reduce unnecessary training epochs.

### Experiment Expansion
- Applied the KAN framework to the MNIST dataset, which was not included in the original KAN paper.
- Added a comparison experiment using MLP (`mlpMNIST.ipynb`) under the same conditions as the KAN experiments to evaluate performance differences.

## Requirements
To run the notebooks in this repository, the following dependencies are required:
- Python (>=3.8)
- PyTorch
- NumPy
- Matplotlib
- scikit-learn
- pykan (Install using `pip install pykan`)

Additional libraries may be required based on the notebooks. Refer to the respective notebooks for their import statements.

## Results Summary
- **Interpretability:** Demonstrates how models can derive interpretable equations like `x * y` from data.
- **Continual Learning:** Highlights the limitations of MLPs in continual learning and showcases the effectiveness of KAN.
- **MNIST Experiments:** Provides a detailed comparison between EfficientKAN and MLP on MNIST, with additional tweaks like optimizer changes and early stopping.
- **GRID Experiment:** Validates KAN’s performance in GRID-based tasks.

## Contributions
This repository:
- Recreates results from research papers for validation.
- Adds original experiments and improvements, particularly with MNIST and EfficientKAN.
- Includes code adapted from the original [pykan GitHub repository]([https://github.com/pykan](https://github.com/KindXiaoming/pykan/tree/master)).

For questions or feedback, feel free to open an issue in the repository. Contributions are welcome!

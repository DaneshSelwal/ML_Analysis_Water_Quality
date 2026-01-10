# ML Analysis of Water Quality

This repository contains comprehensive Machine Learning analyses focused on **Entropy Weighted Water Quality Index (EWQI)** and **Water Quality Index (WQI)**. It utilizes advanced techniques such as Conformal Prediction, Quantile Regression, and Hyperparameter Tuning to provide robust predictions and insights into water quality data.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Methodologies](#methodologies)
- [Installation](#installation)
- [Usage](#usage)

## Overview

The goal of this project is to analyze and predict water quality indices using various statistical and machine learning frameworks. The repository is divided into two main sections:

1.  **EWQI**: Analysis specifically tailored for Entropy Weighted Water Quality Index.
2.  **WQI**: Analysis specifically tailored for standard Water Quality Index.

Key features include uncertainty quantification via conformal prediction, model optimization through hyperparameter tuning, and detailed distribution analysis.

## Project Structure

The codebase is organized hierarchically by the type of index (EWQI/WQI) and then by the methodology used. Below is a guide to navigate the repository:

### [EWQI](./EWQI/)
Analysis related to Entropy Weighted Water Quality Index.

- **[Conformal Predictions](./EWQI/Conformal%20Predictions/)**
    - Notebook: `Conformal Predictions(MAPIE,PUNCC)_EWQI.ipynb`
    - Implements uncertainty quantification using MAPIE and PUNCC libraries.
- **[Hyperparameter Tuning](./EWQI/Hyperparameter%20Tuning/)**
    - Notebook: `Optuna_autosampler_EWQI.ipynb`
    - Uses Optuna for finding optimal model parameters.
- **[Quantile Regression](./EWQI/Quantile%20Regression/)**
    - Notebook: `Quantile_Regression_EWQI.ipynb`
    - Performs regression to estimate conditional quantiles of the target.
- **[Probabilistic Distribution](./EWQI/Probabilistic%20Distribution/)**
    - Notebook: `Probabilistic__Distribution_WQI.ipynb`
    - Analyzes the probabilistic distribution of the data.
- **[Data](./EWQI/Data/)**
    - Contains `train.csv` and `test.csv` used for EWQI models.

### [WQI](./WQI/)
Analysis related to Water Quality Index.

- **[Conformal Prediction](./WQI/Conformal%20Prediction/)**
    - Notebook: `Conformal Predictions(MAPIE,PUNCC)_WQI.ipynb`
    - Similar to the EWQI section, focuses on uncertainty for WQI.
- **[Hyperparameter Tuning](./WQI/Hyperparameter%20Tuning/)**
    - Notebook: `Optuna_autosampler_scour.ipynb`
    - Hyperparameter optimization for WQI models.
- **[Quantile Regression](./WQI/Quantile%20Regression/)**
    - Notebook: `Quantile_Regression_WQI.ipynb`
    - Quantile regression analysis for WQI.
- **[Probabilistic Distribution](./WQI/Probabilistic%20Distribution/)**
    - Notebook: `Probabilistic__Distribution_WQI.ipynb`
    - Distribution analysis for WQI data.
- **[Data](./WQI/Data/)**
    - Contains `train.csv` and `test.csv` used for WQI models.

## Methodologies

### Conformal Prediction
We use [MAPIE](https://github.com/scikit-learn-contrib/MAPIE) and [PUNCC](https://github.com/deel-ai/puncc) to construct prediction intervals that guarantee a certain level of coverage (e.g., 90%). This is crucial for understanding the reliability of the model's predictions in critical domains like water quality.

### Hyperparameter Tuning
[Optuna](https://optuna.org/) is employed to automate the process of hyperparameter optimization. This ensures that the machine learning models (e.g., Gradient Boosting, Random Forest) are tuned for the best possible performance on the given datasets.

### Quantile Regression
Unlike standard regression which predicts the mean, quantile regression predicts specific quantiles (e.g., median, 10th percentile, 90th percentile). This gives a more complete picture of the potential outcomes and risks.

## Installation

To run the analyses in this repository, you need Python installed along with several data science and machine learning libraries.

You can install the dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn mapie puncc optuna
```

*Note: It is recommended to use a virtual environment or Conda environment to manage dependencies.*

## Usage

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/ML_Analysis_Water_Quality.git
    cd ML_Analysis_Water_Quality
    ```

2.  **Navigate to a Directory**:
    Choose the analysis you want to run. For example, to run Conformal Predictions for EWQI:
    ```bash
    cd "EWQI/Conformal Predictions"
    ```

3.  **Run the Notebook**:
    Launch Jupyter Notebook or JupyterLab:
    ```bash
    jupyter notebook
    ```
    Then open the corresponding `.ipynb` file (e.g., `Conformal Predictions(MAPIE,PUNCC)_EWQI.ipynb`) and run all cells.

---
*Created for the ML_Analysis_Water_Quality project.*

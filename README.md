# ML Analysis of Water Quality

This repository contains comprehensive Machine Learning analyses focused on **Entropy Weighted Water Quality Index (EWQI)** and **Water Quality Index (WQI)**. It utilizes advanced techniques such as Conformal Prediction, Quantile Regression, Probabilistic Distribution Analysis, and Hyperparameter Tuning to provide robust predictions and insights into water quality data.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Methodologies](#methodologies)
- [Supported Models](#supported-models)
- [Installation](#installation)
- [Usage](#usage)

## Overview

The goal of this project is to analyze and predict water quality indices using various statistical and machine learning frameworks. The repository is divided into two main sections:

1.  **EWQI**: Analysis specifically tailored for Entropy Weighted Water Quality Index.
2.  **WQI**: Analysis specifically tailored for standard Water Quality Index.

Key features include uncertainty quantification via multiple conformal prediction methods, model optimization through hyperparameter tuning, and detailed probabilistic distribution analysis using state-of-the-art techniques.

## Project Structure

The codebase is organized hierarchically by the type of index (EWQI/WQI) and then by the methodology used. Below is a guide to navigate the repository:

### [EWQI](./EWQI/)
Analysis related to Entropy Weighted Water Quality Index.

- **[Conformal Predictions (MAPIE, PUNCC)](./EWQI/Conformal_Predictions(MAPIE,PUNCC)/)**
    - Notebook: `Conformal Predictions(MAPIE,PUNCC).ipynb`
    - Implements uncertainty quantification using MAPIE and PUNCC libraries.
- **[Conformal Predictions (NEXCP, Adaptive CP, mfcs)](./EWQI/Conformal_Predictions(NEXCP,AdaptiveCP,mfcs)/)**
    - Notebook: `Conformal_Predictions(NEXCP, Adaptive CP, mfcs).ipynb`
    - Advanced conformal prediction techniques including Normalized Empirical Cross Conformal Prediction (NEXCP) and Adaptive CP.
- **[Hyperparameter Tuning](./EWQI/HyperParameter_Tuning/)**
    - Notebook: `Optuna_autosampler_EWQI.ipynb`
    - Uses Optuna for finding optimal model parameters.
- **[Quantile Regression](./EWQI/Quantile_Regression/)**
    - Notebook: `Quantile_Regression_EWQI.ipynb`
    - Performs regression to estimate conditional quantiles of the target.
- **[Probabilistic Distribution](./EWQI/Probabilistic_Distribution/)**
    - Notebook: `Probabilistic__Distribution.ipynb`
    - Standard probabilistic distribution analysis.
- **[Probabilistic Distribution (CARD)](./EWQI/Probabilistic_Distribution(CARD)/)**
    - Notebook: `Probabilistic__Distribution(CARD).ipynb`
    - Advanced distribution analysis using Conditional Autoregressive Density (CARD) and Treeffuser.
- **[Data](./EWQI/Data/)**
    - Contains `train.csv` and `test.csv` used for EWQI models.

### [WQI](./WQI/)
Analysis related to Water Quality Index.

- **[Conformal Prediction (MAPIE, PUNCC)](./WQI/Conformal_Predictions(MAPIE,PUNCC)/)**
    - Notebook: `Conformal Predictions(MAPIE,PUNCC)_WQI.ipynb`
    - Uncertainty quantification using MAPIE and PUNCC for WQI.
- **[Conformal Predictions (NEXCP, Adaptive CP, mfcs)](./WQI/Conformal_Predictions(NEXCP,AdaptiveCP,mfcs)/)**
    - Notebook: `Conformal_Predictions(NEXCP, Adaptive CP, mfcs).ipynb`
    - Implementation of NEXCP, Adaptive CP, and mfcs for WQI data.
- **[Hyperparameter Tuning](./WQI/HyperParameter_Tuning/)**
    - Notebook: `Optuna_autosampler_scour.ipynb`
    - Hyperparameter optimization for WQI models.
- **[Quantile Regression](./WQI/Quantile_Regression/)**
    - Notebook: `Quantile_Regression_WQI.ipynb`
    - Quantile regression analysis for WQI.
- **[Probabilistic Distribution](./WQI/Probabilistic_Distribution/)**
    - Notebook: `Probabilistic__Distribution_WQI.ipynb`
    - Distribution analysis for WQI data.
- **[Probabilistic Distribution (CARD)](./WQI/Probabilistic_Distribution(CARD)/)**
    - Notebook: `Probabilistic__Distribution(CARD).ipynb`
    - CARD-based probabilistic distribution analysis for WQI.
- **[Data](./WQI/Data/)**
    - Contains `train.csv` and `test.csv` used for WQI models.

## Methodologies

### Conformal Prediction
We employ a variety of conformal prediction frameworks to construct valid prediction intervals:
- **MAPIE & PUNCC**: Standard libraries for conformal prediction.
- **NEXCP**: Normalized Empirical Cross Conformal Prediction for robust interval estimation.
- **Adaptive CP**: Techniques that adapt interval widths based on local difficulty.
- **mfcs**: Model-Free Conformal Selection strategies.

### Probabilistic Distribution
Beyond point predictions, we analyze the full probabilistic distribution of the target variable:
- **Standard Methods**: Using established probabilistic modeling techniques.
- **CARD**: Conditional Autoregressive Density estimation using **Treeffuser**, allowing for flexible and accurate density modeling.

### Hyperparameter Tuning
[Optuna](https://optuna.org/) is employed to automate the process of hyperparameter optimization. This ensures that the machine learning models are tuned for the best possible performance on the given datasets.

### Quantile Regression
Unlike standard regression which predicts the mean, quantile regression predicts specific quantiles (e.g., median, 10th percentile, 90th percentile). This gives a more complete picture of the potential outcomes and risks.

## Supported Models
The analyses across different methodologies support a wide range of state-of-the-art machine learning models, including:
- **LightGBM**
- **XGBoost**
- **CatBoost**
- **NGBoost**
- **PGBM (Probabilistic Gradient Boosting Machines)**
- **GPBoost (Gaussian Process Boosting)**
- **TabNet**
- **Gradient Boosting**
- **HistGradientBoosting**

## Installation

To run the analyses in this repository, you need Python installed along with several data science and machine learning libraries.

You can install the dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn mapie puncc optuna xgboost lightgbm catboost ngboost pgbm gpboost pytorch-tabnet treeffuser
```

*Note: It is recommended to use a virtual environment or Conda environment to manage dependencies.*

## Usage

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/ML_Analysis_Water_Quality.git
    cd ML_Analysis_Water_Quality
    ```

2.  **Navigate to a Directory**:
    Choose the analysis you want to run. For example, to run the new Conformal Predictions (NEXCP) for EWQI:
    ```bash
    cd "EWQI/Conformal_Predictions(NEXCP,AdaptiveCP,mfcs)"
    ```

3.  **Run the Notebook**:
    Launch Jupyter Notebook or JupyterLab:
    ```bash
    jupyter notebook
    ```
    Then open the corresponding `.ipynb` file (e.g., `Conformal_Predictions(NEXCP, Adaptive CP, mfcs).ipynb`) and run all cells.

---
*Created for the ML_Analysis_Water_Quality project.*

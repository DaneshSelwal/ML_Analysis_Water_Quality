# ML Analysis of Water Quality

## Overview
This project focuses on the Machine Learning analysis of water quality, specifically targeting **EWQI** (Entropy Weighted Water Quality Index) and **WQI** (Water Quality Index). It employs various advanced statistical and machine learning techniques to analyze and predict water quality metrics.

## Project Structure
The repository is organized into two main directories corresponding to the water quality indices:

- **EWQI/**: Contains analysis and data related to Entropy Weighted Water Quality Index.
- **WQI/**: Contains analysis and data related to Water Quality Index.

Each directory follows a similar structure:
- **Conformal Predictions/**: Implementation of conformal prediction intervals using MAPIE and PUNCC libraries.
- **Data/**: Contains the training (`train.csv`) and testing (`test.csv`) datasets.
- **Hyperparameter Tuning/**: Notebooks for hyperparameter optimization using Optuna.
- **Probabilistic Distribution/**: Analysis of probabilistic distributions of the data.
- **Quantile Regression/**: Implementation of quantile regression models.

## Methodologies
This project utilizes several key methodologies:

### 1. Conformal Prediction
Uses **MAPIE** and **PUNCC** to generate prediction intervals with guaranteed coverage, providing a measure of uncertainty for the predictions.

### 2. Hyperparameter Tuning
Employs **Optuna** for automated hyperparameter optimization to enhance model performance.

### 3. Probabilistic Distribution
Analyzes the underlying probability distributions of the water quality parameters.

### 4. Quantile Regression
Estimates the conditional quantiles of the response variable, offering a more complete view of the possible relationships between variables.

## Prerequisites
To run the notebooks in this repository, you will need the following:
- Python 3.x
- Jupyter Notebook or JupyterLab

### Required Libraries
Install the necessary Python packages using pip:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn optuna mapie puncc
```
*Note: Make sure to check the specific import statements in the notebooks for any other dependencies.*

## Usage
1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
2. Navigate to the project directory:
   ```bash
   cd ML_Analysis_Water_Quality
   ```
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open the desired notebook from the `EWQI` or `WQI` directories (e.g., `EWQI/Conformal Predictions/Conformal Predictions(MAPIE,PUNCC)_EWQI.ipynb`) and run the cells.

## Data
The data for this project is located in the `Data/` subdirectory of each main folder (`EWQI` and `WQI`). It consists of `train.csv` and `test.csv` files used for model training and evaluation.

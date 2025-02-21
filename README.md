# MLFramework

## Table of Contents
- Introduction
- Installing the Required Packages
- Jupyter Notebook
- Implementation
- How to Cite

## Introduction

This repository contains a Jupyter notebook that demonstrates a machine-learning (ML) framework for predicting the Vickers hardness of Refractory High-Entropy Alloys (RHEAs) using experimental data from Laser Powder Bed Fusion (L-PBF) processes. The framework guides users through setting up a supervised regression problem, including feature generation, feature selection, and model selection, with a focus on optimizing alloy design through data-driven methods. 

## Installing the Required Packages

To install the necessary dependencies, run the following command:

```bash
pip install -r requirements.txt
```

Alternatively, you can install individual packages as needed by checking the imports in the notebook.

## Jupyter Notebook

The primary notebook in this repository is `ML_Method_Framework.ipynb`. It includes the entire workflow for predicting the hardness of RHEAs using ML models. Open the notebook using:

```bash
jupyter notebook ML_Method_Framework.ipynb
```

## Implementation

1. Dataset Overview
   - The dataset contains 182 unique RHEA compositions with 11 elemental components.
   - The target property is Vickers hardness (HV), ranging from 347 HV to 782.75 HV.

2. Feature Engineering
   - The initial dataset had 3,372 features, which were reduced using Recursive Feature Elimination (RFE), Mutual Information (MI), and Pearson Correlation Coefficient (PCC).
   - The final model uses 6 key features derived from composition-based feature vectors (CBFV).

3. Model Selection and Evaluation
   - Evaluated regression models include:
     - Random Forest Regression (RFR)
     - CatBoost
     - Kernel Ridge Regression (KRR)
     - Support Vector Regression (SVR)
     - LASSO, Ridge, and Polynomial Regression
   - Hyperparameter tuning was done using GridSearchCV with k-fold cross-validation (k=5 and k=10).
   - Metrics used for evaluation:
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - Root Mean Squared Error (RMSE)
     - R-squared (R2)

## How to Cite

If you use this framework in your research, please cite:

Sofia Sheikha, Raymundo Arróyave, "Predicting Hardness in Refractory High-Entropy Alloys Using Machine Learning," *Materials Letter*, January 2025.

```bibtex
@article{sheikha2025predicting,
  title={Predicting Hardness in Refractory High-Entropy Alloys Using Machine Learning},
  author={Sofia Sheikha, Raymundo Arróyave},
  journal={Materials Letter},
  year={2025}
}
```

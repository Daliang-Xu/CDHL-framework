# Research article
A cross-domain hybrid learning framework for unified prediction and mechanistic insights into disinfection by-products

# Authors
Peng Liu, Daliang Xu, Hangbin Xu, Yufei Cheng, Yanyan Liu, Feng Li, Deyin Hou, Heng Liang, Sui Zhang

# Description

This repository contains the datasets, data-processing scripts, model-development code, trained CDHL-Q framework, and model-interpretation workflows used in this study.

1.Dataset_Origin.xlsx
Original dataset before missing-value imputation. It contains literature-derived data and experimental data used in this study.

2.Dataset_DFT.xlsx
Processed modeling dataset obtained after k-nearest-neighbor imputation. Four density functional theory descriptors, namely single-point energy, highest occupied molecular orbital energy, lowest unoccupied molecular orbital energy, and energy gap were added.

3.Imputation.ipynb
Code for missing-value processing and comparison of six imputation methods: Random start, Median interpolation, MissForest, K-nearest neighbors, Bayesian regression and Multivariate imputation by chained equations.

4.CDHL-Q.ipynb
Main notebook for developing and evaluating the CDHL-Q framework. It includes dataset loading, training–testing dataset partitioning, preprocessing-pipeline construction, Bayesian hyperparameter optimization, 10-fold cross-validation, independent testing-set evaluation, and robustness assessment using 20 repeated random train–test splits.

5.best_params.json
Optimized hyperparameters selected for the final CDHL-Q model.

6.scaler_columns.json
Names of the numerical input features standardized during model development.

7.final_CDHLQ.pkl
Serialized trained CDHL-Q framework containing the fitted preprocessing pipeline and the optimized prediction model. The file can be loaded directly for prediction and SHAP interpretation without retraining the framework.

8.Interpretation.ipynb
Model-interpretation workflow based on the trained CDHL-Q framework and the training dataset. It includes SHAP-value calculation, SHAP summary plots, grouped SHAP summary plots, and sample-level SHAP force plots.
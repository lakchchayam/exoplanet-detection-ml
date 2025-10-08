# Exoplanet Detection using Machine Learning

## Project Overview
This project detects exoplanets — planets outside our solar system — using light curve data from NASA’s Kepler mission. The objective is to classify observations as exoplanet or non-exoplanet using machine learning models.

## Problem Statement
Given flux measurements from telescope observations, predict whether an observation corresponds to an exoplanet. The challenge is distinguishing true planetary signals from noise and other astrophysical effects.

## Dataset
* **Source:** NASA Kepler Mission  
* **Training data:** `exoTrain.csv`  
* **Test data:** `exoTest.csv`  
* **Features:** `FLUX.1` to `FLUX.3197` (light curve flux values)  
* **Target:** `LABEL` (0 = not exoplanet, 1 = exoplanet)  

## Methods
* **Data preprocessing:**  
  * Filled missing values with zero  
  * Converted `LABEL` to binary (0/1)  
  * Reduced memory usage using `reduce_memory` function  
* **Data visualization:**  
  * Class distribution plot  
  * Flux intensity line plots  
  * Gaussian histograms for sample observations  
* **Handling imbalance:**  
  * SMOTE for oversampling the minority class  
* **Feature scaling:** StandardScaler or normalization  
* **Machine learning models:**  
  * Logistic Regression  
  * Random Forest Classifier  
  * Support Vector Machine (SVM)  
  * XGBoost Classifier (optional)  
* **Model evaluation:**  
  * Accuracy  
  * F1-Score  
  * Precision  
  * Recall  
  * ROC-AUC  
  * Confusion Matrix  

## Results
| Model | Accuracy | F1-Score |
|-------|---------|----------|
| Logistic Regression | 86% | 0.84 |
| Random Forest | 92% | 0.90 |
| SVM | 88% | 0.86 |
| XGBoost | 91% | 0.89 |

**Best Model:** Random Forest Classifier with 92% accuracy

## Key Insights
* Transit depth and flux variance are the strongest predictors of exoplanet presence  
* Ensemble models handled noisy and imbalanced data effectively  
* Memory optimization and preprocessing improved training efficiency  

## Tech Stack
* Python  
* Pandas  
* NumPy  
* Scikit-learn  
* Imbalanced-learn (SMOTE)  
* Matplotlib  
* Seaborn  
* SciPy  

## Requirements


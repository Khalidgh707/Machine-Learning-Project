
# DS-471 Machine Learning Project: Energy Efficiency Prediction
Predicting the heating load of buildings from their shape and glazing, using the UCI Energy Efficiency dataset (ENB2012).
This is a supervised regression problem
* Course: DS471 Machine Learning, College of Computing and Informatics
* CRN: 10700
### Group members
  
* (Khalid A ALghamdi, ID:210038421)

* (Fahad Alkhamees, ID:220033879)

* (Abdullah S Almutairi, ID:230031752)

 ### Dataset: 
* Dataset: UCI Energy Efficiency (768 simulated buildings, 8 inputs, 2 outputs)
* Target: `heating_load` (Y1). The other output, `cooling_load` (Y2), is not used as an input.

## Run the notebook in Google Colab
[Open in Colab](https://colab.research.google.com/drive/1TxArhvFamRfFedOyZ18lNFSpiJRrERfZ?usp=sharing)



When the data cell asks for a file, upload `data/ENB2012_data.xlsx` from the report or from this link

[download dataset](https://archive.ics.uci.edu/dataset/242/energy+efficiency)

# Project stages
1. **Data cleaning, preparation and EDA**: missing values, duplicates, outliers, one-hot encoding, correlations, feature importance.
2. **Data splitting**: 70% train / 15% validation / 15% test (stratified by bins of the target).
3. **Model selection**: Ridge (Linear) Regression, Random Forest, Neural Network.
4. **Training and tuning**: Grid Search with 5-fold cross-validation, Early Stopping, training/validation curves.
5. **Final evaluation**: MAE, MSE, RMSE and R2 on the test set.


## Models
| Model | Main settings |
|---|---|
| Linear Regression / Ridge | alpha tuned by grid search (best 0.1) |
| Random Forest | 300 trees, max_depth 20, min_samples_leaf 1 |
| Neural Network (scikit-learn MLPRegressor) | hidden layers 128-64, ReLU, Adam, Early Stopping |


## Test results
| Model | MAE | RMSE | R2 |
|---|---|---|---|
| Random Forest | 0.334 | 0.499 | 0.998 |
| Neural Network | 0.659 | 0.950 | 0.992 |
| Linear Regression | 2.110 | 2.847 | 0.925 |
| Ridge Regression | 2.112 | 2.848 | 0.925 |

**The Random Forest is the most suitable model for this dataset**.

## Repository structure
```
DS471ML_project.ipynb   main notebook (run top to bottom)
data/ENB2012_data.xlsx          dataset
figures/                        figures created by the notebook
results/                        result tables (CSV)
README.md
```

## Run locally
```
jupyter notebook DS471ML_project.ipynb
```




## Course:
### DS471



## Deadline:
### 30/11/2026



## Data source
Tsanas, A. and Xifara, A. (2012). Accurate quantitative estimation of energy performance of residential buildings using statistical machine learning tools. Energy and Buildings. Dataset from the UCI Machine Learning Repository.



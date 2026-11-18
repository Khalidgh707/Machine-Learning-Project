
# DS-471 Machine Learning Project: Energy Efficiency Prediction
Predicting the heating load of buildings from their shape and glazing, using the UCI Energy Efficiency dataset (ENB2012).
This is a supervised regression problem
* Course: DS471 Machine Learning, College of Computing and Informatics
* Dataset: UCI Energy Efficiency (768 simulated buildings, 8 inputs, 2 outputs)
* Target: `heating_load` (Y1). The other output, `cooling_load` (Y2), is not used as an input.

## Run the notebook in Google Colab
https://colab.research.google.com/drive/1TxArhvFamRfFedOyZ18lNFSpiJRrERfZ?usp=sharing
Open in Colab


When the data cell asks for a file, upload `data/ENB2012_data.xlsx` from the report or from this link

https://archive.ics.uci.edu/dataset/242/energy+efficiency.

# Project stages
1. **Data cleaning, preparation and EDA**: missing values, duplicates, outliers, one-hot encoding, correlations, feature importance.
2. **Data splitting**: 70% train / 15% validation / 15% test (stratified by bins of the target).
3. **Model selection**: Ridge (Linear) Regression, Random Forest, Neural Network.
4. **Training and tuning**: Grid Search with 5-fold cross-validation, Early Stopping, training/validation curves.
5. **Final evaluation**: MAE, MSE, RMSE and R2 on the test set.

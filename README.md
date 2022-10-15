# credit-defaults-forecasting
One of the most simple and popular consumer finance products is an Unsecured Personal Loan. Competition in the market is strong and margins are slim so the product has to be well prepared. To be able to offer the right price for the customer The Lender has to know what is the cost of lending and a big part of that cost comes from non-performing loans. The purpose of this notebook is to build a contemporary credit scoring model to forecast credit defaults for unsecured lending, by employing machine learning techniques.

## Installation:

To run this notebook interactively:

1. Download this repository in a zip file by clicking on this [link](https://github.com/Mieczmik/credit-defaults-forecasting/archive/master.zip) or execute this from the terminal:
`git clone https://github.com/Mieczmik/credit-defaults-forecasting.git`
2. Install [virtualenv](http://virtualenv.readthedocs.org/en/latest/installation.html).
3. Navigate to the directory where you unzipped or cloned the repo and create a virtual environment with `virtualenv env`.
4. Activate the environment with `source env/bin/activate`
5. Install the required dependencies with `pip install -r requirements.txt`.
6. Execute `ipython notebook` from the command line or terminal.
7. Click on `credit-defaults-forecasting.ipynb` on the IPython Notebook dashboard and enjoy!
8. When you're done deactivate the virtual environment with `deactivate`.

## The analysis was made in the following steps:
### Data Preprocessing

In order to avoid overfitting models (without feature selection xgboost classifier was overfitted), achieve greater computational efficiency, reduce the occupied memory space, eliminate unnecessary and duplicate information, one of the feature selection methods was used: **SelectFromModel**.
In addition resample dataset (generate synthetic samples with **SMOTE** and undersampling data with **RandomUnderSampler**) was used to combat imbalanced training.

* Importing Data with Pandas
* Data Review using **[pandas-profiling](https://pandas-profiling.ydata.ai/docs/master/index.html)** library
* Cleaning Data
* Creating Pipelines for Numerical and Categorical Data assembled from
  + Numeric/Categorical Column Selector
  + Missing Data Replacement has benn done with **SimpleImputer**
  + Data Standarization with **StandardScaler**
  + Join both pipelines using **ColumnTransformer**
  + Resampling dataset: generate synthetic samples with **SMOTE** and undersampling data with **RandomUnderSampler**,
  + Feature Selection with **SelectFromModel**

### Data Analysis
Griding solutions with cross-validation (**Stratified k-fold**) together with **F1-score** for imbalanced data and **Pipeline** assembled with preprocessing pipeline and the following models:
  + Linear Support Vector Classifier
  + Logistic Regression
  + k-Nearest Neighbors
  + Decission Tree Classifier
  + Random Forest
  + Bagging Classifier
  + Extra Trees Classifier
  + Adaptive Boosting (AdaBoost)
  + Gradient Boosting
  + Extreme Gradient Boosting (xgboost)
### Summary
* Feature importance
* Plotting results
* Export results

### Conclusions
* The solution work with a pretty good total accuracy of 88% and f1-score of 76% for Adaboost Classifier,
* Recall-score, which represents the ratio of people expressed as a percentage that the algorithm predicted would default to the number of people who defaulted was 76%,
* Trees algorithms such as AdaBoost and xgboost achieved the best results. One reason is the lower sensitivity to outliers.

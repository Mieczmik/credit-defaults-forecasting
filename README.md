### forecasting-credit-defaults
One of the most simple and popular consumer finance products is an Unsecured Personal Loan. Competition in the market is strong and margins are slim so the product has to be well prepared. To be able to offer the right price for the customer The Lender has to know what is the cost of lending and a big part of that cost comes from non-performing loans. The purpose of this notebook is to build a contemporary credit scoring model to forecast credit defaults for unsecured lending, by employing machine learning techniques.

**Quick Start:** [View](http://nbviewer.ipython.org/urls/raw.github.com/Mieczmik/forecasting-credit-defaults/main/forecasting-credit-defaults.ipynb) a static version of the notebook in the comfort of your own web browser.

### Installation:

To run this notebook interactively:

1. Download this repository in a zip file by clicking on this [link](https://github.com/Mieczmik/forecasting-credit-defaults/archive/master.zip) or execute this from the terminal:
`git clone https://github.com/Mieczmik/forecasting-credit-defaults.git`
2. Install [virtualenv](http://virtualenv.readthedocs.org/en/latest/installation.html).
3. Navigate to the directory where you unzipped or cloned the repo and create a virtual environment with `virtualenv env`.
4. Activate the environment with `source env/bin/activate`
5. Install the required dependencies with `pip install -r requirements.txt`.
6. Execute `ipython notebook` from the command line or terminal.
7. Click on `forecasting-credit-defaults.ipynb` on the IPython Notebook dashboard and enjoy!
8. When you're done deactivate the virtual environment with `deactivate`.

#### This Notebook will show basic examples of:
#### Data Preprocessing
* Importing Data with Pandas
* Data Review using [pandas-profiling](https://pandas-profiling.ydata.ai/docs/master/index.html) library
* Cleaning Data
* Creating Pipelines for Numerical and Categorical Data assembled from
  + Numeric/Categorical Column Selector
  + Missing Data Replacement with Imputer
  + Data Standarization with StandardScaler
  + Join both pipelines using ColumnTransformer
  + Feature Selection
#### Data Analysis
Training listed below machine learning models using GridSearchCV and Pipelines:
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
#### Summary
* Feature importance
* Plotting results
* Export results

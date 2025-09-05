## fraud-detection-case-study
Fraud Detection Case Study: Identifying Credit Card Fraudulent Transactions.

### Packages to install
* __Note__: An Ubuntu 18.04 environment was utilized for the case study.
* Python 3.12 environment.
* Manual installation
    * ```pip install autogluon --extra-index-url https://download.pytorch.org/whl/cpu```
    * ```pip install dython```
    * ```pip install imbalanced-learn```
    * ```pip install notebook```
* __OR__ from requirements.txt file
    * ```pip install -r requirements_python_3_12.txt``` 



### Case Study Description
#### Introduction:
In this case study, we will explore a fraud detection problem using a dataset containing information about credit card transactions. The goal is to build a model that can accurately classify transactions as fraudulent or benign based on various features associated with each transaction.

#### Dataset Description:
The dataset consists of the following columns:

| Column Name      | Description                                                                                  |
|------------------|----------------------------------------------------------------------------------------------|
| step             | Maps a unit of time in the real world. 1 step = 1 hour of time.                             |
| Customer         | Unique customer ID associated with each transaction.                                         |
| zipCodeOrigin    | The zip code of the transaction's origin/source.                                             |
| Merchant         | The unique ID of the merchant involved in the transaction.                                   |
| zipMerchant      | The zip code of the merchant.                                                                |
| Age              | Categorized age of the customer:<br>- 0: <= 18<br>- 1: 19–25<br>- 2: 26–35<br>- 3: 36–45<br>- 4: 46–55<br>- 5: 56–65<br>- 6: > 65<br>- U: Unknown |
| Gender           | Gender of the customer:<br>- E: Enterprise<br>- F: Female<br>- M: Male<br>- U: Unknown      |
| Category         | Category of the purchase.                                                                    |
| Amount           | The amount of the purchase.                                                                  |
| Fraud            | Target variable: 1 if transaction is fraudulent, 0 if benign.                               |


#### Objective:
The main objective of this case study is to develop a predictive model that can accurately identify fraudulent credit card transactions based on the provided dataset.

#### Key Steps for consideration:
* __Data Preprocessing__:
    * Handle missing values, if any, using appropriate techniques.
    * Encode categorical variables (Age, Gender) using techniques such as one-hot encoding.
    * Split the dataset into features (independent variables) and the target variable (Fraud).

* __Exploratory Data Analysis (EDA)__:
    * Explore the distribution of the target variable (Fraud) to understand the class imbalance.
    * Analyze the distribution of features and their relationships with the target variable.
    * Visualize trends, patterns, and potential outliers in the data.

* __Feature Engineering__:
    * Create new relevant features if possible, such as the time of day from the 'step' column.
    * Normalize or scale numerical features as needed.

* __Model Selection__:
    * Choose appropriate machine learning algorithms for fraud detection, such as Random Forest, Gradient Boosting, Logistic Regression, or Neural Networks.
    * Set up a suitable evaluation metric considering the class imbalance, such as F1-score or Area Under the ROC Curve (AUC-ROC).

* __Model Training__:
    * Split the dataset into training and testing subsets.
    * Train the selected models on the training data.

* __Model Evaluation__:
    * Evaluate the models using the chosen evaluation metric on the test data.
    * Compare the performance of different models and select the best-performing one.

* __Model Interpretation__:
    * Interpret the model's predictions and identify the key features influencing fraud detection.

* __Handling Imbalance__:
    * Implement techniques to address class imbalance, such as oversampling, under sampling, or using synthetic data generation (SMOTE).

* __Fine-tuning and Optimization__:
    * Optimize hyperparameters of the selected model for better performance.

* __Key deliverables__:
    * Push the final model code to a Github and share the link.
    * Create a PowerPoint explaining the steps you have considered and why.
     Create recommendations and key outcomes which can be presented to the business teams.


### Case study stages
* __Data Exploration__
* __Baseline experiment stage__:
    * Feature engineering
    * Train/validation/test split
    * Modeling:
        * Logistic Regression
        * XGBoost
        * Autogluon AutoML Tabular Predictor (ensemble of models)
* __SMOTE experiment stage__:
    * Feature engineering (adding SMOTE to train set)
    * Modeling:
        * Logistic Regression
        * XGBoost
        * Autogluon AutoML Tabular Predictor (ensemble of models). 
* __Temporal features experiment stage__:
    * Feature engineering (adding temporal features)
    * Modeling:
        * Logistic Regression
        * XGBoost
        * Autogluon AutoML Tabular Predictor (ensemble of models).

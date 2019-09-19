# Portfolio_projects
This repository acts as a link to many projects where I have applied machine learning algorithms

----------------------------------------------------
BASIC EXERCISES
---------------------------------------------------
# 1. classification evaluation metrics

In this project, I have demonstrated my understanding of various evaluation metrics for classification problems, like the precision-recall curves, roc/auc curve, confusion metrics.
- This project is just for udnerstanding the eval meterics in detail
- Dataset used is breast_cancer dataset in sklearn.datasets

For detailed analysis, click https://github.com/pat-123/misc/blob/master/notebooks/classification_eval.ipynb

# 2. Predicting Boston Housing Prices using Linear Regression

In this project I investigated the performance and predictive power of a model that has been trained and tested on data collected from homes in suburbs of Boston, Massachusetts. A model trained on this data that is seen as a good fit could then be used to make certain predictions about a home — in particular, its monetary value. This model would prove to be invaluable for someone like a real estate agent who could make use of such information on a daily basis.

Implemented the model using Linear, Ridge and Lasso Regression & achieved a root mean square error of 2.94
For detailed analysis, click https://github.com/pat-123/misc/blob/master/notebooks/linear_regr_house_sales.ipynb

# 3. Predicting measure of disease progression one year after baseline

using the sklearn inuilt diabetes dataset, I have demonstrated the overfit, underfit issue

For detailed analysis, click https://github.com/pat-123/misc/blob/master/notebooks/linear_regr_diabetes.ipynb

# 4. Implementing NaiveBayes

This project is just an exercise to understand naive bayes. I have used the in-built algorithm to get probaility values and then calcuated conditional probabilities manually to match with the former.
Dataset is dummy dataa and 80% model score is acheived in classification of this problem set

For detailed analysis, click https://github.com/pat-123/misc/blob/master/notebooks/naive_bayes.ipynb

# 5. Classification on IRIS dataset

- used scatterplot to visualize the decision boundary
- Used SVC to classify with an accuracy of 96% at best 
- Use varying values for gamma and regularization

For detailed analysis, click https://github.com/pat-123/iris

# 6. DecisionTree pruning and xgboosting

Here I have used dummy dataset to see my model overfits on training data, but fails to perform on test set(very poor performance). I have tried decision tree pruning along with n_estimators and max_features, to avoid the overfit and then see a drastic performance improvement in testing data as well, infact it has better score on test than training

- Also on the same dataset, I have used GradientBoostingClassifier and XGBoostClassifier and observed best performance with max_depth paramter adjusted

For details, click https://github.com/pat-123/misc/blob/master/notebooks/DecisionTree_Pruning_and_XGBoost.ipynb

# 7. Prinicipal component analysis

I have tried to build a model by removing multicollinear variables by checking the vif between independent variable(manually), and also with in-built variation_inflation_factor() and got a model score on sklearn breast cancer dataset to be 0.733

Another way I tried with PCA to reduce the dimensions from 30 to 2 and then see a visual on the decision boundary and model score improved a little because of standardization

For details, click https://github.com/pat-123/misc/blob/master/notebooks/Multi-collinearity%20and%20PCA.ipynb

--------------------------------------------------------------------------
Intermediate Projects
--------------------------------------------------------------------------
# 1. Predicting survival of passengers on the Titanic dataset

In this project I investigated a dataset containing information about Titanic passengers by using NumPy and Pandas, which are two popular Python packages used for manipulating datasets. The goal of this project was to get acquainted with said tools, learn about the different data structures (NumPy Arrays, Series and DataFrames) they offer,and practice the key steps on the whole data analysis process.
- I have used RandomForest, SVM, NaiveBayes and Randomforest performs best with an average of 0.82 with 5 folds, with a max of 0.86
## key points
- Sex determined the survival rate the most(females the most), followed by Passengerclass(pclass=1), then family size(3,4,5) were the most important features
- Model performs poor(0.79) without age and Fare properly cleaned(converting continous range to discrete categories). These both are the key features of this accurate prediction and needs to be handled properly
- When age and fare was continous variables, trees would be having if else conditions and more the range, more the branches/splits would be there and the significance of that variable gets reduced
Hence when you have a numeric variable with fewer number of values, its best to convert to str type(object) and treat it accordingly, which results in better predictions(since these variables were significant)
- Hyper-parameter tuning also helps in getting better perfomance
- For detailed analysis, click https://github.com/pat-123/Titanic

# 2. Predicting sales for bigmart
This is a regression problem, where predict the sale contribution of each sale item towards the overall outlet sale.
There are ten independent variables which predict the dependent variable Item_Outlet_Sale
## Key points
- This dataset is heavy on categorical variables and model score depends on how well the chosen sub-categories describe the sale of outlet
  - This project is heavy on bar graphs and visualizations
  - Feature engineering was critical in getting a better score without these new engineered features
- It was challenging to see, which particular food items or non consumables contribute more as compared to others in the same category and include those to increase the model score
- Overall the Item_Outlet_Sales is curvier rather than linear relation, and hence linearregression wont do much good
  - Acheived a model score of 0.55 with rmse of 0.17
  - LinearRegression works best when you have few features with more weightage than the rest, as opposed to randomforest whihc gives equal importance to all features and picks features randomly(and performance score also is very less)

### Modular code
- Place all the utility functions used by this project in custom made utils package
- All the common imports are placed under bigmart package
- For detailed analysis, click https://github.com/pat-123/bigmart

# 3. Credit card fraud detection
This project is about predicting the no of defaulters who will not pay the credit card bill next month
## Key points
- The target class 'default' is highly imbalanced
- undersampling vs oversampling
  - undersampling : 
    - Generally if we have variables contained with in a small range, we can depend on a sub sample from our training set to represent our dataset and take positive cases equal to the negative ones 
    - This way the result will be same as if drawn on actual population
    - I saw that except for 1 variable, we have low standard deviations, which suggests we can go undersampling as well, but due to that one variable in which the std is too high, if we take a undersample, then we have high chance missing some part of teh distrubution.
  - oversampling :
    - Here we artificially create samples of positive class which are in minority, to balance out the class distribution
    - But since these values are aritifically generated, the result will be based on if the probability of either class is equal(since they are equal in no), whereas the actual distribution is largely imbalanced towards the negative class and we will see a huge difference in predictions also
    - Since the standard dev of LIMIT_BAL is huge(>10k) and none of them are outliers, I chose oversampling
- Few variables are already given as normalized  
- Few variables like age,sex,marriage,education is given as numeric, but actually are categorical(fewer unique values)
  - Sex = 1 has more defaulters than others
  - People towards retirement(55-60 years) and people who just started their carriers(20-25) are more defaulters
  - Marital status has nothing to do with non payment
  - Customers with Education = 1 are good customers, customers with education=3 are highest defaulters
- RandomForestClassifier performs the best with auc= 0.92 , model score = 0.86
### Modular code
- Place all the utility functions used by this project in custom made utils package
- All the common imports are placed under credit_card package
- For detailed analysis, click https://github.com/pat-123/credit_card_fraud

# 4. Santander customer transaction
This project is about predicting if a customer will do transaction or not in future(irrespective of the amount of transaction)
## Key points
- With the predictions, we are more intrested to find out customers who are likely to make a transaction rather than the people who will not.
- So basically we are focussing on positive cases the model can identify i.e. the recall(sensitivity) rather than specificity(True negative rate)
- And it would cost a lot to loose on customers who are likely to make a transaction, i.e. False negative rate should be low(which is labeled as negative but they were actually positive
So our focus is to get a model with high recall and low FNR, rather than specifity and FPR.
- cons of oversampling: If we have say 90-10 in negative-positive cases, then our predictions are actually expected to be more in negative cases, in actual data or even in synthetic minority oversampling techiniq(SMOTE), but what happens in reality is that if prop is made to 50-50, then the predictions of negative and positive classes also becomes more balanced, which doesnt represent the real scenario
- cons of undersampling: we may loose on signifcant information from the samples which we didn't include in the test , if deviation in the variable is more
- naivebayes performs best with 0.88 model score with undersampling 
- with oversampling we get 0.92 with randomforest, naive bayes stops at 0.89

### Modular code
- Place all the utility functions used by this project in custom made utils package
- All the common imports are placed under Santander package
- For detailed analysis, click https://github.com/pat-123/Santander

# 5. cab fare prediction
This project is about predicting the fare of a cab ride, given the coordinates of pick/drop off, along with the pickup timestamp
## Key points
- pickup timestamp analysis
Derived information like was the ride took on a weekend, month end/start, peak night times(10pm-4AM) , peak evening hours(5pm-8pm) , afternoon times or any other normal times, year end, year start
  - The rides on month start/end had higher average fares . Peak night times had greater fares slightly than peak evening hours in any time of the month
  - only evening rides in month start showed a little rise in price, followed by noon times in month start and ending
    - so overall  month start/end and peak night times recorded highest fares
    - Peak night times(11pm-4AM) recorded the highest mean fare
    - day/weekday has no effect
    - seasons have no effect either
    - time of the day like early morning or peak evening times had higher fares than the rest
    - Also year wise also, higher fares are seen towards 2014,2015
- Linear Regression performs the best with model score 0.71 average over 2 iterations, rmse = 0.15
- XGBRegressor performs better with model score slighly improved
### Modular code
- Place all the utility functions used by this project in custom made utils package
- All the common imports are placed under cab_fare package
- For detailed analysis, click https://github.com/pat-123/cab_fare


## NOTE : Overall the intermediate projects are in a structured format, basically in python modules 

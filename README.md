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

--------------------------------------------------------------------------
Intermediate Projects
--------------------------------------------------------------------------
# 1. Predicting survival of passengers on the Titanic dataset

In this project I investigated a dataset containing information about Titanic passengers by using NumPy and Pandas, which are two popular Python packages used for manipulating datasets. The goal of this project was to get acquainted with said tools, learn about the different data structures (NumPy Arrays, Series and DataFrames) they offer,and practice the key steps on the whole data analysis process.
- I have used RandomForest, SVM, NaiveBayes and Randomforest performs best with an average of 0.82 with 5 folds, with a max of 0.86
## key points

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
- used utils package to place all the utility functions used by this project
- All the common imports are placed under bigmart package
- For detailed analysis, click https://github.com/pat-123/bigmart

# 3. Credit card fraud detection
## Key points
### Modular code
- used utils package to place all the utility functions used by this project
- All the common imports are placed under bigmart package
- For detailed analysis, click https://github.com/pat-123/bigmart

# 4. Santander customer transaction
## Key points
### Modular code
- used utils package to place all the utility functions used by this project
- All the common imports are placed under bigmart package
- For detailed analysis, click https://github.com/pat-123/bigmart

# 5. cab fare prediction
## Key points
### Modular code
- used utils package to place all the utility functions used by this project
- All the common imports are placed under bigmart package
- For detailed analysis, click https://github.com/pat-123/bigmart


## NOTE : Overall the intermediate projects are in a structured format, basically in python modules 

# Neural-Networks-Using-Gas-Turbine-Dataset
This code performs a binary classification task using a gas turbine dataset. It predicts whether the turbine would generate more or less than 134 MW of energy based on the input features. The code uses a neural network built with the Keras API and performs hyperparameter tuning using grid search with cross-validation.

Here's a breakdown of the code:

The necessary libraries are imported.

The dataset is read into a pandas DataFrame.

The mean value of the target variable (TEY) is calculated.

The target variable is binarized based on a threshold value of 134 MW.

The value counts of the target variable are displayed to check for class imbalance.

Information about the DataFrame is displayed to check for missing values and data types.

The input and target variables are separated and split into training and testing sets using train_test_split() from scikit-learn.

The training set is standardized using StandardScaler() from scikit-learn.

A function create_model() is defined that creates a neural network model with two hidden layers, dropout regularization, and the given hyperparameters.

A KerasClassifier wrapper is created for the model to enable it to be used with scikit-learn's grid search.

The hyperparameters to be tuned are defined using a dictionary.

Grid search with cross-validation is performed using GridSearchCV() from scikit-learn.

The best score and best parameters found by grid search are printed.

The mean test scores and standard deviations for each parameter combination are extracted from the grid search results.

A plot of the mean test scores and standard deviations is displayed to visualize the results of grid search.

The code can be improved by adding more layers, changing activation functions, and experimenting with different hyperparameters. The model's performance can also be further evaluated by calculating additional evaluation metrics such as precision, recall, and F1 score.

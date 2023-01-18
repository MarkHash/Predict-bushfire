# ML models to predict bushfire
This project produces multiple ML models predicting bushfires based on forest fires data.

## Background
Due to the devastating bushfires in Australia, bushfires are major envnrionmental issues, creating economic and ecological damages. Because of traditional human surveilance is expensive and inefficient, machine learning with a variety of data about the forest has a potential to detect potential bushfires to make effective and efficient firefighting plans.

This project is to develop several ML models for predicting the burned area of a bushfire and compared their performance.

## Dataset
- Dataset can be downloaded from https://archive.ics.uci.edu/ml/machine-learning-databases/forest-fires/
- Description of dataset can also be downloaded from https://archive.ics.uci.edu/ml/machine-learning-databases/forest-fires/forestfires.names

## Installation
A list of packages to install:

```
- sklearn
- matplotlib
- numpy
- pandas
- seaborn
- smogn
```

## Models
This project explores the following models and its parameters:

- Naive average predictor: strategy: ‘mean’
- Multiple regression: LinearRegression class
- Decision tree: criterion: ’squared_error’
- Random forest: Criterion: absolute_error, Max_depth: 3, max_features: sqrt, n_estinators: 500
- Neural network: MLPRegressor class with parameters hidden_layer_sizes:(4,), activation:'logistic', solver:'lbfgs', max_fun:300
- Support vector machine: default parameter
- Bagging regressor: Max_samples: 1.0, n_estimators: 50
- AdaBoost regressor: Learning_rate: 1.0, n_estimators: 50
- Stacking regressor: Knn__n_neighbors: 6, tree__max_depth: 5

## Performance metrics
This project uses RMSE (Root mean square error) as a performance metric.
The best performance metrics (RMSE score: 43.612) is with Bagging regressor and with the following features to train.

- four weather conditions (‘temp’, ‘RH’, ‘wind’, ‘rain’)


# House-Value-Prediction-Kaggle-
House Value Prediction(Python)

## Introduction:

The goal of this project is to predict  saleprice of houses based on features like total square feet,year built or remodelled, overall quality etc. The data used is the data from kaggle's 'House Prices: Advanced Regression Techniques' prediction competition.

Multiple regression techniques were used on the train data to find the best model with lowest mean squared error.

The tool used is Python 3 along with its libraries and packages such as numpy, pandas, matplotlib, seaborn and sklearn to do data manipulation, data visualization and building the predictive model

## Exploratory Data Analysis(EDA):
### Visualizing Target Variable
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/target%20variable.png)
In the target variable's plot there were some suspicious potential outliers. 1.5 IQR rule was used to find the upper and lower bound of suspected outliers. After careful examination all data was retained.

### Correlation between numerical features and the target variable
A heatmap was plotted on correlation between all the numeric variables and  features that are highly correlated with the target variable were selected. A heatmap of these features were plotted for a better understanding
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/heatmap.png)
The scatter and bar plots of numeric and categorical features respectively were plotted against the target variable the following plots were obtained
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/grvlivarea.png)
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/totalbsmtsqft.png)
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/fullbath.png)
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/garagecars.png)
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/overallqual.png)
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/yearbuilt.png)
![myimage-alt-tag](https://github.com/Ahsana-Ahffan/House-Value-Prediction-Kaggle-/blob/master/images/yearremodadd.png)

##Missing Values
80 features of the dataset has missing values.PoolQC had the highest percentage of missing values(99.6%),followed by Miscfeature(96.4%),Alley(93.2%),Fence(80.4%) and so on. All the missing values are handled by replacing them with None,median or mode. Only the feature utilities was dropped.

## Model Selection and Evaluation:

The six different regreesion algorithms selected were
1.Linear Regression
2 Random Forest Regression
3.Gradient Boosting Regression
4.ElasticNet Regression
5.Lasso Regression
6.BayesianRidge

Root Mean Squared Error is selected as the evaluation metric. The model with lowest rMSE is selected has the best model.

### Best Model
After doing 5 fold cross validation on each selected models, the following rMSE was measured for corresponding models
1.Linear Regression- 383973048.26582015
2 Random Forest Regression-81912.54959754692
3.Gradient Boosting Regression-383973048.26582015
4.ElasticNet Regression-81414.7368470685
5.Lasso Regression-90625.05465575153
6.BayesianRidge-79282.3309428574

## Conclusion
The rMSE can be improved a lot and I am still working on it to get a better model


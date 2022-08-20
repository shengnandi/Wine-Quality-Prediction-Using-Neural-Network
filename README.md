# Wine-Quality-Prediction-Using-Neural-Network

The wine quality prediction project is essentially a kind of classification or regression task. The quality score range from 0 to 10, and the samples of normal wines are much more then the poor ones. The task aims to use these features to predict the quality score of the wine. 
This dataset is also available from the UCI machine learning repository [https://archive.ics.uci.edu/ml/datasets/wine+quality]
The dataset contains 11 physiochemical properties: fixed acidity (g[tartaric acid]/dm3),volatile acidity (g[acetic acid]/dm3), total sulfur dioxide (mg/dm3), chlorides (g[sodium chloride]/dm3), pH level, free sulfur dioxide (mg/dm3), density (g/cm3), residual sugar (g/dm3), citric acid (g/dm3), sulphates (g[potassium sulphate]/dm3), and alcohol (vol\%)

## Data Analysis

We conduct data visualization, correlation analysis, PCA analysis, and Shapiro test in File Code/machine-learning-for-red-wine-prediction.ipynb
The result shown as following

##Data visualization:
![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/2.png)

##Correlation analysis:
It indicates that there are some positive linear correlations between those variables. For example:  "Fixed acidity" and "Density" ,  "Fixed acidity" and "Citric acid", "Fixed acidity" and "pH", "Volatile acidity" and "Citric acid" ,"Total sulfur dioxide" and "Free sulfur dioxide"

![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/1.png)

##PCA analysis: 
We use PCA decomposition to test the importance of the random variables.
![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/3.png)

Shapiro test: 
The Shapiro test can inform whether the variables follow a normal distribution. After the Shapiro test, we can find out the density and ph features are more likely from a normal distribution.
![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/4.png)
![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/5.png)


## Model Training
Training data is used for this part to train models. In order to find the best model, 5 different commonly-used models are trained: Lasso Regression Model, Elastic Net Regression Model, Light GBM, Regression Tree and Random Forest.
Linear regression is a simple but effective approach to identify the relationship between predictors and dependent variables. But because the number of variables in dataset is relatively large, therefore, lasso regression is chosen as base model since it can select parameter automatically by regularization. Elastic Net regression is also trained showing a different way to constraint the parameters. Tree method is really powerful in practice because it’s easy to implement and explain. Besides some advanced models including Light GBM and Random Forest are used in this report in order to get a better result on training data.
All those models are trained using Scikit-Learn package.

## Comparison

![avatar](https://github.com/shengnandi/Machine-Learning-Project-Airbnb-Prediction-/blob/main/picture/4.png)





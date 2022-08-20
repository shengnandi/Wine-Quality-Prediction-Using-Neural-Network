# Wine-Quality-Prediction-Using-Neural-Network

The wine quality prediction project is essentially a kind of classification or regression task. The quality score range from 0 to 10, and the samples of normal wines are much more then the poor ones. The task aims to use these features to predict the quality score of the wine. 
This dataset is also available from the UCI machine learning repository [https://archive.ics.uci.edu/ml/datasets/wine+quality]
The dataset contains 11 physiochemical properties: fixed acidity (g[tartaric acid]/dm3),volatile acidity (g[acetic acid]/dm3), total sulfur dioxide (mg/dm3), chlorides (g[sodium chloride]/dm3), pH level, free sulfur dioxide (mg/dm3), density (g/cm3), residual sugar (g/dm3), citric acid (g/dm3), sulphates (g[potassium sulphate]/dm3), and alcohol (vol\%)

## Data Analysis

We conduct data visualization, correlation analysis, PCA analysis, and Shapiro test in File Code/machine-learning-for-red-wine-prediction.ipynb
The result shown as following

## Data visualization:

![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/2.png)

## Correlation analysis:

It indicates that there are some positive linear correlations between those variables. For example:  "Fixed acidity" and "Density" ,  "Fixed acidity" and "Citric acid", "Fixed acidity" and "pH", "Volatile acidity" and "Citric acid" ,"Total sulfur dioxide" and "Free sulfur dioxide"

![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/1.png)

## PCA analysis: 
We use PCA decomposition to test the importance of the random variables.

![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/3.png)
![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/4.png)

## Shapiro test: 

The Shapiro test can inform whether the variables follow a normal distribution. After the Shapiro test, we can find out the density and ph features are more likely from a normal distribution.

![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/5.png)


## Result Comparison 

Here we use Accuracy, Precision, Recall, F1-Score, ROC-AUC to measure the performance.

![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/6.png)
![avatar](https://github.com/shengnandi/Wine-Quality-Prediction-Using-Neural-Network/blob/main/picture/7.png)



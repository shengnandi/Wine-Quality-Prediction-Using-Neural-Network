# Wine-Quality-Prediction-Using-Neural-Network
## Data Preprocessing & Data Transformation

By looking at the histogram of original price (left plot above), it indicates that the distribution is high right-skewed. 
In order to reduce the variability of predicted model, log-transformation should be done and it shows that the distribution is approximate to normal distribution after this transformation.
![avatar](https://github.com/shengnandi/Machine-Learning-Project-Airbnb-Prediction-/blob/main/picture/1.png)
### Outliers Analysis
Outliers were identified by looking at the scatter plot created for all numerical variables against price. As outliers can severely influence the model stage and introduce the bias to the model, 2 outliers from “security deposit” are removed across all variables. Dropping these outliers can help increase the accuracy of the model.
![avatar](https://github.com/shengnandi/Machine-Learning-Project-Airbnb-Prediction-/blob/main/picture/2.png)
### Dealing with Geographic Featuress
The dataset contains geographic features “longitude” and “latitude, and by using these two features every room can be located.
From the above graph it indicates the location is highly correlated with the room price, but most machine learning algorithm cannot fully capture this geographic features. Therefore, instead of using “latitude” and “longitude” directly, the K-cluster method is used to transfer this geographic features into a categorical variable that allocate each observation into a cluster with the nearest mean.
![avatar](https://github.com/shengnandi/Machine-Learning-Project-Airbnb-Prediction-/blob/main/picture/3.png)

## Model Training
Training data is used for this part to train models. In order to find the best model, 5 different commonly-used models are trained: Lasso Regression Model, Elastic Net Regression Model, Light GBM, Regression Tree and Random Forest.
Linear regression is a simple but effective approach to identify the relationship between predictors and dependent variables. But because the number of variables in dataset is relatively large, therefore, lasso regression is chosen as base model since it can select parameter automatically by regularization. Elastic Net regression is also trained showing a different way to constraint the parameters. Tree method is really powerful in practice because it’s easy to implement and explain. Besides some advanced models including Light GBM and Random Forest are used in this report in order to get a better result on training data.
All those models are trained using Scikit-Learn package.

### Tuning

The choose of parameters determines the performance of models on the training data and test data. Ridge Regression and Regression Tree are used as example here.
Lasso Regression has a regularized parameter alpha, which weights the L2 norm term. If the alpha value is 0, it means that it’s just an Ordinary Least Squares Regression model. So, the larger is the alpha, the higher is the smoothness constraint. From the following graph, it shows that when alpha equals to 1, the predictability on the test data is the strongest.

![avatar](https://github.com/shengnandi/Machine-Learning-Project-Airbnb-Prediction-/blob/main/picture/4.png)





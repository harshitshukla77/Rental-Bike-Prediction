# Rental-Bike-Prediction

# Problem Statement
The increasing demand for rental bikes in urban areas presents a unique opportunity to optimize bike distribution and availability. However, accurately predicting the demand for rental bikes poses several challenges due to the influence of various factors such as weather conditions, time of day, holidays, and socio-economic events. This project aims to develop a predictive model that can forecast the number of bikes rented at a particular time enabling rental services to optimize their operations.

# Project Summary
The Seoul Bike Sharing Demand Dataset provides data on the number of rented bikes for every hour of the day in Seoul, South Korea, from December 2017 to November 2018. The data is useful for understanding bike rental trends and predicting bike rental demand.
The first phase of the project involved data wrangling. I have changed the Date column to datetime object that will help in EDA as well as modelling. Found out that around 295 rows of data had 0 Rented Bike Count since it was non functioning day. So we have dropped those rows so as to make data more consistent.

In the second phase, I conducted exploratory data analysis (EDA) to identify trends and patterns in the data. Some of the important findings are: demand for rented bikes increases as temperature increases to a certain level, demand was higher during non-holiday days, demand was lowest during winter and highest during summer, rainfall and snowfall had a negative impact on demand, demand is high during rush hours of the day etc. I used different types of charts like histogram, Box Plot, Scatter Plot, Line Chart, Bar Chart, Correlation Heatmap etc.

Next, I conducted hypothesis testing to validate my findings from EDA. I used two-sample t-tests to test whether rented bike demand was higher in hot weather and during rush hour. I also used one-way ANOVA tests to test whether rented bike demand was different in different seasons. The results of these tests confirmed my findings from EDA.

The fourth phase involved feature engineering. I have capped the Rainfall and Snowfall columns to categorical value like 0 for no snowfall and rainfall, and 1 value tell that there is rainfall and snowfall. I also used one-hot encoding for categorical features like Seasons, Holiday, and Functioning. Using the correlation matrix and heatmap I found out that the temperature and dew point temperature columns have very high co-relation among them and this could lead to multicolinearity so I dropped the dew point temperature column. After that I applied data scaling to some columns that needed it using methods like StandardScaler and MinMaxScaler.

Next, I used five different machine learning models – Linear Regression, KNN Regressor, Decision Tree, Random Forest, and Decision Tree Regressor – to predict rented bike demand. Using GridSearchCV and RandomSearchCV, I tuned the hyperparameters for each model and used cross-validation to evaluate their performance. Hyperparameter optimized Random Forest Regressor gave the best results, with an of 0.94.

In conclusion, this project shows that bike rental demand in Seoul is influenced by weather conditions, day of the week, and season. To increase bike rental demand, companies can focus on promoting bike rental during good weather, non-holiday days, summer season etc. In addition to that, companies can use the insights gained from this project to optimize their rental pricing and inventory management.


# Technologies Used

• Programming Language: Python

• Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

• Model Deployment: GitHub

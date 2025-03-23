### Big Mart sales data analysis
# Source : https://www.kaggle.com/datasets/brijbhushannanda1979/bigmart-sales-data?select=Train.csv

# Problem statement: 
A supermarket chain called Bigmart has several outlets or several stores around the world & they want us to predict the sales which they can expect.
# Steps taken: 
1. Data cleaning: Replacing missing numerical value in Item_Weight column with mean value, replacing missing non mumerical value in Outlet_Size        column with mode.(Found 4 seperate mode based on Outlet_Type columns) 
2. Data visualization: Graphical representaion of all columns, found issue in Item_Fat_Content columns, Low fat and regular data was entered with other names as LF and ref, corrected the error and standerdised the data.
3. Label encoding: Converted non numerical columns to numerical data so that ML model can process it.
4. Train test split: Spliting data into features and target and then spliting into training and testing data, which we will use to train our ML model and evaluate it.
5. ML model training and evaluation: We trained 3 ML models( XGBRegressor, Multiple linear Regressor and Polynomial Regressor) and evaluated them with  root mean square error value. XGBoost regressor model performed best with value of 0.55 in rmse, but initially it was overfitted to training data and thus we had to reduce the sample size that model was being trained with by redcing the value in colsample_bylevel, colsample_bynode and colsample_bytree.
6. Conclusion: This we have our ML model ready to forecast future sales value.


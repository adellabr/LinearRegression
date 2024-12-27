# LinearRegression
Implementation a Python class for a linear regression algorithm with two basic methods — fit and predict

Answer the questions

Derive an analytical solution to the regression problem. Use a vector form of the equation.
What changes in the solution when L1 and L2 regularizations are added to the loss function.
Explain why L1 regularization is often used to select features. Why are there many weights equal to 0 after the model is fit?
Explain how you can use the same models (Linear regression, Ridge, etc.) but make it possible to fit nonlinear dependencies.



Introduction — make all the preprocessing staff from the previous lesson

Import libraries.
Read Train and Test Parts.
Preprocess "Interest Level" feature.



Intro data analysis part 2

Let's generate additional features for better model quality. Consider a column called "Features". It consists of a list of highlights of the current flat.
Remove unused symbols ([,], ', ", and space) from the column.
Split values in each row with the separator "," and collect the result in one huge list for the whole dataset. You can use DataFrame.iterrows().
How many unique values does a result list contain?
Let's get acquainted with the new library — Collections. With this package you could effectively get quantity statistics about your data.
Count the most popular functions from our huge list and take the top 20 for this moment.
If everything is correct, you should get next values:  'Elevator', 'HardwoodFloors', 'CatsAllowed', 'DogsAllowed', 'Doorman', 'Dishwasher', 'NoFee', 'LaundryinBuilding', 'FitnessCenter', 'Pre-War', 'LaundryinUnit', 'RoofDeck', 'OutdoorSpace', 'DiningRoom', 'HighSpeedInternet', 'Balcony', 'SwimmingPool', 'LaundryInBuilding', 'NewConstruction', 'Terrace'.
Now create 20 new features based on the top 20 values: 1 if the value is in the "Feature" column, otherwise 0.
Extend our feature set with 'bathrooms', 'bedrooms', 'interest_level' and create a special variable feature_list with all feature names. Now we have 23 values. All models should be trained on these 23 features.



Models implementation — Linear regression

Implement a Python class for a linear regression algorithm with two basic methods — fit and predict. Use stochastic gradient descent to find optimal model weights. For better understanding, we recommend implementing separate versions of the algorithm with the analytical solution and non-stochastic gradient descent under the hood.
Define the R squared (R2) coefficient and implement a function to calculate it.
Make predictions with your algorithm and estimate the model with MAE, RMSE and R2 metrics.
Initialize LinearRegression() from sklearn.linear_model, fit the model, and predict the training and test parts as in the previous lesson.
Compare the quality metrics and make sure the difference is small (between your implementations and sklearn).
Store the metrics as in the previous lesson in a table with columns model, train, test for MAE table, RMSE table, and R2 coefficient.




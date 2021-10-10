# insurance-cross_sell
**Summary** <BR>
In this case, we were asked to predict if an existing policy-holder will be interested to buy Motor Insurance from the same company. We were provided with various parameters of individual customers and using that information we needed to predict the individual’s behaviour. It always makes sense for any company to allocate its resources to only interested customers as every communication strategy is tied with a certain price. Thus, to optimize a company’s resources, Predictive Modelling using Machine Learning is very important.
While undertaking this project, I removed the duplicate values present in the dataset and did some basic EDAs. I found out that the dataset was highly imbalanced in terms of the dependent variable, “Response”. Moreover, a few of the columns such as “Driving License” was also imbalanced with the majority of the people possessing a Driving License. Hence, I removed the mentioned column. For removing the imbalance present in the “Response” column, I tried to implement the “SMOTE” technique.
Also, one of the important features of this dataset was the presence of columns such as “Age” and “Annual Premium” which could affect our model thus I tried to make them discrete by assigning them in Bins by performing Descritization. I also did Mean Encoding on the policy Channel for getting average positive responses per channel. One-hot encoding was done for other categorical variables available within our dataset. At final stage for preparation of data, I scaled “Vintage” column.
Chi-square test was conducted to check the applicability of categorical values in our model. All the categorical variables available had their p-value below threshold levels thus suggesting that we can use all our models for prediction purposes.
In the model implementation part, we started with Logistic Regression and then proceeded to Decision Tree, Random Forest, Naive Bayes, Light GBM and Xtreme GBM. I also tried Hyper tuning the various parameters available.  At the end I also tried to implement Stacking by keeping Logistic Regression, Random Forest and Light GBM at the Level 0 and keeping XGBM at the Level 1.
I tried to have stronger Recall values for class 1 as the company should not miss any potential customer.
The ROC-AUC scores for the model prediction ranged between 80 to 90% with XGBM giving us better results. 
One of the biggest challenge observed while modeling was the huge time taken for fitting and cross validation due to Huge Dataset.
Overall, we can implement XGBM for prediction purposes

Summary
Project : Lead Score case Study
Project Overview:
An education company X Education identifies people who show interest and share personal details as lead. The problem was to improve the lead conversion rate of X Education, from current rate of 30%. It wants to make lead conversion process more efficient by identifying the most potential leads, also known as Hot Leads The company intent to build a model to assign a lead score to each lead so that customers with a higher lead score have a higher conversion chance.
Data Cleaning:
o Columns with >40% nulls were dropped. Value counts within categorical columns were checked to decide appropriate action: if imputation causes skew, then column was dropped, created new category (others), impute high frequency value, drop columns that don’t add any value.
o Numerical categorical data were imputed with mode and columns with only one unique response from custome were dropped.
o Other activities like outliers’ treatment, fixing invalid data, grouping low frequency values, mapping binary categorical values were carried out.
EDA:
o Data imbalance checked- only 38.5% leads converted.
o Performed univariate and bivariate analysis for categorical and numerical variables. ‘Lead Origin’, ‘Current occupation’, ‘Lead Source’, etc. provide valuable insight on effect on target variable.
o Time spend on website shows positive impact on lead conversion.
Data Preparation:
o Created dummy features (one-hot encoded) for categorical variables
o Splitting Train & Test Sets: 70:30 ratio
o Feature Scaling using Standardization
o Dropped few columns, they were highly correlated with each other
Model Building:
o Used RFE to reduce variables from 48 to 15. This will make dataframe more manageable.
o Manual Feature Reduction process was used to build models by dropping variables with p – value > 0.05.
o Total 3 models were built before reaching final Model 4 which was stable with (p-values < 0.05). No sign of multicollinearity with VIF < 5.
o logm4 was selected as final model with 12 variables, we used it for making prediction on train and test set.
Model Evaluation:
o Confusion matrix was made and cut off point of 0.345 was selected based on accuracy, sensitivity and specificity plot. This cut off gave accuracy, specificity and precision all around 80%. Whereas precision recall view gave less performance metrics around 75%.
o As to solve business problem CEO asked to boost conversion rate to 80%, but metrics dropped when we took precision-recall view. So, we will choose sensitivity-specificity view for our optimal cut-off for final predictions
o Lead score was assigned to train data using 0.345 as cut off.
Making Predictions on Test Data:
o Making Predictions on Test: Scaling and predicting using final model.
o Evaluation metrics for train & test are very close to around 80%.
o Lead score was assigned.
o Top 3 features are
1. Lead Source_Welingak Website
2. Lead Source_Reference
3. Current_occupation_Working Professional
Recommendations:
o More budget/spend can be done on Welingak Website in terms of advertising, etc.
o Incentives/discounts for providing reference that convert to lead, encourage to provide more references.
o Working professionals to be aggressively targeted as they have high conversion rate and will have better financial situation to pay higher fees too.

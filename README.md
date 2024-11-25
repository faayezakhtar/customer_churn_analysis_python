## Customer Churn Analysis Project
### Aim
* The aim of this project to use customer attributes provided by local bank data to predict customers that are at high risk of churning and customers that are at low risk of churning

### Project background
* Banks operate in really competitive markets. As such, things such as brand loyalty are extremely important - not only to maintain a steady flow of revenue but also contribute to network effects that can lead to demand side economies of scale and help the bank establish a presence in the market.
* To inspire brand loyalty and use word of mouth for network effects, the bank needs to build a good reputation and tailor deals and programs to customers. Predicting churn rates allows banks to identify factors that lead to churn, tailor programs to deal with these factors, limit churn and consequently establish a good reputation. That brings us to the need for a model that accurately predicts customers at risk of churning i.e. the aim of this project. 

### Data structure
* 10,000 observations and 14 columns

### Column description:
* RowNumber
* CustomerId
* Surname
* CreditScore - Customer's credit score
* Geography - Geographical location
* Gender (male, female)
* Age
* Tenure - number of years the person was a customer at that bank
* Balance - Account balance
* EstimatedSalary - Estimated salary
* NumOfProducts - Number of products that a customer purchased through the bank
* HasCrCard - Credit card status (whether or not a customer has a credit card)
* IsActiveMember - Active member status (whether or not the person is an active bank customer)
* Exited - Whether a customer has left the bank or not (response variable)

### Report structure
#### Data set overview
 
 a. Exploring shape of data
	
 b. Checking for class imbalance in data

#### Data cleaning and transformation
	
 a. Renaming columns for ease of use + relevance
	
 b. Identifying and dropping duplicates
	
 c. Identifying and dropping NA values

#### Exploratory data analysis (EDA)
	
 a. Descriptive statistical analysis (numerical variables)
	
 b. Checking numerical var distribution (histograms) (checking for normality assumption needed in hypothesis testing)
	
 c. Hypothesis testing
		
  i. Difference in means test to verify validity of a "generalized conclusion" on impact of EstimatedSalary on churn rate
		
  ii. Chi-square hypothesis test to verify validity of a "generalized conclusion" on impact of CountryofOrigin on churn rate
	
 d. Feature engineering
	
  i. One-hot encoding for to create dummy var for the categorical var
	
  ii. Creating bins for the numerical variables to better interpretation of var by the model
	
  iii. Standardizing Tenure var

#### Model building

 a. Creating train and test data set
	
 b. Fitting Logistic Regression, Random Forest 1, Random Forest 2, and LightGBM model (Random Forest 1 & 2 are both RF models with different hyperparameter values)

#### Evaluation and Model selection

 a. Utilizing ROC-AUC, accuracy, precision, and recall metrics to evaluate models

 b. Utilizing cross validation to calculate mean evaluation metric values for each model and subsequently determine best model

 c. Plotting confusion matrix


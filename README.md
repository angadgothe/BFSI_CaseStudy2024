The objective is to build a statistical model to estimate borrowers’ LGD.
As a business analyst working for a bank, you have been tasked with developing a model that can estimate borrowers’ LGD. 
To develop this model, you have been provided with relevant data sets that include information about defaulted accounts and the amount of money that has been retrieved from them using collaterals and other collection methods. 
Details about the data sets are provided in subsequent sections.


Understand the business problem deeply in the context of the current business and domain.
Define your business objective. For this assignment, you need to build a model that can predict the loss given default (LGD) for defaulted accounts and evaluate it based on the performance metric that will be described in the subsequent segments.
Thoroughly understand the data sets provided to you and familiarise yourself with the variables in the data set, data types and data distribution. Ensure that you have a thorough understanding of the target variable, which is the LGD of the accounts, and how it is calculated. The collection data is provided in a separate data set and needs to be aggregated and merged to gather relevant information. It is essential to ensure that the data types of the variables are identified correctly, as Python is notorious for running into errors owing to datatype mismatch errors.
Clean and pre-process the data. This includes handling missing values, outliers and any other issues that may affect the model's performance. Also, perform any necessary feature engineering or feature extraction to create new variables that may be useful for the model.
The target variable LGD is not specified directly and, hence, needs to be calculated. Calculate the LGD using the following formula:

The LGD would be represented as a decimal value ranging from 0 to 1. The value represents the proportion of the total loan amount that is expected to be lost in the event of default. A value of 0 indicates that no loss is expected, whereas a value of 1 indicates that the entire loan amount is expected to be lost. The collateral value and collected amount through repayments need to be utilised to calculate this.

Use any appropriate statistical or machine learning technique to develop a model for predicting the borrowers’ LGD.
Once the model is built, the next step is to evaluate its performance. For this purpose, you will be provided with a separate test data set that does not include the repayment data. The collateral value will be provided in this test data set as well. Run the model on the test data set and submit the predicted LGD values. Submit your workings in the form of a Jupyter Notebook.
Articulate the model’s implications for the bank's business operations - specifically, its ability to enhance risk management and compliance with regulatory standards such as Basel norms. Summarise the results of the analysis, highlighting successes and areas for improvement, as well as potential avenues for further improvisation.
Note that although the scope of the assignment is confined to calculating the LGD only, it would be beneficial to understand how the expected credit loss (ECL) is calculated and used to determine the amount of provisioning required. Understand the role of the probability of default (PD) and the loss given default (LGD) in the ECL calculation.

The three datasets can be merged using the loan_acc_num as the common key. The information from these datasets can be combined to get a more complete picture of the loan accounts, including the repayment history for each account.
Caution: When you merge the main_loan_base and repayment_base datasets, it should be noted that not all accounts present in the main_loan_base will have corresponding entries in the repayment_base. This results in the presence of null values in the merged data set, which must be properly handled before you proceed with the calculation of the loss given default (LGD) metric. Failure to address these null values may result in errors during the LGD calculation process.
 

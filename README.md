# Bank_Marketing_Campaign_Data_Analysis_Using_Python-Logistic_Regression-

## I have used Bank Campaign Marketing dataset for doing analysis of it and applied Logistic regression upon to classify new  customers if they will ready to opt for deposit or not based upon current campaign data.
## I have included Final Cleaned excel file named(Modeling_Dataset.xlsx) which i have used for applying Logistic Regression as well as python jupyter notebook (Banking_Marketing_Data_Logistic_Regression.ipynb).

### Python Libraries need to Install:

* pandas
* sklearn
* numpy
* matplotlib
* xlrd

### Data Understating:

* Our Dataset is about bank marketing campaign where they are marketing term deposit to their customer.
* Dataset contains various details about customer information as well as campaign related information.
* There are total 10,000 observations and 17 variables in dataset below is brief description about each variables:

#### Age: Age of customer.
#### Job: Contains customer job type such as categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown'
#### Marital: Marital status of customer contains divorced, married, single , unknown
#### Education: What is education of customer contains primary, secondary, tertiary and unknown
#### Default: Customer has default has or not contains yes, no and unknown
#### Housing: Customer has housing loan or not contains yes and no
#### Loan: Customer has any other loan or not contains yes and no
#### Balance: Customer bank balance
#### Contact: During term deposit campaign how customer were contacted contains cellular, telephone and unknown
#### Day: Contains last contacted day of month to customer all 1 to 30/31 day of month
#### Month: Contains last contacted month of year to customer all months of year
#### Duration: During Campaign for how many seconds of duration customer talked
#### Campaign: During campaign how many times customer were contacted.
#### Pdays: number of days that passed by after the client was last contacted from a previous campaign
#### Previous: number of contacts performed before this campaign and for this client
#### Poutcome: outcome of the previous marketing campaign contains failure, success, other and unknown
#### Deposit: Contains yes and no if customer made customer deposit than yes otherwise no.

### Data Cleaning: 

* Our dataset is not having any missing values.
* Some of columns like job, education and contact are having unknown values we assume that those values exist because some customer may not want to disclose this information.  By Removing those unknown values we can loose other useful records of that whole row. So,  We will keep them.
* Out of all columns or variables we are going to remove columns like Blank Column_Name, Month, Day, Poutcome, Pdays  and Previous using Access which we will not require for future analysis. 

### Identify Business Questions:

* Highlight of this banking marketing dataset is that after running campaign how many customer agreed to make term deposit and how many not.
* Customer’s who is  ready to make and who is not ready to make term deposit:

 #### what is age of those customer?
 #### How much bank balance they have?
 #### How many number of times they have been contacted during campaign?
 #### What is time duration of call?
 #### What is their marital status?
 #### Which type of job they have?
 #### What is their education? 
* By finding all this patterns in both type of customer who made term deposit and not made term deposit bank can make future decision about in next marketing campaign which type of customer need to target.
* So, based upon all this we can conclude that for finding relationship between two variables our dependent variable is deposit which is yes if customer made and no if customer has not and any of  these independent variables like bank balance, marital status, number of time contacted , duration for they talked, type of job and what is their education level.

### Data Pre-Processing:

* Target variable deposit is categorical so we will convert it into 0 for “no” and 1 for “yes” using Excel.
* Some of independent variable are categorical variable like job, marital, education, default, housing, loan and contact.
* For doing Logistic regression we need to convert them into numerical values.
* In Python to apply logistic regression on categorical variables get_dummies() function is available inside Pandas library which will create additional variable of each categorical variables and  fill it’s values with 0 and 1 dummies. For Example, in case of marital variable it will create marital_married,  marital_divorced and marital_single than fill each of this variables with 1 and 0.Likewise for each categorical variable.
* In R also same like python there is one function dummy_cols function is available inside fastDummies library which does same thing will create additional variable of each categorical variables and  fill it’s values with 0 and 1 dummies. 

### Interpreting Python Model :

* In case of python From Accuracy of our logistic regression model it says that out of all term deposit that were marketed in campaign 78% of them liked by customer and subscribed for it.  
* From above results we can say that Bank may rely on this model if they apply same marketing campaign on targeted customer there are 78% of probability that bank can predict weather a customer will subscribe for term deposit or not.

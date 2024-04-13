# Data Analytics Customer Segmentation

## Goal of the project
The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing a RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions. In this analysis the customer segment was divided into 11 groups. The analysis will help in determining which customers segments should be targeted in order to enhance sales revenue for the company.

## Analysis Approach
### 1. Data Quality Assessment and Data Cleaning
The first step towards generating useful insights from the data was the data prepartion, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset and identification customer purchasing behaviours to generate insights can be performed.

In the data cleaning step the data quality of the following datasets were first assesed. After a data quality assessment the following data quality issues was observed and the necessary process to mitigate the issue was followed :
### [CustomerDemographics_data_cleaning(click_here)](https://github.com/kiransuryaa/Data_Analysis_customer_segmentation-RFM-/blob/main/data_cleaning_customer_demographic.ipynb)
  - 1 Irrelevent column was present and such columns were dropped from the dataset.
  - There were 5 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values
  - For gender column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
  - The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution. An <b>outlier</b> was observed and the record was removed.
  - Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.
    
### [NewCustomerList_data_cleaning(click_here)](https://github.com/kiransuryaa/Data_Analysis_customer_segmentation-RFM-/blob/main/Data_cleaning_new_customer_data.ipynb)
  - 5 Irrelevent column was present and such columns were dropped from the dataset.
  - There were 4 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values
  - The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution.
  - There was no data inconsistency.
  - Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

### [Transaction_data_cleaning(click_here)](https://github.com/kiransuryaa/Data_Analysis_customer_segmentation-RFM-/blob/main/Data_cleaning_transaction_data.ipynb)
  - The product_first_sold_date column is not in datetime format. The data type of this column was changed from int64 to datetime format.
  - There were 7 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values
  - A new feature column 'Profit' was created which is basically the difference between list price and standard price.
  - There was no data inconsistency.
  - Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

### [CustomerAddress_data_cleaning(click_here)](https://github.com/kiransuryaa/Data_Analysis_customer_segmentation-RFM-/blob/main/Data_cleaning_customer_address_data.ipynb)
  - For states column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.

### 2. [Exploratory Data Analysis on Customer Segments(click_here)](https://github.com/kiransuryaa/Data_Analysis_customer_segmentation-RFM-/blob/main/customer_RFM_analysis.ipynb)
  After the data cleaning process, exploratory analysis on the dataset is performed and the following insights are obtained :
- <b>New vs Old Customers Age Distribution</b><br> 
    - Most New / Old Customers are aged between 40-49. The lowest age groups are under 20 and 80+ for Old and New Customers respectively.
    - Among the New Customers the most populated age bracket is 50-59, while the maximum Old Customers are from the age bracket 30-39.
    - There is a steep drop in number of customers in 70-79 age groups among the New Customers.

 - <b>Bike purchases over last 3 years by Gender</b><br>
    - Over the last 3 years approximately 51% of the buyers are women and 49% were male buyers.
    - Female purchases are approximately 10,000 more than male (numerically). Gender wise majority of the bike sales comes from female customers.

 - <b>New vs Old Customers Job Industry Distribution</b><br>
    - Among the New Customers the highest amount of sales comes from customers having a job in Manufacturing and Financial services sector. 
    - The samllest chunk of sales comes from customers in Agriculture sector and from Telecom sector with 3% sales only. Similar trend is observed among Old Customers.

- <b>Wealth Segmentation by Age Category</b><br>
    - Across all age categories the largest number of customers are from 'Mass Customer' Segment
    - The next category comes from the 'High Net Worth' customers.
    - In the age group 40-49, Affluent segment out performs the High Net Worth customers in terms of number of customers.

- <b>Cars owned by States</b><br> 
    - New South Wales has the largest number of people who donot own a car.
    - In Victoria the proportion is quite even.
    - In Queensland the number of people owning a car is greater than who donot have a car.

### 3. [RFM Analysis and Customer Segmentation(click_here)](https://github.com/kiransuryaa/Data_Analysis_customer_segmentation-RFM-/blob/main/customer_RFM_analysis.ipynb)
In this stage of analysis the customer segmentation was done by developing an RFM Model. The RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions.

In this analysis the customer segment was divided into 11 groups. The groups being : 
- Platinum Customers
- Very Loyal Customers
- Recent Customers
- Potential Customers
- Lost Customers
- Losing Customers
- Late Bloomer
- High Risk Customers
- Evasive Customers
- Becoming Loyal
- Almost lost Customers
  


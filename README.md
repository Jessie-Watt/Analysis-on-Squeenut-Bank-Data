# Analysis-on-Squeenut-Bank-Data

# **Introduction**
Power BI will be extensively used to analyse squeenut bank dataset to determine the rate at which the bank monitors loan issued to different job sectors, through the marital status of the borrower, the educational level and their individual balance. A dashboard will be created including KPIs using Data Analysis Expressions(DAX) to solve this financial analysis.

# **Activity**
- [ ]  Importation of the ‘Bank Term Deposit Subscription’ dataset into Power BI Desktop
- [ ]  Creating a dashboard to visualize key point indicators of the bank
- [ ]  To create a measure for the ‘Average age of depositors’
- [ ]  To create a new column named ‘Age band’ containing the following; ‘Young’ for ages below 30, ‘Mid-aged’ for ages between 30 and 50 and ‘Old’ for ages above 50
- [ ]  To create a measure calculating the total balance for Job:Technician, and Marital:Single and Married
- [ ]  To create a measure to get the number of depositors on Loan
 

# **Skills Demonstrated**
- Data Importation and data cleaning
- Creating a Dashboard
- Using Dax functions

# **Data Importation and Cleaning**
The bank_full dataset was imported from the 'bank term dataset subscription' it was later renamed to squeenut bank dataset where it was loaded into the power query. The data was cleaned by first captalizing the first letter of all title headers and choosing suitable 'data name' for each column title. The 'Data Type', Data format, 'summarization' and 'category' were all formated to suit the column select. The squeenut bank data was also transformed into the power query editor where the text listed in all rows were capitalized, each column quality, column distribution and column profile was checked to determine values/text distribution, errors, valid rows and empty rows. The first one thousand rows were kept to remove null values.
The raw dataset can be seen here[] while the cleaned squeenut bank data set can also be seen here[]

To calculate the average age of depositors, a DAX measure was used to calculate average age of all depositors. This calculated value was inserted into a card visual. The card visual, callout value, title name and visual was formatted to represent the value as seen below.

![Average age of depositors](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/e39a4204-df3b-4911-8dce-958b715dcf26)

A new column titled 'Age Band' was created to show ‘Young’ for ages below 30, ‘Mid-aged’ for ages between 30 and 50 and ‘Old’ for ages above 50. This was achieved by inserting a new column


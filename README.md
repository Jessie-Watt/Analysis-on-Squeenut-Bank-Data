# Analysis-on-Squeenut-Bank-Data

# **Introduction**
Power BI will be extensively used to analyse squeenut bank dataset to determine the rate at which the bank monitors loan issued to different job sectors, through the marital status of the borrower, the educational level and their individual balance. A dashboard will be created including KPIs using Data Analysis Expressions(DAX) to solve this financial analysis.

# **Activity**
- [ ]  Importation of the ‘Bank Term Deposit Subscription’ dataset into Power BI Desktop
- [ ]  To create a measure for the ‘Average age of depositors’
- [ ]  To create a new column named ‘Age band’ containing the following; ‘Young’ for ages below 30, ‘Mid-aged’ for ages between 30 and 50 and ‘Old’ for ages above 50
- [ ]  To create a measure calculating the total balance for Job:Technician, and Marital:Single and Married
- [ ]  To create a measure to get the number of depositors on Loan
- [ ]  Creating a tracking dashboard to visualize key point indicators of the bank using the ‘Bank Term Deposit Subscription’ dataset.
 

# **Skills Demonstrated**
- Data Importation and data cleaning
- Creating a Dashboard
- Using Dax functions

# **Data Importation and Cleaning**
The bank_full dataset was imported from the 'bank term dataset subscription' it was later renamed to squeenut bank dataset where it was loaded into the power query. The data was cleaned by first captalizing the first letter of all title headers and choosing suitable 'data name' for each column title. The 'Data Type', Data format, 'summarization' and 'category' were all formatted to suit the column select. The squeenut bank data was also transformed into the power query editor to further clean the data where the text listed in all rows were capitalized, each column quality, column distribution and column profile was checked to determine values/text distribution, errors, valid rows and empty rows. The first one thousand rows were kept to remove null values, this gave the dataset a better presentation to work on. The raw dataset can be seen here[] while the cleaned squeenut bank data set can also be seen here[]

To calculate the average function DAX measures was used with syntax format; AVERAGE(column or expression) to calculate average age of all depositors. This calculated value was inserted into a card visual. The card visual, callout value, title name and visual boarder was formatted to represent the value as seen below.

![Average age of depositors](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/e39a4204-df3b-4911-8dce-958b715dcf26)



A new column titled 'Age Band' was created in the table view to show rows containing ‘Young’ for ages below 30, ‘Mid-aged’ for ages between 30 and 50 and ‘Old’ for ages above 50. This was achieved by inserting a calculated column with a measure to determine the age band. The following syntax was used; 'Age Band = IF(Squeenut_Bank[Age]<30,"Young",IF(Squeenut_Bank[Age]<50,"Mid-aged","Old"))'.

![Age Band](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/d86889a1-b57d-4e8d-8e35-69774fc44853)

 Two card visuals were also imported into the report view show ing measures calculating the total balance for Job:Technician, and Marital:Single and Married. Using syntax format: CALCULATE(expression, filter1, filter2, ...). The measure used to aggregate the married and single balance was "Total Balance for Single & Married = CALCULATE(SUM(Squeenut_Bank[Balance]),OR(Squeenut_Bank[Marital] = "Single",Squeenut_Bank[Marital]="Married"))',  while for the technicians was 'Total Balance for Technicians = CALCULATE(SUM(Squeenut_Bank[Balance]), Squeenut_Bank[Job] IN { "Technician" })'. The calculated measures were placed in the card visuals the result is as seen below

![image](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/3c17f6d0-f4d5-4c43-88ce-4c826a3cada6)
![Balance for Technicians](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/d3258c47-4619-4e32-8098-7e1f00f099f4)

A measure to get the total number of depositors on Loan was achieved using the syntax format: CALCULATE(expression, filter1, filter2, ...). This particular syntax was applied in this measure; "Number of Depositors on Loan = CALCULATE(SUM(Squeenut_Bank[Age]), Squeenut_Bank[Loan] IN { "Yes" })". The measure was applied to a card visual with the visual formatted. The total number of depositors on loan can be seen in the card visual below

![image](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/1005080a-4df1-45fd-a705-71ff08ba7fcf)



A tracking dashboard to monitor squeenut bank deposit subscription was developed including the above calculated key point indicators. The total balance for all depositors was calculated using a card visual, this produced an insight of the sixy-two million as the balance to closeout from all depositors, while balance by marital status was also considered, this displayed married depositors to have thirty-nine million as a greater percentage to closeout the total balance margin, followed by singles having seventeen million, and divorce as six million. Hence married individuals should be sent a reminder mail to pay up their balance within the expected duration period. The balance by job type was all visualize showing Management, Blue collar, Technician, Admin and Retired as the hightest balance having job type individuals. A loan slicer was also inserted into the dash to monitor the total loan balance for the marital and job type depositors. The total balance value, balance by marital visual and job type visual can be seen below. The Squeenut Bank dashboard can be viewed here[]


![Screenshot 2023-09-08 102653](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/676b158b-bde7-48bb-953d-e64299a996fd)

![Screenshot 2023-09-08 102529](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/6ca9e64a-0854-40f6-a6b2-6ac64ba4895e)

![Screenshot 2023-09-08 102541](https://github.com/Jessie-Watt/Analysis-on-Squeenut-Bank-Data/assets/140435577/97e24f82-6f44-430b-a8c0-702d0fe2dfc6)





# **Conclusion**
This financial analysis exercise has made it easy to simplify, track and visualize the loan system of the bank, the total balance required from all depositors and the marital status using a dashboard with calculated columns and measures.



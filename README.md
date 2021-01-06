# Tableau_Project_101
Project 101
# Sales Insightes Project


### Problem Statement:

-Computer hardware and Peripheral Manufacturer company that has clients across India 
- Across India they have regional office and their HO is at Delhi.
- Computer hardware market is very dynamic and rapidly evolving, Companies CEO facing challenge in order to keep track of company’s sales across different regions
- From all the regional offices CEO gets data in the form of huge excel files and its nearly impossible for him to go through these excels reports and get any meaningful insights out of the data
- CEO knows overall numbers are declining and he wants to know what are the weakest areas of the company?  
-  Be it a certain product or a region, CEO wants to take a call on how to improve sales and it can be either improving certain underselling product or rolling out an attractive campaign in certain locality to attract more customers… 

### Requirement: 

- CEO is more interested in getting dashboard set-up that will give an overview of companies’ performance in few clicks
- He wants dashboard to easy to understand and dynamic, so that every time he log in into dashboard he gets real time view of the data.

### ETL:
Data Transformation and Exploration:
Company stores all the data in MySQL and we were given access to database. We set up our own Datawarehouse for this project and we did not want to disturb companies’ routine sales process data generation.

Following are data schemas available:
1-	Customers:
-	This table has information about all the customers who has made purchase with the company
-	This is the dimension table

2-	Dates:
-	Table stores all the important dates
-	This is the dimension table

3-	Markets:
-	This table has information about the market in which a particular sale has happened
-	This is the dimension table

4-	Product:
-	This table has information about the product
-	This is the dimension table

5-	Transactions:
-	This is the most important table
-	It contains details about all transactions that has happened so far

![Revenue Analysis_Tableau_1](https://user-images.githubusercontent.com/61430361/103801838-4b9de700-5074-11eb-9d55-47b36db14552.JPG)



As a part of data cleaning process, we performed following operations in Tableau interface:
1)	Markets tables contains details about few markets that are out of the scope for this analysis (New York and Paris), so we removed these details 
2)	Transactions tables there were few transactions which has negative sales values and some of them had 0 as sales value, we were told to remove those as those were the data errors. 
3)	Transactions table also had few duplicate rows, we also removed them
4)	Looking at the required we created few new fields using VIZ language (Total Revenue and Sales Quantity) and stored them in new table BaseMeasure
5)	There were some transaction that happened in USD, using VIZ expression we created new variable Normalised sales and used this in reporting


#Dashboard

### Following are the few key insightes that we provided to the CEO - Based on Year/Month selected  these vaues will dynamically change 
 - Total Revenue
 - Total Sales
 - How is each region performing in terms of Revenue : CEO can do comparitive analysis between top performing and under performing markets, he can understand what top markets doing correctly to get higher revenue and use those stratrgies in out markets
 - How is the sales across mupliple regions
 - What are some top selling products ? can they cross sell ? 
 - Who are top cusomters and how relationship with then can be further improved
 
![Revenue Analysis_Tableau](https://user-images.githubusercontent.com/61430361/103801904-5f494d80-5074-11eb-924f-5f5d1ce72da7.jpg)




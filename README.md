# Sales Documentation
## Project Title: Sales Analysis
---
## Project Outlines

[Project Overview for sales data](#project-overview-for-sale-data)

[Data source](#data-source)

[Tool used](#tool-used)

[Data cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

---
### Project Overview for sales data
The examination of last year's and some of this year's sales performance served as the foundation for this endeavor. After learning a few things from the data, this analysis will help us make an informed decision and show us how well the store is doing.

### Data source
The data used for this analysis was downloaded from my canvas learning management system account (Lita Capstone Dataset.xlsx)

### Tool used  
- Microsoft Excel- This tool was used to clean the dataset 
- SQL Server Management Studio-for querying of the dataset 
- Power BI- for creating dashboard to visual some insights
- GitHub- this is used to build my portfolio as well as document my project

### Data cleaning and Preparation
After opening the dataset, we perform some data cleaning such as
- Adjusting the dataset
- Add another column to the dataset
- Removing some duplicates in the dataset
- Perform some calculation using the conditional excel funtions
- Perform some visuals using pivot table etc
- Data formatting
### Exploratory Data Analysis 
We provide answer some questions on the dataset such as 
- What is the total sales
- Average sale for each product
- Total sales for each region 
- The highest selling product etc

### Data analysis
These are some of the functions and queries used to achieve our analysis
```Excel 
=F4*G4 ENTER
=AVERAGEIF(C4:C9924,C9912,H4:H9924)
=SUMIF(D4:D9924,D4242,H4:H9924)
```
```SQL 
SELECT PRODCUT, SUM(TOTAL_SALE) AS TOTAL_SALE_PER_PRODUCT
SELECT CUSTOMERID, COUNT(CANCELED) FROM [DBO].[LITA CAPSTONE DATASET]
GROUP BY PRODUCT
ORDER BY 1 ASC

SELECT REGION, COUNT(TOTAL_SALE) AS [NO OF SALE TRANSACTION PER REGION]
FROM [DBO].[LITA CAPSTONE DATASET]
GROUP BY REGION
ORDER BY 1 ASC

SELECT TOP 1 PRODUCT, SUM(TOTAL_SALE) AS TOTAL_SALE_PER_PRODUCT
FROM [DBO].[LITA CAPSTONE DATASET]
GROUP BY PRODUCT
ORDER BY 2 DESC

SELECT ORDERDATE, SUM(TOTAL_SALE) AS [MONTHLY SALE FOR CURRENT YEAR]
FROM [DBO].[LITA CAPSTONE DATASET]
WHERE ORDERDATE BETWEEN '2024/01/01' AND 2024/12/31'
GROUP BY ORDERDATE

SELECT REGION, SUM(TOTAL_SALE) AS TOTAL_SALES,
SUM(TOTAL_SALE)*100.0/(2101090) AS PERCENTAGE_SALES_BY_REGION
FROM [DBO].[LITA CAPSTONE DATASET]
GROUP BY REGION
ORDER BY  PERCENTAGE_SALES_BY_REGION DESC
ORDER BY ORDERDATE
```

### Data Visualization
This section contain some screenshots of the outputs of the analysis

- Excel calculation for Sales data
![Calculation for Sale data](https://github.com/user-attachments/assets/5aa8a915-8ff7-4f86-96c5-96e49de64896)

-This showcase the some summary of the data set 
![Pivot Table for sale data](https://github.com/user-attachments/assets/9fe9bf78-4b68-4b61-89d4-7c65a57702f4)

- Using SQL queries to perform some analysis 
![Total Sale per product](https://github.com/user-attachments/assets/35a20098-e91a-4df0-b98e-6ab30615bd64)


![Number of sale transaction](https://github.com/user-attachments/assets/53d4f1a0-ca97-45bc-9322-59f33958d726)


![Highest Selling Product](https://github.com/user-attachments/assets/3537e421-fbc6-4a3f-bbe9-0c97fe6de9cf)


![Total Revenue per product](https://github.com/user-attachments/assets/c1de693f-fcf2-4cc0-8a5b-f9f392731323)


![Monthly Sale total for current year](https://github.com/user-attachments/assets/cbdeb6f3-ead2-4621-9307-fafdacd92aad)


![Top 5 Customer](https://github.com/user-attachments/assets/49ffb68f-615d-4f32-9657-daba1173bbea)


![% of total Sale by region](https://github.com/user-attachments/assets/7e64a5ed-d42e-448c-b8a6-e8d849541eff)


![Product with no sale for last quarter](https://github.com/user-attachments/assets/701ccf70-def7-4410-b654-a8a76553be4a)


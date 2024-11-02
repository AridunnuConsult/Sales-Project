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
SELECT Product, SUM(Total_Sale) from [dbo.Litacapstone Dataset]
Group by Product
Order By desc
```

### Data Visualization
This section contain the screenshots of the outputs of the analysis


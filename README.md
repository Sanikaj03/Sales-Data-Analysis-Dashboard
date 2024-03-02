## Sales Insights Dashboard

## Abstract 
This project focuses on the development of a PowerBI dashboard for analysing sales data obtained from kaggle. This data is of global_superstore which is an ecommerce platform similar to amazon .com. The dashboard aims to provide valuable insights. into various parameters related to sales performance, enabling stakeholders to make informed decisions and optimise business strategies.
The dashboard encompasses a comprehensive analysis of multiple parameters, including :

Sales Trends: Visualising the overall sales trends over a specified time period to identify patterns and seasonal variations.

Product Performance: Analysing the performance of individual products based on factors such as sales volume, revenue generated, and profit margins.

Customer Segmentation: Segmenting customers based on their purchasing behaviour, frequency of purchases, and total spending to target specific customer groups effectively.

Regional Analysis: Evaluating sales performance across different regions or geographical areas to identify high-performing regions and areas for improvement.

Inventory Management: Monitoring inventory levels, identifying product with maximum profit along with those going out-of-stock, and optimising inventory turnover to minimise stockouts and excess inventory costs.


## Steps Followed:

Step 1 : Load data into Power BI Desktop, dataset is a csv file.

Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

Step 3 : It was observed that in none of the columns errors & empty values were present.

Step 4 : There were a total of three tables named “Orders”, “Product”, “Return”.

Step 5 : Few columns were added to the table which were used for generating insights. They were “Delivery days”, “Year”, “Return Orders”. Following is the syntax of dax query for creating these columns:

Delivery Days: first go to power query editor, select create custom column, in that write formula:
= ([Ship Date]-[Order Date])
This will create columns named as delivery days which will show no of days required to deliver the product.

Year:First go to power query editor, select create custom column, in that write formula 
=Date.Year([Order Date])
This will extract the year from the date present in the “Order Date” column.

Return Orders: First go to power query editor, select conditional column, in that with reference to “Returned” column give condition that wherever there is yes in Returned Column, 1  will be obtained in Returned Order column.

Step 6 :  Visual filters (Slicers) were added for the field named  as "Year".

Step 7 : Four card visuals were added to the canvas,representing Sales, Quantity, Average Delivery Days, Returned Order.
Using a visual level filter from the filters pane, basic filtering was used.

Step 8: A bar chart was added showing top 5 products with maximum and minimum profit along with the top 10 customers generating maximum profit.

Step9: A filled map was used to depict the sales trend in various regions around the globe.

Step10: A pie chart and donut chart was added to show the Sum of Sales based on different segments and market respectively. 

## Snap of Dashboard
![overall sales](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/3e8a0030-cbe8-48d8-b841-b3c58f14b13c)

Insights:
Sales in 4 year: $12.64M,

Quantity: 178k,

Avg. Delivery Days: 4,

No. of Returned Orders: 1097,

## Snap of Sales in each year:

## 2012:
![2012](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/be75c850-9ee1-4ed2-aa02-e88be490e5f5)

## 2013:
![2013](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/d9bc70c2-de9a-40e3-bdb0-022e414be9fd)

## 2014:
![2014](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/0a27c31a-9195-4631-8159-fb028fddaff6)

## 2015:
![2015](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/5701ae72-c8cd-4190-b8af-8c772dd0bc1c)

Insights:
from this it can be analysed that sales have increased gradually over in 3 years and are maximum in 2015.

## Snap of Sum of Sales based on region:
![sum of sales by region](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/f31a9795-b5e2-4e84-88f2-4144be2213c1)

## Snap of Sum of Sales based on market:
![sum of sales by market](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/93d38a6d-247b-44fe-8741-9878bad704f6)

Insights:
from this it can be analysed that "Asia Pacific" Market and regions associated with it generates maximum sales while compared to other Markets.

## Snap of Sum of Sales by segment:
![sumof sales by segment](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/9d29d9f1-891e-422b-8848-29a030aa6a19)

Insights:
from this it can be analysed that compared to three segment consumer segment is generating maximum sales to the company.

## Snap of top 5 products generating maximum and minimum profit:
![top 5 products ](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/863ac70c-44ef-439b-8b90-055f84386b2a)


Insights:
from this top 5 products generating maximum and minimum profit can be analysed based on which company can decide which products should it upstock and which should it limited or removed completely.


![Top 10 Customers](https://github.com/Sanikaj03/Sales-Data-Analysis-Dashboard/assets/125180335/cad23585-fb61-4f50-b32b-0eb2d044bab1)


Insights:
from this top 10 Customers giving  maximum profit to the company can analysed based on which company can give some offers and discount to those customers who are their consistent buyers.

# Car Sales Dashboard using Power BI  
Creating a dashboard using POWER BI Tool
## View the Project  
You can view the interactive Car Sales Dashboard [here](https://app.powerbi.com/view?r=eyJrIjoiYzZiMzJmYjctNzYwZi00M2ZiLTljMTQtYWFjYWQ4MjAwMWU2IiwidCI6ImQxNzU2NzliLWFjZDMtNDY0NC1iZTgyLWFmMDQxOTgyOTc3YSIsImMiOjZ9).

---
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
## Project Overview  
This project focuses on building an interactive **Car Sales Dashboard** with Power BI to monitor and analyze sales performance metrics effectively. It delivers meaningful insights into sales patterns, empowering the business to track progress and make data-driven decisions. The dashboard visualizes various KPIs across multiple dimensions, including time, price, regions, and car specifications.

---

## Objectives  
The primary goal is to design a **dynamic sales dashboard** that helps the company assess its performance over different periods. It will uncover trends, highlight growth areas, and provide actionable insights into car sales operations.

---

## Problem Statement  

### 1. KPI Requirements  

The dashboard should focus on **real-time insights** into key performance indicators to enable data-informed decision-making and trend identification. Key metrics include:  

#### Sales Overview:  
- **Year-to-Date (YTD) Total Sales**  
- **Month-to-Date (MTD) Total Sales**  
- **Year-over-Year (YOY) Growth in Total Sales**  
- **Difference between YTD and Previous Year-to-Date (PTYD) Sales**  

#### Average Price Analysis:  
- **YTD Average Selling Price**  
- **MTD Average Selling Price**  
- **YOY Growth in Average Price**  
- **Difference between YTD and PTYD Average Price**  

#### Cars Sold Metrics:  
- **YTD Total Cars Sold**  
- **MTD Total Cars Sold**  
- **YOY Growth in Cars Sold**  
- **Difference between YTD and PTYD Cars Sold**

---

### 2. Visualization Requirements  

To better understand performance trends, several interactive visualizations are needed:  

- **YTD Sales Weekly Trend:**  
  A **line chart** showcasing weekly trends in YTD sales, with weeks on the X-axis and total sales amount on the Y-axis.  

- **YTD Sales by Body Style:**  
  A **pie chart** representing the proportion of YTD sales across different car body styles (e.g., sedan, SUV, etc.).  

- **YTD Sales by Color:**  
  A **pie chart** illustrating the contribution of each car color to YTD sales.  

- **YTD Cars Sold by Dealer Region:**  
  A **map chart** to display the geographic distribution of car sales across various dealer regions.  

- **Company-Wise Sales Trend Grid:**  
  A **tabular view** presenting YTD sales figures for each manufacturer, helping analyze company-wise performance.  

- **Detailed Car Sales Grid:**  
  A **detailed grid view** capturing all relevant sales data, including car model, body style, color, sale amount, dealer region, and sale date for every transaction.

---

## Key Learnings  

- **Using DAX (Data Analysis Expressions):**  
  DAX is a powerful formula language used in Power BI to create custom calculations. For example, to calculate the Year-to-Date (YTD) Total Sales, you might use the following DAX expression:
  ```dax
  YTD Total Sales = CALCULATE(SUM(Sales[TotalSales]), DATESYTD(Sales[Date]))
  ```

- **Adding Relationships in Power BI:**  
  Relationships between tables in Power BI are established in the **Model** view. For instance, to link a **Sales** table to a **Cars** table using a common **CarID**:
  1. Go to the **Model** view.
  2. Drag the **CarID** field from the **Sales** table to the **CarID** field in the **Cars** table.
  3. Ensure that the relationship type is set correctly (e.g., one-to-many).


- **Creating a Calendar Table using the CALENDAR function:**  
  Creating a calendar table is essential for time-based analysis. You can create a calendar table with the following DAX code:
  ```dax
  CalendarTable = CALENDAR(MIN(Sales[Date]), MAX(Sales[Date]))
  ```
  After creating the table, you can add additional columns to this calendar table for year, month, and day:
  ```dax
  Year = YEAR(CalendarTable[Date])
  Month = FORMAT(CalendarTable[Date], "MMMM")
  Day = DAY(CalendarTable[Date])
  ```

---

## Technologies Used  
- **Power BI** for visualization and dashboard development.  
- **Excel/CSV** file as data sources.  

---

## Conclusion  
This Car Sales Dashboard will serve as a **powerful tool for sales monitoring and strategic planning**. By analyzing sales trends and KPIs through intuitive charts and grids, the company can quickly identify growth opportunities and areas needing attention.

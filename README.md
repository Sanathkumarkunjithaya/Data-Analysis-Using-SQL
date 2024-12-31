# **Supply Chain Analytics - SQL Project**

## **Project Overview**

This project focuses on **Supply Chain Analytics** to analyze and improve the accuracy of sales forecasts. By comparing actual sales data with forecasted quantities, this project aims to provide actionable insights into forecasting performance, helping businesses optimize their supply chain and inventory management.

The project involves using **SQL** to process a large dataset of sales and forecast data, calculate key metrics like **Net Error**, **Absolute Error**, and **Forecast Accuracy**, and generate reports that can inform decision-making.

## **Key Features**

### 1. **Data Integration and Analysis**
   - The project consolidates sales and forecast data to track discrepancies between actual sales and forecasted quantities.
   - Key metrics such as **Net Error** (the difference between forecasted and actual sales), **Absolute Error**, and **Forecast Accuracy** are calculated and used to assess forecasting performance.

### 2. **Triggers for Real-Time Data Updates**
   - **SQL Triggers** are used to automatically update a consolidated table whenever new data is inserted into the sales or forecast tables, ensuring the analysis is always up-to-date.

### 3. **Scheduled Data Maintenance**
   - **SQL Events** are employed to automatically delete outdated log data, helping to maintain database performance over time.

### 4. **Forecast Accuracy Report**
   - A detailed **Forecast Accuracy Report** is generated, showing how accurately sales forecasts match actual sales for each customer, helping businesses identify areas for improvement.

### 5. **Temporary Tables for Efficient Data Handling**
   - Temporary tables are used to store intermediate data results, improving the efficiency of complex queries and overall system performance.

## **Columns in the Dataset**

The dataset used in this project contains several key columns that are crucial for analyzing the performance of sales forecasts. Here’s a brief explanation of each:

1. **customer_code**:  
   - A unique identifier for each customer. This helps differentiate between customers in the dataset.
   - **Example**: `70003181`

2. **customer_name**:  
   - The name of the customer or retailer.
   - **Example**: `Atliq Executive`, `Flipkart`, `Amazon`

3. **market**:  
   - The geographic market where the customer operates. This helps categorize customers based on their location or region.
   - **Example**: `India`, `USA`, `Australia`

4. **total_sold_qty**:  
   - The total quantity of products sold to the customer within a specific period (e.g., monthly, yearly).
   - **Example**: `106946` units sold.

5. **total_forecast_qty**:  
   - The total quantity forecasted to be sold to the customer. This represents the predicted sales based on historical data or market trends.
   - **Example**: `70871` units forecasted.

6. **net_error**:  
   - The difference between the forecasted quantity (`total_forecast_qty`) and the actual sold quantity (`total_sold_qty`). A positive value indicates that the forecast was higher than actual sales, while a negative value suggests the opposite.
   - **Formula**: `net_error = total_forecast_qty - total_sold_qty`
   - **Example**: `-36075` (the forecasted sales were higher than the actual sales by 36,075 units).

7. **abs_error**:  
   - The absolute error is the absolute difference between the forecasted quantity and the actual sold quantity. It represents the magnitude of the error, regardless of whether the forecast was too high or too low.
   - **Formula**: `abs_error = abs(total_forecast_qty - total_sold_qty)`
   - **Example**: `72333` (the absolute difference between forecasted and actual sales is 72,333 units).

8. **abs_error_pct**:  
   - The percentage of absolute error relative to the forecasted quantity. It helps assess how significant the error is in the context of the forecast.
   - **Formula**: `abs_error_pct = (abs_error / total_forecast_qty) * 100`
   - **Example**: `102.06%` (the absolute error is 102.06% of the forecasted sales quantity).

9. **forecast_accuracy**:  
   - A metric that indicates the accuracy of the forecast. It is calculated as `100.0 - abs_error_pct`, meaning the lower the absolute error percentage, the higher the forecast accuracy.
   - **Formula**: `forecast_accuracy = 100.0 - abs_error_pct`
   - **Example**: `0%` (the forecast was highly inaccurate, with an absolute error percentage over 100%).

These columns help analyze the performance of sales forecasts, allowing businesses to identify discrepancies and optimize their forecasting processes.

## **How It Works**

This project processes a large dataset using SQL to compare forecast data with actual sales data. Here's how the system works:
1. **Sales and Forecast Data**: The dataset includes monthly records of actual sales and forecasted sales for various products and customers.
2. **Data Processing**: SQL queries are used to clean and analyze the data, calculating key metrics such as **Net Error** and **Absolute Error**.
3. **Automated Reporting**: The system generates real-time reports that show how accurate the forecasts are, based on the calculated metrics.
4. **Real-Time Updates**: **Triggers** automatically update the data whenever new sales or forecast records are inserted, ensuring that the analysis is up-to-date.
5. **Scheduled Cleanup**: **Events** are used to periodically delete outdated log records, keeping the database clean and optimized.

## **Use Cases**

This project can be applied in various scenarios:
- **Retail and E-commerce**: To evaluate how well sales forecasts match actual sales, helping businesses improve inventory management.
- **Supply Chain Management**: By identifying forecasting errors, companies can adjust their inventory levels to better meet customer demand.
- **Business Analytics**: It provides insights into the accuracy of forecasting models, which can be used to refine business strategies.

## **Technologies Used**

- **SQL** for data querying and analysis
- **MySQL/MariaDB** for database management
- **Triggers and Events** for automating tasks and ensuring real-time updates
- **Temporary Tables and Stored Procedures** for optimized performance and reusable queries

## **Outcome**

The project produces detailed reports on forecast accuracy, helping businesses identify trends, make better decisions, and improve forecasting processes. It offers valuable insights into sales performance and forecasting methods, making it a key tool for supply chain optimization.

## **Conclusion**

This project demonstrates the power of SQL in solving real-world supply chain challenges. By using advanced SQL features like triggers, events, and temporary tables, the project automates complex tasks and provides real-time insights, enabling businesses to make data-driven decisions that enhance their operations.


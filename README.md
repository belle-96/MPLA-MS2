# ==========================================
# FinMark Milestone 2 Sales Forecast Notebook
# ==========================================
"""
Purpose:
---------
This notebook generates a 6-month sales forecast for FinMark based on historical
customer transactions. Forecasts are produced for:
1. Overall sales
2. City-level sales
3. Price Segment (Standard/Premium)
4. City × Price Segment combination

Input Data:
-----------
- Cleaned_Customer_Transactions_BI.csv : Cleaned sales transactions with customer
  and product information. Must include columns:
  - Transaction_Date
  - Total_Cost
  - City
  - Price_Segment
- Optional: customers_data.csv, products_data.csv, transactions_data.csv

Processing Steps:
-----------------
1. Aggregate historical sales by month (YearMonth)
2. Create lag features (Lag_1, Lag_2) and 3-month rolling average
3. Train Random Forest models to capture trends
4. Forecast next 6 months sales
5. Visualize results (line plots, heatmaps)
6. Generate CSV output for THE 6MONTHS FORECAST

Outputs:
--------
- forecast_overall : Overall 6-month forecast
- forecast_city_product : City × Price Segment 6-month forecast
- Milestone2_6Month_Forecast.csv
- Visualizations:
  - Overall sales line chart
  - City-level forecast line chart
  - Price segment forecast line chart
  - City × Month heatmap

# Revenue and Shipping Cost Analysis Project

This project includes comprehensive analyses and forecasts for revenue projections, parcel shipping costs, and sales trends, leveraging various datasets and methodologies. 


## Table of Contents

1. [Q1 - Revenue Projection Analysis for 20X4](#question-1-revenue-projection-analysis-for-20x4)
2. [Q2 - Analysis of Increasing Parcel Shipping Costs](#question-2-analysis-of-increasing-parcel-shipping-costs)
3. [Q3 - Forecasting Daily Line Items and Quantity Sold for 2004 Based on Historical Order Data](#question-3-forecasting-daily-line-items-and-quantity-sold-for-2004-based-on-historical-order-data)

---

## Question 1: Revenue Projection Analysis for 20X4

Attached, please find an Excel worksheet `Q1.Rev_Projection` with a mock-up revenue history. Based on the data points offered, the goal is to project monthly revenue for 20X4 using three different forecasting methods, sharing formulas/code, and explaining methods to identify the most accurate projection.

### Methods Explanation
We employ three forecasting methods for revenue prediction:
1. **Exponential Smoothing (ETS)**  
   - *Description*: Models trends and seasonality using additive components.  
   - *Strengths*: Simple to implement; effective for clear seasonality.  
   - *Weaknesses*: Struggles with irregular patterns.

2. **Prophet Model**  
   - *Description*: Facebook's robust additive forecasting tool with built-in seasonality and holiday features.  
   - *Strengths*: Handles missing data, accommodates holidays.  
   - *Weaknesses*: May overfit if not tuned properly.

3. **SARIMA (Seasonal ARIMA)**  
   - *Description*: Combines autoregression, differencing, and moving average with seasonality components.  
   - *Strengths*: Flexible in capturing both seasonal and non-seasonal data.  
   - *Weaknesses*: Requires parameter tuning.

The analysis results and visualizations can be found in `main_file.ipynb`, with plots stored in the `plots/` folder.

---

## Question 2: Analysis of Increasing Parcel Shipping Costs

An Excel workbook with UPS shipment data for the same week in 2017 vs. 2018 (`Q2.2017` and `Q2.2018` tabs) highlights an increase in shipping costs as a percentage of revenue, despite a new UPS contract in 2018.  

### Objectives
1. Identify reasons for increased shipping costs relative to revenue using provided data and supplemental calculations (Excel formulas/code).  
2. Propose strategies for decreasing shipping costs based on analysis insights.

### Methodology
- Analyze shipment data from New Jersey and Ohio warehouses.
- Compare metrics like average cost per shipment, revenue-to-cost ratios, and parcel weight distributions.  
- Investigate operational inefficiencies or pricing discrepancies.

Key findings and proposed cost-reduction opportunities are documented in `main_file.ipynb`.

---

## Question 3: Forecasting Daily Line Items and Quantity Sold for 2004 Based on Historical Order Data

Attached is `Assessment Data2.csv`, which contains mock-up order history data. This analysis predicts daily line items and quantities sold for 2004 to optimize workload preparation at fulfillment centers.

### Objectives
1. Predict daily line items and total quantity sold using formulas/code.  
2. Identify trends and handle outliers in sales history.

### Assumptions
- A line item is defined as a unique combination of `Order ID` and `Product ID`.  
- Quantities include both box and individual sales.  
  - E.g., `order1_productA_qty3` and `order1_productA_qty1` combine to form 1 line item with 4 units sold.

### Methodology
- Forecasting: Used time-series techniques (e.g., ARIMA, Prophet) to predict daily metrics.
- Outlier Handling: Days with anomalous sales were flagged and treated to avoid skewing results.

Key trends, outlier treatments, and forecasting insights are documented in the Jupyter Notebook.

---

## Dependencies
To replicate the analyses, install the required Python libraries by running:
```bash
pip install -r requirements.txt


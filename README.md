# Supply Chain Analysis & Delivery Risk Prediction

## Project Overview
This project provides a comprehensive analysis of supply chain operations, focusing on delivery performance and risk assessment. By leveraging a historical dataset of orders, customers, and shipping details, the project identifies key bottlenecks and develops machine learning models to predict late deliveries.

## Business Problem
In a globalized supply chain, **late deliveries** are a major pain point that leads to:
*   Decline in customer satisfaction and brand loyalty.
*   Operational inefficiencies and increased overhead costs.
*   Financial losses due to canceled orders and penalties.

The primary goal of this analysis is to identify **where, why, and how** delays occur and to provide actionable insights for logistics optimization.

## Business KPIs (Key Performance Indicators)
Based on the comprehensive analysis of 172,765 total orders, the following KPIs were established:
*   **Total Orders**: 172,765
*   **Delayed Orders Percentage**: 54.71%
*   **On-Time Delivery Rate**: 45.29%
*   **Average Delay**: 1.647 days
*   **Total Profit**: $7.5M
*   **Total Loss**: -$3.7M
*   **90th Percentile Delay**: 3.0 days (90% of delays are within 3 days)
*   **Impact of Delays**: 55.43% of total losses are associated with delayed orders.

## Solution & Analysis

### 1. Delivery & Delay Analysis
We conducted an extensive EDA to understand the distribution of delays across various categories.
![Delay Analysis](Delay_analysis.png)
*Figure 1: Distribution of late deliveries across different shipping modes and departments.*

### 2. Time Series Trends
The analysis looked at how delivery performance fluctuated over time to identify seasonal patterns or systemic failures.
![Time Series Analysis](Time_series_Analysis.png)
*Figure 2: Delivery performance and shipping volume trends over time.*

### 3. Bottleneck Identification
Specific "hotspots" in the supply chain were identified. Regions like **Southeast Asia** and **South Asia** were found to have significantly higher late delivery rates compared to others.
![Bottleneck Analysis](bottleneck_analysis.png)
*Figure 3: Identification of regional and departmental bottlenecks.*

### 4. Root Cause Deep Dive
We investigated the underlying factors contributing to these delays, such as shipping mode efficiency and order status correlations.
![Root Cause Analysis](RootCauseAnalysis.png)
*Figure 4: Factors most strongly correlated with delivery failure.*

### 5. Predictive Modeling & Risk Evaluation
Multiple machine learning models (Logistic Regression, XGBoost, and **Random Forest**) were trained to predict the `Late_delivery_risk`.
*   **Model Accuracy**: ~74%
*   **Recall**: ~75% (Critical for capturing as many potential late orders as possible)

#### Risk Probability Distribution
The model generates a probability flag for each order, allowing logistics managers to prioritize high-risk shipments.
![Probability Flag Distribution](Probability_flag_dist.png)
![Probability Flag](Probability_flag.png)
*Figures 5 & 6: Distribution of risk probabilities and the effectiveness of the risk flagging system.*

## Suggestions to Improve Root Cause
1.  **Logistic Partner Review**: Audit and potentially renegotiate terms with regional logistics providers in high-delay zones (SE Asia/South Asia).
2.  **Predictive Flagging**: Integrate the Random Forest model into the dispatch system to flag "at-risk" orders for priority handling.
3.  **Customer Communication**: For regions with inherently higher risk, set more realistic "scheduled" shipping days to manage customer expectations.
4.  **Segment-Specific Logistics**: Develop specialized lanes for high-priority 'Corporate' and 'Home Office' segments to ensure business reliability.
5.  **Departmental Optimization**: Re-evaluate inventory management for the 'Fitness' department, which shows a higher propensity for delays.

---
*Created as part of the Analytics Course Work.*

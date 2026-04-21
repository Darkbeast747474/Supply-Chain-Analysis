# Supply Chain Analysis & Delivery Risk Prediction

## Project Overview
This project provides a comprehensive analysis of supply chain operations, focusing on delivery performance and risk assessment. By leveraging a historical dataset of orders, customers, and shipping details, the project identifies key bottlenecks and develops machine learning models to predict late deliveries.

## Business Problem
In a globalized supply chain, **late deliveries** are a major pain point that leads to:
*   Decline in customer satisfaction and brand loyalty.
*   Operational inefficiencies and increased overhead costs.
*   Financial losses due to canceled orders and penalties.

The primary goal of this analysis is to identify **where, why, and how** delays occur and to provide actionable insights for logistics optimization.

## Solution
The analysis follows a structured data science workflow:
1.  **Data Preprocessing**: Cleaned raw logistics data, handled missing values, and dropped redundant features (e.g., longitude, latitude, customer credentials).
2.  **Exploratory Data Analysis (EDA)**: 
    - Analyzed delay percentages across different **Order Regions**, **Customer Segments**, and **Shipping Modes**.
    - Identified that regions like **Southeast Asia** and **South Asia** are significant bottlenecks.
3.  **Predictive Modeling**: 
    - Built and evaluated multiple classification models (Logistic Regression, XGBoost, and Random Forest) to predict delivery risk.
    - **Random Forest** proved to be the most balanced model with an accuracy of **~74%** and a recall of **~75%**, ensuring high capture of late orders.
4.  **Operational Insights**: Correlated shipping status with profit margins to understand the financial impact of logistics failures.

## Key Findings & Bottlenecks
*   **Regional Delays**: Southeast Asia and South Asia show the highest percentage of delayed orders.
*   **Shipping Consistency**: Standard shipping often bears the brunt of delays, while certain categories like 'Fitness' show higher risk profiles.
*   **Model Success**: The machine learning models can effectively flag high-risk orders with ~74% accuracy, allowing for proactive intervention.

## Suggestions to Improve Root Cause
1.  **Logistic Partner Review**: Audit and potentially renegotiate terms with regional logistics providers in high-delay zones (SE Asia/South Asia).
2.  **Predictive Flagging**: Implement the Random Forest model into the dispatch system to flag "at-risk" orders for priority handling.
3.  **Customer Communication**: For regions with inherently higher risk, set more realistic "scheduled" shipping days to manage customer expectations.
4.  **Segment-Specific Logistics**: Develop specialized lanes for high-priority 'Corporate' and 'Home Office' segments to ensure business reliability.

---
*Created as part of the Analytics Course Work.*

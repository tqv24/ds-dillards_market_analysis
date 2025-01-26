# Department Sales Forecasting and Strategy

## Purpose
This project aims to forecast monthly sales for Dillards' product departments across cities in the United States. By leveraging predictive modeling and data-driven insights, the project assists with inventory management, pricing strategies, and understanding sales trends by department, location, and sales channel (online vs. in-store).

---

## Repository Contents
This repository includes the following files and directories:

- **`1_data_cleaning`**: R script for cleaning raw data, handling missing values, and merging datasets.
- **`2_exploratory_data_analysis`**: Script for analyzing trends, visualizing sales by month, state, and department, and ROI analysis.
- **`3_xgboost_model`**: Script for the prediction model of average store sale of each department with respect to city and month of Dillard's business
- **`dept_sale.pkl`**: Feature-engineered dataset used for predictive modeling, stored as a pickle file.
- **`project_update`**: Document tracking the progress and iterations of the project.
- **README**: This file, providing an overview of the project and instructions for reproducing the analysis.

---

## Project Overview
1. **Data Collection**:
   - Integrated data from multiple tables (e.g., store info, product info, transaction records).
   - Merged datasets while removing inactive SKUs and stores.

2. **Data Cleaning**:
   - Addressed missing values, corrected entry errors, and standardized data types.
   - Filtered out invalid transactions and unmatched SKU-store pairs.

3. **Feature Engineering**:
   - Aggregated metrics at the department, store, city, and state levels:
     - Average cost and price
     - Total sales amount
     - Number of products sold
   - Created new features such as seasonal trends for modeling.

4. **Modeling**:
   - **Baseline Model**: Linear Regression for basic insights into sales predictors.
     - R²: 0.6411, MAE: 8,498.41, RMSE: 12,065.56
   - **Enhanced Model**: XGBoost for advanced predictions.
     - Score: 0.958, WMAPE: 19.48%, MAE: 16.39, RMSE: 59.39
   - Applied square root transformation to address skewed sales distribution.
   - Hyperparameter tuning to optimize XGBoost performance.

5. **Recommendations**:
   - Optimize costs by negotiating supplier rates and reducing procurement expenses.
   - Plan inventory for seasonal peaks (e.g., summer and December) and low seasons.
   - Address underperforming months and departments with promotional strategies.

---

## How to Run the Project
1. **Set up the environment**:
   - Install required Python packages:
     ```bash
     pip install -r requirements.txt
     ```

2. **Execute the scripts**:
   - Run `1_data_cleaning` to preprocess and clean the data.
   - Run `2_exploratory_data_analysis` to explore trends and generate visualizations.
   - Run `3_xgboost_model` to predict average store sale for each department
   - Load the processed `dept_sale.pkl` file and train predictive models (e.g., XGBoost) in your notebook or script.
---
 


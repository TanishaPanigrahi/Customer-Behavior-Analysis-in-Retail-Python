#Exploratory Data Analysis & Customer Purchase Behavior Analysis in Retail

📌 Problem Statement

A retail company wants to understand customer purchase behavior and determine how demographic and product-related features influence spending patterns.

The objective is to build a predictive model that estimates purchase amount based on customer attributes.
Insights from this project will help the company:

🎯 Personalize offers

💰 Optimize marketing campaigns

🤝 Improve customer engagement

🎯 Objectives

🧹 Data Preprocessing: Handle missing values, duplicates, and categorical encoding.

📊 Exploratory Data Analysis (EDA): Identify patterns and relationships.

📈 Descriptive Analysis: Summarize data and visualize key metrics.

👥 Customer Segmentation: Identify behavioral clusters.

🤖 Predictive Modeling: Forecast purchase amount.

💡 Recommendations: Suggest actionable business insights.

🧾 Data Dictionary
Column	Description
User_ID	Unique identifier for each customer
Product_ID	Product code
Gender	M/F
Age	Customer age group
Occupation	Occupation code
City_Category	City type (A, B, or C)
Stay_In_Current_City_Years	Duration of stay
Marital_Status	0 = Unmarried, 1 = Married
Product_Category_1	Primary product category
Product_Category_2	Secondary product category
Product_Category_3	Tertiary product category
Purchase	Purchase amount
<details> <summary>⚙️ <b>Data Preparation Steps</b></summary>
🧩 1️⃣ Importing Libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

🧩 2️⃣ Data Loading & Merging

Loaded two CSVs — demographics and purchase details

Merged using User_ID

Saved combined dataset as BlackFridaySales.csv

🧩 3️⃣ Data Cleaning

Handled missing values (Product_Category_2, Product_Category_3)

Converted categorical columns (Age, Gender, City_Category)

Dropped duplicates

🧩 4️⃣ Feature Engineering

Created Total_Products_Bought

Applied Min-Max Scaling to Purchase

One-Hot Encoded categorical variables

</details>
<details> <summary>📊 <b>Exploratory Data Analysis (EDA)</b></summary>
🔹 Visualizations

Histogram for purchase distribution

Bar plots for gender & age distribution

Scatter: Purchase vs. Total Products Bought

Box plot for outlier detection

🔹 Key Insights
Factor	Observation
Gender	Males spend more than females
Age Group	26–35 years = highest spenders
City Category	City B dominates in purchases
Marital Status	Little difference in spend between married/unmarried
Stay Duration	Customers living 2+ years spend more
</details>
<details> <summary>📈 <b>Descriptive & Statistical Analysis</b></summary>
🧮 Summary Stats

Mean, Median, Std Dev, Percentiles of numerical features

Frequency count of categorical features

🧪 Hypothesis Tests
Test	Purpose	Result
T-Test	Compare Product_Category_1 vs. 2	No significant difference
ANOVA	Variance across categories	No significant difference
Chi-Square	Relationship between categories	Weak dependency
</details>
<details> <summary>💡 <b>Key Insights & Findings</b></summary>
Insight	Result
👥 Highest Spending Age Group	26–35 years
👨‍🦱 Highest Spending Gender	Male
🏙️ Highest Spending City	City B
💍 Higher Spending Marital Status	Married
📦 Top Product Categories	1, 5, 8, 11, 2
</details>
🧠 Next Step — Predictive Modeling

You can now use the preprocessed dataset for:

Regression models: Linear Regression, Random Forest, XGBoost

Evaluation Metrics: MAE, RMSE, R²

Goal: Predict purchase amount and optimize pricing strategies

💼 Business Recommendations

🎯 Target Age 26–35 group with personalized marketing.

🏙️ Focus campaigns on City Category B.

💸 Offer discounts on popular categories to boost repeat sales.

🕒 Reward customers with longer city stays to enhance loyalty.

🧰 Tech Stack
Tool	Purpose
🐍 Python 3.10+	Programming language
📊 Pandas, NumPy	Data manipulation
📈 Matplotlib, Seaborn	Visualization
⚙️ Scikit-learn	Feature scaling & encoding
🧪 SciPy / Statsmodels	Statistical analysis
💻 Jupyter Notebook / VS Code	Development environment

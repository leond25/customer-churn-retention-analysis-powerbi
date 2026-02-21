# Customer Churn & Retention Analysis (MySQL + Power BI)

## 📌 Project Overview
This project analyzes customer churn for a simulated subscription-based product to identify key drivers of churn and recommend retention strategies.  
An executive-facing dashboard was built in Power BI using data modeled in MySQL to quantify churn severity, isolate high-risk segments, and uncover behavioral patterns associated with churn.

## 🎯 Business Question
Why are customers churning, which segments are most at risk, and what actions can reduce churn?

## 🧱 Data Model
Relational schema designed in MySQL:

- customers (customer_id, signup_date, plan_type, country)  
- subscriptions (customer_id, status, churn_date)  
- usage_events (event_id, customer_id, event_date, feature_used)

A Date dimension was added in Power BI to enable time-based churn analysis.

## 📊 Dashboard Pages

### Page 1 – Executive Summary

- KPI Cards: Total Customers, Active Customers, Churned Customers, Churn Rate  
- Churn Over Time (by churn date)  
- Churn Rate by Plan Type  
- Interactive filters (Plan, Country, Month)

### Page 2 – Drivers of Churn

- Average Product Usage by Customer Status (Active vs Churned)  
- Feature Adoption Comparison (Login, Export, Report, API)  
- Churn by Tenure (Early vs Later churn)  
- Key drivers and recommendations for retention

## 🔍 Key Insights
- Churn is elevated, with **Basic plan customers at the highest risk**.  
- Churn is concentrated within the **first 1–3 months after signup**, highlighting onboarding risk.  
- Churned customers exhibit **lower engagement** and underutilize advanced features (Export, API) compared to retained users.  
- Login behavior alone does not differentiate retention; **adoption of value-driving features correlates with retention**.

## 💡 Recommendations
- Improve onboarding flows to guide new users to **Export and API features within the first week**.  
- Add in-product prompts and tutorials to accelerate **advanced feature adoption**.  
- Introduce activation milestones (e.g., “Export your first report”) to increase early value realization.  

## 🛠 Tools & Skills
- SQL (MySQL): data modeling, joins, aggregations  
- Power BI: dashboard design, interactive visuals  
- DAX: churn rate, time-based churn analysis using Date dimension and USERELATIONSHIP  
- Business Analysis: KPI design, segmentation, root-cause analysis, executive storytelling

## 📂 Files
- `/sql/schema.sql` – database schema  
- `/sql/sample_data.sql` – simulated dataset  
- `/dax/measures.md` – DAX measures used in Power BI  
- `/screenshots/` – dashboard screenshots  

## 🔁 How to Reproduce
1. Create the database using `/sql/schema.txt`  
2. Insert sample data using `/sql/sample_data.txt`  
3. Connect Power BI to MySQL  
4. Recreate visuals using measures in `/dax/measures.txt`

## 📝 Notes
This project uses simulated data to demonstrate an end-to-end business analytics workflow, from data modeling and KPI design to dashboarding and executive recommendations.

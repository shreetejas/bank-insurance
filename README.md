# Insurance Insights

### Dashboard Link : https://app.powerbi.com/groups/me/reports/9ed1a73e-e156-4eb3-ab51-9f9abeefb2af/f83a4fa47b97c6096180?experience=power-bi

## Problem Statement

Insurance companies handle large volumes of policy, customer, premium, and claim data. Without proper analytics, it becomes difficult to monitor claim trends, understand customer behavior, identify risk patterns, and evaluate the performance of different policy types.
This Power BI report was created to help the insurance provider overcome these challenges through interactive dashboards, KPIs, trend analysis, and customer sentiment insights.

This report helps the insurance team:

Identify how many claims are Settled, Pending, and Rejected.

Analyze premium and coverage amounts to understand revenue vs. risk.

Evaluate customer demographics such as age group, gender, activity status, and how they affect claims.

Understand customer concerns through feedback text analysis to find service gaps.

Detect high claim age groups and policy types generating heavy claim amounts.


Since rejected and pending claims together form a significant portion, the company must improve claim approval processes, documentation clarity, and communication.
Additionally, analysis shows that certain policy types have higher premium amounts but also higher claim amounts, indicating the need for improved risk management.

Steps Followed

- Step 1: Loaded the dataset into Power BI Desktop (CSV/Excel format)

- Step 2: Opened Power Query Editor and enabled:

Column Quality,
Column Distribution,
Column Profile.

- Step 3: Switched to “Column profiling based on entire dataset” for accurate data assessment.

- Step 4: Identified Null/Blank values:
Mostly found in Claim Date and some optional fields.
Required cleaning was applied.

- Step 5: Null values in key metrics like Premium Amount, Coverage Amount, Claim Amount were ignored while calculating averages and totals (as they represented missing or inapplicable data).

- Step 6: Applied a professional theme in the report view for standardized formatting.

- Step 7: Added Report Filters for:

Policy Number

Claim Number

Customer ID

Gender

Policy Type

Claim Status

- Step 8: Added KPI Cards for:

Total Premium Amount

Total Coverage Amount

Total Claim Amount

- Step 9: Created bar charts and donut charts for:

Premium Amount by Policy Type

Claim Status distribution

Claim Amount by Age Group

Gender-wise Active/Inactive policies

- Step 10: Created a detailed table visual to display:

Policy Number, CustomerID, Claim Number, Age, Gender, Coverage Amount, Premium Amount, Policy Dates, Policy Type, Claim Status, Claim Date.

- Step 11: Added a Customer Feedback Table and performed text analysis manually through summarization.

- Step 12: Inserted branding elements:
Company name, Tagline, Logo. Shapes for design consistency

- Step 13: Created a calculated column for Age Grouping using DAX:

= Table.AddColumn(#"Sorted Rows1", "Age Group", each 

if [Age] <= 24 then "Young Adult" 

else if [Age] >= 60 then "Adult" else "Elder")


- Step 14: Published the report to Power BI Service.
Insights

fully interactive Insurance Analytics Dashboard was created. Key business insights include:

[1] Premium, Coverage & Claims Overview

Total Premium Amount: ₹5.98M

Total Coverage Amount: ₹600M

Total Claim Amount: ₹16.9M

These KPIs help understand total revenue vs. risk exposure.

[2] Claim Status Distribution

Pending: 2.3K

Settled: 3.4K

Rejected: 4.4K

Rejected claims are the highest, indicating possible:

documentation issues

claim fraud

customer dissatisfaction

internal approval inefficiencies

[3] Policy Type Insights
Premium Amount by Policy Type

Travel: Highest premium contributor

Health & Auto: Moderate revenue

Home & Life: Lowest premium generation

This helps identify top-performing policy segments.

[4] Claim Amount by Age Group

Elder: 8.5M (Highest risk)

Young Adult: 6.7M

Adult: 1.7M

Older customers generate a significantly higher claim amount — crucial for pricing, risk scoring, and premium adjustments.

[5] Gender-wise Policy Status

Male Active Policies: 5.82K

Female Active Policies: 4.19K

This helps understand customer base composition.

[6] Customer Feedback Insights

Common issues from customer feedback table:

Website/login issues

Billing disputes

Premium increase complaints

Claim process delays

Confusing policy terms

Lack of transparency

Good staff behaviour & quick resolutions reported by some

Feedback helps refine digital services & claims workflow.

Conclusion

This dashboard provides a comprehensive overview of the insurance company’s operational and customer metrics.
It helps decision-makers understand:

which policy types generate more revenue

which age groups create higher claims

claim settlement efficiency

customer satisfaction issues

demographic insights

# snapshot
<img width="956" height="538" alt="Screenshot 2025-12-09 213542" src="https://github.com/user-attachments/assets/4bc1ec7b-3394-4244-ac41-15bc65bd37f4" />
<img width="954" height="537" alt="Screenshot 2025-12-09 213608" src="https://github.com/user-attachments/assets/ff66e129-9669-4f55-92a2-127775bccb35" />
<img width="934" height="532" alt="Screenshot 2025-12-09 213701" src="https://github.com/user-attachments/assets/14430ce2-a517-49da-a02a-2b8cd0810543" />

# Conclusion

reducing claim rejection rates

improving customer support

resolving billing/website issues

strengthening fraud detection for high-risk age groups

Overall, this dashboard supports better decision-making, risk management, and customer experience improvement.

🧾 Customer Segmentation using RFM Analysis & K-Means Clustering
📘 Project Overview

This project applies RFM (Recency, Frequency, Monetary) analysis and K-Means clustering to an e-commerce dataset to identify distinct customer segments. The goal is to support targeted marketing strategies and customer relationship management through data-driven insights.

🎯 Objective

To segment customers based on purchasing behavior using RFM metrics and clustering techniques, helping businesses tailor marketing efforts for each group effectively.

📊 Dataset Summary

Source: Online Retail dataset (e-commerce transactions)

File Used: online_retail.csv

Main Features:

InvoiceNo – Unique transaction number

StockCode – Product ID

Description – Product name

Quantity – Units purchased

InvoiceDate – Date of transaction

UnitPrice – Price per item

CustomerID – Unique customer identifier

Country – Customer’s country

🧹 Data Cleaning Steps

Handled Encoding: Fixed UnicodeDecodeError using encoding='ISO-8859-1'

Removed Null Values: Especially from CustomerID and Description

Filtered Cancellations: Excluded invoices starting with “C”

Created TotalAmount: Quantity * UnitPrice

Converted Dates: InvoiceDate → datetime format

Removed Duplicates and Outliers

📈 Methodology
🔹 RFM Definition

Recency (R): Days since last purchase

Frequency (F): Number of purchases

Monetary (M): Total amount spent

Each metric was calculated per CustomerID and normalized for clustering.

🔹 Clustering

Used Elbow Method to determine optimal k

Applied K-Means Clustering

Validated cluster quality using Silhouette Score

🧩 Results
🔸 Elbow Plot

Indicated k = 4 as the optimal number of clusters.

🔸 Silhouette Score

Average silhouette score ≈ 0.61, showing clear cluster separation.

🔸 Cluster Summary Table
Cluster	Avg Recency	Avg Frequency	Avg Monetary	Interpretation
0	Low	High	High	Loyal / VIP Customers
1	Medium	Medium	Medium	Regular Buyers
2	High	Low	Low	Lost / Inactive Customers
3	Low	Low	Medium	New or Occasional Buyers
🔸 Customer Personas

Cluster 0: VIPs — Frequent, high spenders, very recent activity

Cluster 1: Engaged Regulars — Moderate engagement and value

Cluster 2: Lost Customers — Need reactivation strategies

Cluster 3: New Buyers — Potential for conversion to loyal customers


💡 Recommendations
Persona	Suggested Marketing Strategy
VIPs	Offer loyalty rewards, exclusive previews
Regulars	Send personalized discounts or bundles
Lost Customers	Reactivation emails, limited-time offers
New Buyers	Welcome campaigns, onboarding discounts
⚖️ Limitations & Ethical Considerations

Missing or inaccurate customer data may affect segmentation quality.

Dataset anonymized — no personally identifiable information used.

RFM assumes equal weight across metrics; future models could apply advanced weighting or behavioral features.

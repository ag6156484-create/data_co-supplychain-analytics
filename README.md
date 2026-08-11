# Supplychain Analytics & Logistics Performance Dashboard
End-to-End Supply Chain Analytics Using Python(EDA) and interactive Tableau Dashboards to analyse sales ,logistics efficiency,and fraud risk
 🚚 DataCo Supply Chain & Logistics Analytics

<p align="center"
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Total_Sales-%2436.78M-008080?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Profit_Margin-12.00%25-10B981?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Late_Delivery-54.83%25-D97706?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Fraud_Loss-%24825.93K-DC2626?style=for-the-badge"/>
</p>

Executive Summary
 This repository contains end to end data processing, data hygiene checks, Exploratory data analysis (EDA) conducted on the DataCoSupply Chain dataset using Python (pandas, NumPy, matplotlib, and seaborn) with Tableau for executive level interactive dashboarding. The primary goal is to evaluate financial health, identify operational supply chain bottlenecks, assess delivery fulfillment delays, and mitigate global fraud risk exposure.

📊 KPI's & Calculated Fields
 
 1.Total Fraud loss: if [Fraud Loss] = 1 then [Sales] else 0 end
 
 2.ON Time Delivery Rate: COUNTD (if [Delivery Status] ='Advance shipping' OR [Delivery Status] ='Shipping on time' then [Order Id] END)/ COUNTD ([Order Id])
 
 3.Profit Margin = sum ([Order Profit Per Order])/ SUM ([Sales per customer])
 
 4.Late Delivery rate = sum ([Late Delivery Flag])/ COUNT ([Order Id])
 
 5.Fraud Loss = if [Order Status] ="SUSPECTED_FRAUD" then 1 else 0 END
 
🎯Business Questions

1.Which geographical regions generates the highest sales volume versus those yielding higher net profit margins?

2.Which Product Categories yield the highest sales per customer and how does product volume correlate with profitability?

3.How does Late delivery rate fluctuate month over month alongside fraud loss across specific customer segments?

4. What is the total monetary loss attributed to payment fraud and which global market contributes to most fraud loss?

5.Which shipping mode exhibits the highest late delivery rate across different geographical regions?

6.How significance is the variance between scheduled shipping days and actual transit days across different fulfillment channels?

7.How does fraud loss distribute across different shipping modes when broken down by customer segments?

 
 📁 Project Structure

```text
dataco-supplychain-analytics/
├── notebooks/
│   └── dataco_supply_chain_analysis.ipynb   # Python EDA & Notebook Analysis
├── dashboards/
│   ├── supply_chain_overview.twbx           # Tableau Interactive Workbook
│   ├── dashboard1.png                        # Executive Overview Screenshot
│   ├── dashboard2.png                        # Risk & Fraud Analytics Screenshot
│   └── dashboard3.png                        # Logistics Efficiency Screenshot
└ ── README.md
```


 🔗 Project Links


* Jupyter Notebook (EDA & Modeling): (https://colab.research.google.com/drive/1l7t-f3j1nLmvZ5P4uGey6zN4iK8ENRon?usp=sharing)
* Original Dataset (Kaggle): (https://www.kaggle.co)
* Tableau Dashboard link: https://github.com/ag6156484-create/data_co-supplychain-analytics/blob/main/dashboards/supply%20chain%20and%20Logistic%20Management%20Tableau%20project.twbx



 🔑 Key Findings

| Metric | Value |
| :--- | :--- |
| *Total Shipment Analysed* | 180,519 |
| *Total Sales Volume* | $36.78M |
| *Overall Late Delivery Rate* | 54.83% |
| *Total Fraud Loss* | $825.93K |
| *Average Profit Margin* | 12.00% |
| *Highest Sales Region* | Europe ($10.87M / 29.56%) |
| *Worst Fulfillment Mode* | Standard Class |
| *Highest Fraud Exposure Region* | United States ($112.47K) |
| *On Time Delivery Rate* | 40.83% |



📊 Findings of EDA

1. Created summary statistics showing the mean days for real shipping is around 3 days with only 1 standard deviation.
2. Applied data cleaning steps to check for missing values, duplicate values, and outliers in sales distribution.
3. Actual shipping duration follows a normal distribution centered around 3 days (ranging between 0 and 6 days).
4. High-value order volumes are primarily driven through electronic payment modes (DEBIT and TRANSFER).
5. A significant proportion of orders fall under the LATE_DELIVERY category, highlighting fulfillment bottlenecks within specific shipping routes.
6. Order volume tracking shows high concentration in COMPLETE and PENDING_PAYMENT states.
7. *EUROPE* leads overall sales generation at *29.56%, followed by **LATAM (27.94%)* and *PACIFIC_ASIA (22.49%)*.
8. Most business revenue (~half of revenue) comes from the *Consumer* segment, while Corporate is the second largest segment.
9. Sales per customer, total sales, and order item total show a strong positive correlation with each other.
10. High discounts negatively impact profitability, driving transactions into negative profit margins.



 📈 Dashboard Report and Insights

 1. Executive Overview & Sales Performance Dashboard
* *High-Margin Drivers:* Product categories like *Fishing, **Cleats, and **Camping & Hiking* drive high-margin contributions.
* *Profit Yield:* Moderate-volume categories maintain healthy profit spans, while heavy discounts sporadically reduce yield.

 2. Supply Chain Risk & Fraud Analytics Dashboard
* *Fraud Exposure:* The *United States* accounts for the highest financial loss exposure from fraudulent activities (*$112.47K), alongside **Indonesia* and *Canada*.
* *Regional Losses:* *France ($58.21K)* and *Mexico ($46.12K)* show notable fraud concentration requiring payment gateway validation.
* *Late Delivery Risk:* Several categories face high late delivery rates despite strong profit margins, posing a potential risk to customer retention.

 3. Logistics & Fulfillment Efficiency Dashboard
* *Standard Class:* Accounts for the highest total volume of late shipments (~59k orders), functioning as the primary supply chain bottleneck.
* *Second Class:* Records moderate delay volume (~19k orders).
* *First Class & Same Day:* Exhibit higher SLA compliance rates but require routing optimization during peak seasons.
* *Order Status vs. Shipping Mode:* Evaluates delay proportions across carriers to isolate carrier-specific operational deficiencies versus warehouse dispatch delays.
* *Geographic Corridor SLA Analysis:* Tracks origin-to-destination transit delays to pinpoint regional transit hubs needing warehouse re-allocation.



 💡 Executive Strategic Recommendations

* *Inventory Prioritization:* Focus fulfillment resources on top-margin categories to protect core revenue streams from delivery delays.
* *Discount Threshold Control:* Cap promotional discounts strictly under $50, as higher discounts (>$100) trigger severe negative profit margins.
* *Carrier SLA & Standard Class Restructuring:* Address logistics operational bottlenecks since fulfillment delays show no correlation (~0.00) with item prices.
* *Inventory & Warehouse Regional Prioritization:* Allocate supply chain inventory and storage capacity closer to core revenue drivers in Europe and LATAM (>57% of total global sales).
* *Targeted Fraud Prevention Protocol:* Implement automated high-value verification checks for US-bound shipments to safeguard against $825K+ in fraud exposure.









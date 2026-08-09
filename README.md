# supplychain Analytics & Logistics Performance Dashboard
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
├── requirements.txt                          # Python Environment Dependencies
└── README.md

🔗 Project Links

 📊 *Tableau Public Interactive Dashboard:* [View Live Dashboards]() (Aapka Tableau Public Link)
 📓 *Jupyter Notebook (EDA & Modeling):* [View Python Notebook](notebooks/dataco_supply_chain_analysis.ipynb)
 💾 *Original Dataset (Kaggle):* [DataCo Supply Chain Dataset](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data)
 💼 *Developer Profile:* [LinkedIn Profile](https://linkedin.com/in/)

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

1.Executive Overview & Sales Performance Dashboard
Key Metrics Monitored:
Total Sales Volume: $36.78M across global operations.
Total Order Volume: 65,752 orders processed.
Distinct Customer Base: 20,652 unique customers.
Overall Profit Margin: Sustained at 12.00%.
Core Visual Components & Analytics:
Revenue Trends by Customer Segment:
Consumer Segment generates the primary market revenue (51.93% / $19.10M).
Corporate Segment accounts for 30.35% ($11.16M).
Home Office Segment contributes 17.72% ($6.52M).
Geographic Sales Distribution:
Europe represents the top-performing market with $10.87M (29.56% share).
LATAM (Latin America) follows closely at $10.28M (27.94% share).
North America and Pacific Asia drive remaining high-value order volumes.
Category Profitability Breakdown:
Fishing, Cleats, and Camping & Hiking drive high-margin contributions.
Moderate-volume categories maintain healthy profit spans, while heavy discounts sporadically reduce yield.

2. Supply Chain Risk & Fraud Analytics Dashboard
Key Metrics Monitored:
Total Financial Exposure (Suspected Fraud): $825.93K.
Fraud Order Count: 3,212 high-risk orders identified.
Overall Late Delivery Rate: 54.83% across all operational fulfillment channels.
Core Visual Components & Analytics:
Regional Fraud Exposure Matrix:
United States accounts for the highest financial loss exposure from fraudulent activities ($112.47K).
France ($58.21K) and Mexico ($46.12K) show notable fraud concentration requiring payment gateway validation.
Order Status & Fulfillment Risk Categorization:
Late Delivery: Represents 54.83% of all shipped orders (~98,900 shipments).
Advance Shipping / On Time: Accounts for 41.6% combined.
Canceled / Delivery Blocked: Represents ~3.57% of total order processing.
Financial Impact of Delivery Delays:
Identifies correlated profit losses from fulfillment penalties and chargebacks across delayed regional orders.

3.logistics & Fulfillment Efficiency Dashboard
Key Metrics Monitored:
Average Delivery Days: Real-time shipping duration averages 3.0 days against scheduled timelines.
SLA Non-Compliance Volume: Over 98k shipments breached original delivery estimates.
Core Visual Components & Analytics:
Shipping Mode Performance & Delay Breakdown:
Standard Class: Accounts for the highest total volume of late shipments (~59k orders), functioning as the primary supply chain bottleneck.
Second Class: Records moderate delay volume (~19k orders).
First Class & Same Day: Exhibit higher SLA compliance rates but require routing optimization during peak seasons.
Order Status vs. Shipping Mode Cross-Analysis:
Evaluates delay proportions across carriers to isolate carrier-specific operational deficiencies versus warehouse dispatch delays.
Geographic Corridor SLA Analysis:
Tracks origin-to-destination transit delays to pinpoint regional transit hubs needing warehouse re-allocation.

💡 Executive Strategic Recommendations
Discount Threshold Control:
Cap promotional discounts strictly under $50, as higher discounts (> \$100) trigger severe negative profit margins (losses up to -$4,000 per transaction).
Carrier SLA & Standard Class Restructuring:
Since fulfillment delays show no correlation (r \approx 0.00) with item prices, bottlenecks stem strictly from logistics operations. Conduct an urgent SLA review for Standard Class carriers.
Inventory & Warehouse Regional Prioritization:
Allocate supply chain inventory and storage capacity closer to core revenue drivers in Europe and LATAM (>57% of total global sales).
Targeted Fraud Prevention Protocol:
Implement automated high-value verification checks for US-bound shipments to safeguard against $825K+ in fraud exposure.





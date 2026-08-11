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

Executive Summary
 This repository contains end to end data processing, data hygiene checks, Exploratory data analysis (EDA) conducted on the DataCoSupply Chain dataset using Python (pandas, NumPy, matplotlib, and seaborn) with Tableau for executive level interactive dashboarding. The primary goal is to evaluate financial health, identify operational supply chain bottlenecks, assess delivery fulfillment delays, and mitigate global fraud risk exposure.

 KPI's & Calculated Fields:
 
  1.Total Fraud loss: if [Fraud Loss] = 1 then [Sales] else 0 end
 2.ON Time Delivery Rate: COUNTD (if [Delivery Status] ='Advance shipping' OR [Delivery Status] ='Shipping on time' then [Order Id] END)/ COUNTD ([Order Id])
 3.Profit Margin = sum ([Order Profit Per Order])/ SUM ([Sales per customer])
 4.Late Delivery rate = sum ([Late Delivery Flag])/ COUNT ([Order Id])
 5.Fraud Loss = if [Order Status] ="SUSPECTED_FRAUD" then 1 else 0 END
 
Business Questions
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


## 🔗 Project Links

 📊 *Tableau Public Interactive Dashboard:* [View Live Dashboards](dashboards/supply chain and Logistic Management Tableau project.twbx) (Aapka Tableau Public Link)
 📓 *Jupyter Notebook (EDA & Modeling):* [View Python Notebook](https://colab.research.google.com/drive/1l7t-f3j1nLmvZ5P4uGey6zN4iK8ENRon?usp=sharing)
 💾 *Original Dataset (Kaggle):* [DataCo Supply Chain Dataset](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data)
 💼 *Developer Profile:* [LinkedIn Profile](https://linkedin.com/in/)


## 🔑 Key Findings
| Metric | Value |
| :--- | :--- |
| Total Shipment Analysed* | 180,519 |
| Total Sales Volume* | $36.78M |
| Overall Late Delivery Rate* | 54.83% |
| Total Fraud Loss* | $825.93K |
| Average Profit Margin* | 12.00% |
| Highest Sales Region* | Europe ($10.87M / 29.56%) |
| Worst Fulfillment Mode* | Standard Class |
| Highest Fraud Exposure Region* | United States ($112.47K) |
| On Time Delivery Rate* | 40.83% |


## Findings of EDA:
1. Created a summary statistics showing the Mean days for real shipping is around 3 days with only one standard deviation and max days goes to 6 days sometime which we should reduce by identifying regions and delay reason . Avg Sales per customer is around 180 while it has very high deviation of 100 while some sales goes up to 1900 shows high value customers. while looking at avg discount it is 20 but the highest value is 500 which could be problematic for our profit . profit per order shows high fluctuations with range of 100 - 900 which means some orders are giving very high profit while some orders are giving us medium profit.
2. Apply data cleaning step to check any missing values, to handle duplicate values and to check for outliers in the sales distribution by creating a histogram. Majority transactions concentrated in the range of 0 to 250. but some multiple outliers are present at 300+ which represents premium customer segment of our supply chain.
3. Actual shipping duration follows a normal distribution centered around 3 days (ranging between 0 and 6 days)
4. In payment preferences column, High value order volumes are primarily driven through electronic payment modes (DEBIT and TRASFER)
5. A significant proportion of orders fall under the LATE_DELIVERY category, highlighting fulfilment
bottleneck within specific shipping routes and transit schedules.
6. order volume tracking shows high concentration in COMPLETE and PENDING_PAYMENT states.
7.EUROPE leads overall sales generation at 29.56%, followed by LATAM (27.94%) and PACIFIC_ASIA (22.49%)
8.Most of our business revenue around half of revenue comes from consumer segment while corporate is our second largest segment with smaller contribution from Homeoffice segment.
9. Our growing markets are Europe and LATAM in terms of product demand while PACIFIC_ASIA is third largest growing market.
10. sales per customer, sales, order item total shows nearly perfect positive correlation with each other indicates that overall revenue drives from order items. Days for shipping real shows medium relationship with days for shipping scheduled means there is possibility of delivery delay. sales per customer and order item discount relationship shows that with increase in discount sales got affected.
11. As discount shows negative impact in profit in this data most of high discount transactions falls in the negative profit region which means giving discount reduce company profit so we should adapt new factor to increase sales.


## Dashboard Report and Insights:
1.Executive Overview & Sales Performance Dashboard:
# Category like Fishing, Cleats, and Camping & Hiking drive high-margin contributions.
Moderate-volume categories maintain healthy profit spans, while heavy discounts sporadically reduce yield.
# 
2. Supply Chain Risk & Fraud Analytics Dashboard
United States accounts for the highest financial loss exposure from fraudulent activities ($112.47K) and Indonesia and Canada also suffering significant losses.
France ($58.21K) and Mexico ($46.12K) show notable fraud concentration requiring payment gateway validation.
Several categories face high late delivery rates despite strong profit margins, posing a potential risk to customer retention and brand equity.

3.logistics & Fulfillment Efficiency Dashboard
Shipping Mode Performance & Delay Breakdown:
Standard Class: Accounts for the highest total volume of late shipments (~59k orders), functioning as the primary supply chain bottleneck.
Second Class: Records moderate delay volume (~19k orders).
First Class & Same Day: Exhibit higher SLA compliance rates but require routing optimization during peak seasons.
Order Status vs. Shipping Mode Cross-Analysis:
Evaluates delay proportions across carriers to isolate carrier-specific operational deficiencies versus warehouse dispatch delays.
Geographic Corridor SLA Analysis:
Tracks origin-to-destination transit delays to pinpoint regional transit hubs needing warehouse re-allocation.

## 💡 Executive Strategic Recommendations:

Inventory prioritization:
focus fulfillment resources on top margin category to protect core revenue streams from delivery delays.
Discount Threshold Control:
Cap promotional discounts strictly under $50, as higher discounts (> \$100) trigger severe negative profit margins (losses up to -$4,000 per transaction).
Carrier SLA & Standard Class Restructuring:
Since fulfillment delays show no correlation (r \approx 0.00) with item prices, bottlenecks stem strictly from logistics operations. Conduct an urgent SLA review for Standard Class carriers.
Inventory & Warehouse Regional Prioritization:
Allocate supply chain inventory and storage capacity closer to core revenue drivers in Europe and LATAM (>57% of total global sales).
Targeted Fraud Prevention Protocol:
Implement automated high-value verification checks for US-bound shipments to safeguard against $825K+ in fraud exposure.





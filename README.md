
# 🕵️‍♂️ Fraud Detection in Banking Transactions Using Excel

A hands-on Excel-based mini-project that simulates rule-based fraud detection in financial transaction data. Ideal for learning data cleaning, formula logic, lookup functions, pivot tables, KPIs, and dashboards—all inside Excel.

## 📌 Project Objectives

1. Identify Suspicious Transactions Using Rule-Based Logic
   - Apply logical rules (e.g., high amount, cross-country, new device, odd hours) to flag potential fraud.
   - Use Excel formulas such as `IF()`, `TEXT()`, `HOUR()`, and `VLOOKUP()` to build fraud rules.

2. Leverage Lookup Functions to Enrich Transaction Data
   - Use `VLOOKUP()` and `XLOOKUP()` to merge customer-level information (country, device, average amount) into transaction data.

3. Design a Fraud Risk Scoring System
   - Assign scores based on the number of fraud rules triggered by each transaction.
   - Categorize transactions into `Low`, `Medium`, and `High` risk.

4. Create an Interactive Dashboard to Monitor Transactions
   - Use PivotTables, PivotCharts, and Conditional Formatting to summarize and visualize trends.
   - Track metrics like total flagged transactions, most common fraud rule, and country-wise fraud distribution.

5. Enable Stakeholders to Drill Down into Data
   - Add drop-down filters with Data Validation to slice and dice data by customer, transaction type, country, or date.

6. Showcase Advanced Excel Skills for Real-World Use Cases
   - Demonstrates Excel’s power in financial risk monitoring with dashboards and formula-driven analytics.

## 🧠 Rule-Based Flags

| Rule Name       | Description                                                | Formula Example                                      |
|------------------|------------------------------------------------------------|-------------------------------------------------------|
| High_Value      | Amount > 2 × Avg Amount (customer-wise)                   | `=IF(D2>2*L2,1,0)`                                    |
| Cross_Country   | Transaction country ≠ Registered country                   | `=IF(E2<>J2,1,0)`                                     |
| New_Device      | Current Device ≠ Registered Device                        | `=IF(F2<>K2,1,0)`                                     |
| Odd_Hour        | Hour of transaction is before 4 AM or after 11 PM         | `=IF(OR(HOUR(C2)<4, HOUR(C2)>23),1,0)`                 |

## 📊 Pivot Tables

PivotTables answered:
- How many flagged transactions are there by rule?
- Which customers have the most suspicious transactions?
- Which countries show higher fraud activity?

## 📈 Dashboard

The interactive dashboard includes:
- KPI cards for:
  - Total transactions
  - Flagged transactions
  - High-risk %
  - Most triggered rule
- Pie chart: Flagged by country
- Bar chart: Flagged by rule
- Horizontal Barchart: Suspicious transactions per device registered
- Table: Drill-down of top flagged customers

## 🛠 Excel Features Used

- `IF`, `VLOOKUP`, `XLOOKUP`, `TEXT`, `HOUR`
- Conditional Formatting
- PivotTables & PivotCharts
- Data Validation (for filters)
- INDEX-MATCH (for KPI like Top Rule)

## ✅ Example KPI Formula

Top Rule Triggered
```excel
=INDEX(Fraud_Summary!D10:D15, MATCH(MAX(Fraud_Summary!E10:E15), Fraud_Summary!E10:E15, 0))

```
🔍 Key Findings:

1. The majority of suspicious activities were attributed to unusually high transaction amounts compared to the customer's averages.
2. Many transactions were made from countries different from the customer's registered country, raising red flags.
3. A significant number of transactions occurred from devices that were not previously linked to the customer.
4. Several transactions were made during odd hours (between 12 AM and 4 AM), which are less typical and possibly fraudulent.
5. A few customers appeared multiple times in the flagged transactions list, indicating potential repeated fraud behavior.
6. Specific countries or locations had a disproportionately high number of suspicious transactions.
7. Among all rules, High_Value transactions were the most frequent fraud indicators.

## 📁 Files Included

- `Fraud_Detection.xlsx`: Sample transaction and customer data
- `Dashboard`: Dashboard with KPIs & visuals
- `README.md`: Project guide

---

👨‍💻 Author

Meer Tozammel Hossain
Department of Statistics  
University of Dhaka  
Project Type: SQL Portfolio
Status: Completed  


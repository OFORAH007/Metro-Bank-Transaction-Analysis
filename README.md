# 🏦 Metro Bank - Transaction Overview
![jon-tyson-RfJ0sNDIOno-unsplash](https://github.com/user-attachments/assets/7d57adc8-d01e-41d2-aa71-87cd8fc49f0d)

##  Project Overview
This project analyzes the **transaction history of Metro Bank** to provide a comprehensive overview of customer behavior and key performance indicators. The dashboard delivers insights into **transaction volume, account types, customer activity, and channel preferences**.  

The goal is to help **Metro Bank’s management make data-driven decisions** to improve customer engagement and optimize banking services.  

The dashboard is **interactive**, allowing users to filter data by demographic segments such as:
- Baby Boomers  
- Gen X  
- Millennials  
- Gen Z  

---

##  Data Source and Description
- **Primary Source:** Transaction history of Metro Bank.  
- **Data Includes:**  
  - Transaction types: deposits, payments, transfers, and withdrawals  
  - Transaction channels: ATM, Branch, Online, POS  
  - Customer account details  
  - Customer demographics (e.g., generation)  

This dataset is essential for understanding **how customers interact with banking services and channels**.  

---

![james-orr-E99lndzGTYQ-unsplash](https://github.com/user-attachments/assets/5604b41b-5182-44db-a5be-77e9797e1816)

##  Objective
The main objective is to **create an interactive dashboard** that visualizes Metro Bank’s transaction data to uncover trends, patterns, and insights.  

### Specific Goals
1. Analyze transaction volume and value over time.  
2. Understand customer behavior by transaction type and channel.  
3. Identify the most active merchants and their transaction counts.  
4. Segment insights by customer demographics (generations).  
5. Provide actionable recommendations to improve services and engagement.  

---

![louis-hansel-Rf9eElW3Qxo-unsplash](https://github.com/user-attachments/assets/b6336352-5a10-4b9a-9a43-97616e655a73)

## Tools Used
- **Azure Data Studio** → Database management and querying raw transaction data.  
- **Microsoft Excel** → Data cleaning, transformation, and analysis using:  
  - **Power Query** → For ETL (extract, transform, load).  
  - **DAX (Data Analysis Expressions)** → For custom measures and calculated columns.
  -  
```
Important SQL Queries worth documenting include;
1️⃣ Aggregate total transaction value and count by transaction type
SELECT 
    TransactionType,
    COUNT(TransactionID) AS TotalTransactions,
    SUM(TransactionValue) AS TotalValue,
    AVG(TransactionValue) AS AvgTransactionValue
FROM Transactions
GROUP BY TransactionType
ORDER BY TotalValue DESC;

```
``` 2️⃣ Analyze channel preference segmented by customer generation
SELECT 
    c.Generation,
    t.Channel,
    COUNT(t.TransactionID) AS TotalTransactions,
    SUM(t.TransactionValue) AS TotalValue
FROM Customers c
JOIN Transactions t 
    ON c.CustomerID = t.CustomerID
GROUP BY c.Generation, t.Channel
ORDER BY c.Generation, TotalTransactions DESC;

```

##  Data Preparation and Cleaning
Steps taken to ensure accuracy and reliability:

1. **Data Loading** → Imported raw transaction data into Excel.  
2. **Data Type Conversion** → Ensured numeric and date fields had correct formats.  
3. **Handling Missing Values** → Removed or imputed missing/null entries.  
4. **New Columns Creation** → Added fields such as “Transaction Month” and “Day of Week.”  
5. **Data Aggregation** → Calculated total transaction volume and average transaction values.  

---


##  Key Findings and Market Insights
- **Transaction Volume:**  
  - Total: **N25.1M**  
  - Transactions: **5,000**  
  - Average Transaction Value: **N5.0K**  

- **Transaction Type:**  
  - Strong positive correlation (**0.95**) between **payments** and transaction value.  
  - Transfers show lower correlation, reflecting frequent but lower-value transactions.  

- **Customer Channel Preference:**  
  - Correlation between account balance and channel choice = **-0.11** → almost no relationship.  

- **Channel Popularity:**  
  - **POS** is most popular for payments.  
  - **Branches** dominate for high-value transactions.  

- **Top Merchants:**  
  Airbnb, LocalStore, Apple, and Uber rank highest by transaction count.  

<img width="1836" height="851" alt="Metro_Bank03" src="https://github.com/user-attachments/assets/0a6537ed-f5b9-4134-9383-91e60944b6d0" />


---

##  Recommendations
1. **Targeted Campaigns**  
   - Promote channel-specific campaigns without segmenting by balance.  
   - Example: Incentives for **Online/Mobile app usage**.  

2. **Optimize Branch Services**  
   - Enhance branch experience for **large transactions** with personalized service.  

3. **Partner with Top Merchants**  
   - Collaborate with Airbnb, Uber, and Apple for **exclusive offers and joint promotions**.  

4. **Improve Transfer Experience**  
   - Simplify peer-to-peer (P2P) transfers to encourage higher usage and value.  

---

##  Limitations
- **Data Scope:** Limited to provided dataset, excluding external factors (economy, competitors, customer surveys).  
- **Demographic Depth:** Segmentation limited to generation; no location/profession data available.  

---
![markus-spiske-j2s9TffBQLk-unsplash](https://github.com/user-attachments/assets/284e76ef-1e9d-48f2-b73b-bfa68eb3c608)


## Conclusion
This project successfully leverages **data visualization** to provide a clear and actionable overview of **Metro Bank’s transaction landscape**.  

- **Branches** remain crucial for high-value transactions.  
- **POS and Digital channels** dominate for everyday customer interactions.  

The insights and recommendations can help Metro Bank:  
- Enhance customer satisfaction  
- Optimize service channels  
- Drive sustainable growth through **data-driven strategy**  


# 📊 PhonePe Payment Insights Dashboard (Power BI)

> An end-to-end Power BI dashboard analysing **300K UPI transactions worth ₹3.47bn** across **108K users**, built to uncover payment performance, user behaviour and growth opportunities.

![Dashboard Preview](images/dashboard.png)

---

## 🎯 Business Problem

A digital payments company needs to answer questions like:

- How reliable are our payments (success vs failed vs pending)?
- Which months and services drive the most transaction value?
- Which age groups and users contribute the most?
- When should we run offers to boost low-activity periods?

This dashboard turns raw transaction data into clear, decision-ready insights.

---

## 📈 Key Insights

| Metric | Value |
|---|---|
| Total Transactions | **300K** |
| Total Transaction Value | **₹3.47bn** |
| Unique Users | **108K** |
| Success Rate | **96.00%** |
| MoM Growth | **8.98%** |

- ✅ **High reliability:** 96% of payments succeed, indicating a strong payment experience.
- 📅 **Seasonality:** Activity peaks in **Jan, Mar, May, Jul and Oct**, with dips in **Feb and Jun**.
- 👥 **Age mix:** **Gen X (~42%)** is the largest segment, followed by Millennials (~37%) and Gen Z (~21%).
- 🗓️ **Usage pattern:** Weekdays account for ~72% of transactions vs ~28% on weekends.
- 💳 **Service value:** **Loans** drive the highest transaction value, well ahead of Insurance, Money Transfer and Recharge Bills.
- 💡 **Recommendation:** Run cashback and offers in low-activity months, and reduce failed/pending payments to lift the success rate further.

---

## 🗂️ Dashboard Pages

| Page | What it shows |
|---|---|
| **Page 1 (Overview)** | KPI cards, transactions over time, age segment contribution, service value analysis, top 5 users, weekday vs weekend usage, insights |
| **Service Type** | Total transactions by service type (UPI ID, Self Account, Mobile Number, QR Code, Bike Loan) |
| **Age Group** | Transaction share by Age_Group (Gen X, Millennials, Gen Z) |

**Interactive filters:** Month slicer and Payment Status buttons (Failed / Pending / Successful).

---

## 🛠️ Tools & Skills Used

- **Power BI Desktop:** data modelling, visuals, slicers, custom UI design
- **DAX:** measures such as Total Transactions, Successful Transactions, Success Rate, MoM Growth
- **Excel:** data preparation and cleaning
- **SQL:** data exploration and validation
- **Data Storytelling:** insight-driven layout with a clear recommendation

### Sample DAX

```DAX
Total Transactions = COUNTROWS(All_Transactions)

Successful Transactions =
CALCULATE([Total Transactions], All_Transactions[Payment_Status] = "Successful")

Success Rate =
DIVIDE([Successful Transactions], [Total Transactions])
```

---

## 🧾 Dataset

The dataset is synthetic and contains two tables:

| Table | Rows | Columns |
|---|---|---|
| `All_Transactions` | 300,000 | Transaction_ID, Amount, User_ID, Service, Service Type, Payment_Status, Reason, Date |
| `All_Users` | 107,658 | User_ID, Name, Age, Join_Date |

Tables are linked on `User_ID` (one user → many transactions).

---

## 📁 Repository Structure

```
PhonePe-Payment-Insights-PowerBI/
│
├
├── PhonePay.pdf                   # Exported dashboard (all pages)
├── Phonepe-Final-Dataset.xlsx     # Dataset
├── images/
│   └── dashboard.png              # Dashboard screenshot
└── README.md
```

---

## ▶️ How to Open

1. Clone or download this repository.
2. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
3. Open `PhonePay.pbix`.
4. If prompted, update the data source path to `Phonepe-Final-Dataset.xlsx` via **Transform data → Data source settings**.

---

## 🚀 What I Learned

- Designing a clean, branded dashboard with a clear visual hierarchy
- Writing DAX measures and formatting them correctly (count vs percentage)
- Turning numbers into business recommendations, not just charts
- Using slicers and cross-filtering for interactive analysis

---

## 👤 Author

**Aaryan**
BCA Graduate | Aspiring Data Analyst
📍 Haryana, India

🔗 [LinkedIn](https://www.linkedin.com/in/your-profile) · 💻 [GitHub](https://github.com/your-username)

⭐ If you found this project useful, consider giving it a star!

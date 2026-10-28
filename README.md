# 🚆 UK Train Rides Analysis Dashboard | Power BI

## 📌 Project Overview

This project presents an interactive Power BI dashboard built using the **UK Train Rides** dataset provided by **Maven Analytics**. The dashboard transforms raw railway transaction data into meaningful business insights, enabling stakeholders to monitor operational performance, revenue trends, and customer travel patterns.

The dashboard was developed by understanding the business requirements and converting them into interactive visualizations using Power BI.

---

## 📂 Dataset

- **Dataset:** railway.csv
- **Source:** Maven Analytics
- **Rows:** 30,000+
- **Tool Used:** Power BI Desktop

---

## 🎯 Business Requirements

The dashboard answers the following business questions:

- What are the most popular train routes?
- What are the peak travel hours?
- How does revenue vary by ticket types and ticket classes?
- What is the on-time performance?
- What are the main contributing factors behind train delays?

---

## 📊 Dashboard KPIs

The dashboard includes the following Key Performance Indicators:

- 💰 Total Revenue
- ✅ On-Time %
- ⚠️ Delayed %
- ❌ Cancelled %
- 🚆 Number of Delays
- 🎫 Number of Transactions

---

## 📈 Dashboard Visuals

- Revenue KPI Card
- On-Time Performance KPI
- Delay Percentage KPI
- Cancellation Percentage KPI
- Number of Delays KPI
- Total Transactions KPI
- Most Popular Routes
- Peak Travel Hours Analysis
- Revenue by Ticket Class
- Revenue by Ticket Type
- Delay Contributing Factors

---

## 🛠 Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Data Visualization

---

## 📐 DAX Measures Used

### Revenue

```DAX
Revenue =
SUM(railway[Price])

No of Transactions =
COUNTROWS(railway)

On Time % =
DIVIDE(
    CALCULATE(
        COUNTROWS(railway),
        railway[Journey Status] = "On Time"
    ),
    COUNTROWS(railway)
)

No of Delays =
CALCULATE(
    COUNTROWS(railway),
    railway[Journey Status] = "Delayed"
)

Delayed % =
DIVIDE(
    CALCULATE(
        COUNTROWS(railway),
        railway[Journey Status] = "Delayed"
    ),
    COUNTROWS(railway)
)

Cancelled % =
DIVIDE(
    CALCULATE(
        COUNTROWS(railway),
        railway[Journey Status] = "Cancelled"
    ),
    COUNTROWS(railway)
)

🔍Key Insights
Identified the busiest train routes based on passenger demand.
Analyzed peak travel hours throughout the day.
Compared revenue across different ticket classes and ticket types.
Measured overall operational performance using On-Time, Delayed, and Cancelled ride percentages.
Identified the major factors contributing to train delays such as weather, technical issues, staffing, and signal failures.

UK-Train-Rides-Analysis-PowerBI
│
├── Dashboard Screenshot.png
├── UK_Train_Rides_Analysis.pbix
├── railway.csv
├── README.md
└── LICENSE

⭐ Learning Outcomes
Through this project, I strengthened my skills in:
Power BI Dashboard Development
Data Cleaning using Power Query
Data Modeling
DAX Measure Creation
KPI Design
Business Intelligence Reporting
Data Storytelling
Revenue =
SUM(railway[Price])

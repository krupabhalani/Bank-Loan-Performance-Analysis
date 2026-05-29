# 📊 Bank Loan Report | Power BI Dashboard

## 📌 Project Overview

### 🏦 Project Name

**Bank Loan Report**

### 🎯 Goal / Objective

The objective of this project is to analyze bank loan data to monitor lending performance, evaluate loan quality, track repayment behavior, and identify business insights that help financial institutions make data-driven decisions.

This dashboard enables stakeholders to:

* Monitor loan applications and funding trends
* Analyze good vs bad loans
* Evaluate customer repayment behavior
* Track month-over-month (MoM) performance
* Identify high-risk loan segments
* Understand lending distribution across states, terms, purposes, and employee lengths

---

## 🚀 Key Insights / Value Added

### ✅ Business Insights Delivered

* Identified **86.2% Good Loans** indicating healthy lending performance
* Analyzed **13.8% Bad Loans** to highlight potential financial risks
* Tracked **$435.8M Total Funded Amount** and **$473.1M Total Received Amount**
* Measured monthly funding growth using **MTD & PMTD analysis**
* Found major loan purposes such as:

  * Debt Consolidation
  * Credit Card
  * Home Improvement
* Analyzed loan distribution by:

  * State
  * Grade
  * Home Ownership
  * Employment Length
  * Loan Term

### 💡 Value Added

* Improved visibility into lending operations
* Enabled faster executive decision-making
* Simplified risk analysis through interactive visuals
* Automated KPI tracking using DAX measures
* Enhanced data storytelling with dynamic filtering and drill-down analysis

---

# 🛠 Technologies Used

| Category            | Tools / Technologies            |
| ------------------- | ------------------------------- |
| BI Tool             | Power BI Desktop                |
| Data Source         | CSV Files                       |
| Data Transformation | Power Query (M)                 |
| Data Modeling       | Power BI Relationships          |
| Calculations        | DAX (Data Analysis Expressions) |
| Visualization       | Interactive Charts & KPI Cards  |

---

# 📂 Dataset Information

The dataset contains loan-level financial records including:

* Loan Amount
* Loan Status
* Interest Rate
* Installment Amount
* DTI Ratio
* Purpose
* Grade & Sub Grade
* Home Ownership
* Employee Length
* State
* Issue Date

---

# 📈 Dashboard Pages

## 1️⃣ Summary Page

Provides high-level KPIs and loan performance overview.

### KPIs Included

* Total Loan Applications
* Total Funded Amount
* Total Received Amount
* Average Interest Rate
* Average DTI
* Good Loan vs Bad Loan Analysis
* MTD & MoM Performance

---

## 2️⃣ Overview Page

Provides detailed trend and segmentation analysis.

### Visual Analysis Includes

* Total Funded Amount by Month
* Loan Distribution by Term
* Loan Distribution by Purpose
* Funded Amount by State
* Employee Length Analysis
* Home Ownership Analysis

---

## 3️⃣ Details Page

Provides transaction-level loan details for deep analysis.

### Table Insights

* Loan ID
* Purpose
* Grade
* Interest Rate
* Installment
* Funded Amount
* Received Amount
* Issue Date

---

# 📊 Key DAX Measures

## Total Funded Amount

```DAX
Total Funded Amount =
SUM(financial_loan[loan_amount])
```

## MTD Funded Amount

```DAX
MTD Funded Amount =
CALCULATE(
    TOTALMTD(
        [Total Funded Amount],
        'Date Table'[Date]
    )
)
```

## PMTD Funded Amount

```DAX
PMTD Funded Amount =
CALCULATE(
    [Total Funded Amount],
    DATESMTD(
        DATEADD('Date Table'[Date], -1, MONTH)
    )
)
```

---

# 📌 Additional Features

✅ Dynamic Filtering & Slicers

* State Filter
* Grade Filter
* Purpose Filter
* Loan Status Filter

✅ Good vs Bad Loan Classification

✅ Drill-through Analysis

✅ Interactive KPI Cards

✅ MoM Trend Analysis

✅ Responsive Dashboard Navigation

---

# 🧩 Data Model

## Fact Table

### `financial_loan`

Contains all transactional loan records.

### Important Columns

* loan_amount
* total_payment
* int_rate
* dti
* issue_date
* loan_status
* purpose
* address_state
* grade

---

## Dimension Table

### `Date Table`

Used for:

* Time Intelligence
* MTD Analysis
* Monthly Trends
* MoM Comparison

### Relationship

```text
Date Table[Date]  →  financial_loan[issue_date]
```

---

# 🎨 Visuals Used

| Visual Type             | Purpose               |
| ----------------------- | --------------------- |
| KPI Cards               | Performance Tracking  |
| Line Chart              | Monthly Trends        |
| Bar Charts              | Comparative Analysis  |
| Donut Charts            | Loan Distribution     |
| Matrix/Table            | Detailed Records      |
| Slicers                 | Interactive Filtering |
| Map Visual *(Optional)* | State-wise Analysis   |

---

# 🖥 Screenshots

## 📌 Dashboard Preview

> Find Financial Bank Loan Dashboard.pdf

---

# 🧭 Dashboard Navigation

## 📍 How to Interact with Dashboard

### 🔹 Page 1: Summary

* View overall KPIs
* Analyze Good vs Bad Loans
* Monitor monthly performance

### 🔹 Page 2: Overview

* Explore trends by:

  * State
  * Purpose
  * Loan Term
  * Employment Length

### 🔹 Page 3: Details

* Analyze individual loan transactions
* Use filters for granular insights

### 🎛 Navigation Buttons

Use the bottom navigation buttons:

* Summary
* Overview
* Details

to switch between pages interactively.

---

## ☁️ Power BI Service Deployment

### 📌 Publishing Dashboard to Power BI Service

After developing the dashboard in Power BI Desktop, the report was successfully published to **Power BI Service** for cloud-based access, sharing, and collaboration.

---

# 🚀 Steps to Publish Dashboard

## 1️⃣ Save the Power BI Report

## 2️⃣ Sign In to Power BI Desktop

* Open **Power BI Desktop**
* Click:

```text
File → Sign In
```

* Login using your Power BI account

---

## 3️⃣ Publish the Report

Click the **Publish** button from the Home ribbon.

```text
Home → Publish
```

---

## 4️⃣ Select Workspace

Choose the destination workspace:

## 5️⃣ Upload Successful

After publishing:

```text
Your report has been successfully published to Power BI Service.
```

---

# 🌐 Accessing Dashboard in Power BI Service

Open:

```text
https://app.powerbi.com
```

Navigate to:

```text
Workspace → Bank Loan Report
```

---

# 📊 Features Used in Power BI Service

✅ Interactive Report Sharing

✅ Auto Refresh Support

✅ Web Access Anywhere

✅ Dashboard Pinning

✅ Secure Workspace Collaboration

---

# 🔄 Data Refresh Configuration

Configured scheduled refresh to keep dashboard data updated automatically.

### Steps:

```text
Power BI Service
→ Dataset Settings
→ Scheduled Refresh
→ Configure Credentials
→ Set Refresh Timing
```

---

# 🔐 Sharing & Collaboration

The dashboard can be shared securely with:

* Managers
* Business Analysts
* Financial Teams
* Stakeholders

### Sharing Option:

```text
Share → Enter Email Address → Send
```

---

# 📱 Accessibility

The published dashboard can be accessed on:

* Desktop Browser
* Mobile Devices
* Power BI Mobile App

---

# 🎯 Benefits of Publishing to Power BI Service

* Real-time accessibility
* Centralized reporting
* Better stakeholder collaboration
* Automated report distribution
* Improved decision-making speed

---

# 📊 Business Impact

This dashboard helps banking stakeholders:

* Reduce loan default risk
* Improve lending strategy
* Monitor repayment efficiency
* Identify profitable customer segments
* Enhance operational reporting

---

# 🔮 Future Enhancements

* Predictive Loan Default Analysis
* Integration with SQL Database
* Real-Time Data Refresh
* Customer Segmentation using ML
* Advanced Risk Scoring

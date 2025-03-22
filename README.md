# UPI Transaction Analysis Dashboard 🚀
![image](https://github.com/user-attachments/assets/287c71aa-410b-4e0f-87fc-ac487f372dfc)

## 📌 Project Overview
This Power BI dashboard provides an in-depth analysis of UPI transactions, visualizing key insights such as spending trends, payment method preferences, failure rates, and merchant-wise transactions. The dashboard enables users to track transaction patterns, identify issues, and optimize digital payment experiences.

## 📊 Key Features
- **📈 Amount Spending Trend Using UPI**: A line chart displaying the monthly trend of transaction amounts.
- **🏪 Total Transaction Amount by Merchant and Payment Method**: A bar chart comparing transaction amounts across different merchants and payment methods.
- **💳 UPI Payment Method Preferences**: A pie chart showcasing the distribution of different payment methods (UPI ID, Phone Number, QR Code).
- **⚠️ Failure Rate by Month-Year**: A KPI visualization tracking the failure rate of transactions over time.
- **📍 City-Wise Transactions Trend**: A geographical map highlighting transaction volumes across different cities.
- **🧑‍💼 UPI Trend Based on Age**: A combined bar and line chart showing transaction amounts segmented by customer age groups.

## 🛠️ Tech Stack
- **🔹 Power BI**: Used for data visualization and interactive dashboard creation.
- **🔹 DAX**: Custom calculations for KPI metrics.

## 📂 Dataset Fields
The dataset contains transaction details with the following key fields:
- **Amount**: Transaction amount.
- **PaymentMethod**: UPI ID, QR Code, or Phone Number.
- **TransactionDate**: Date of the transaction.
- **Status**: Success or Failed transactions.
- **MerchantName**: Name of the merchant where the transaction was made.
- **CustomerAge**: Age of the customer.
- **City, BankNameSent, BankNameReceived**: Additional transaction details.

## 📌 DAX Measures Used
1. **Failure Rate Calculation**
   ```DAX
   Failure Rate = 
   DIVIDE(
       COUNTROWS(FILTER('UPI Transactions', 'UPI Transactions'[Status] = "Failed")),
       COUNTROWS('UPI Transactions'),
       0
   ) * 100

This `README.md` is designed to show recruiters that you are not just a coder, but a **Data Analyst** who understands the full end-to-end pipeline: from raw SQL data to statistical proof and business-ready dashboards.

Copy and paste the content below into a file named `README.md` in your project folder.

---

# Retail Customer Churn & Segmentation Analysis

### 📊 Project Overview

This project analyzes transactional data from a UK-based online retailer to identify customer churn patterns and segment the customer base using **RFM (Recency, Frequency, Monetary) Analysis**. As a Data Analyst, the goal was to transform raw sales data into actionable business insights that can help the marketing team reduce churn and increase customer retention.

### 🛠️ Tech Stack

* **SQL (SQLite):** For data aggregation and calculating customer-level metrics.
* **Python (Pandas, Scipy, Seaborn):** For data cleaning, RFM scoring, and statistical hypothesis testing (T-Tests).
* **Power BI:** For building an interactive executive dashboard to visualize churn risk and geographic performance.

---

### 🚀 Data Pipeline & Methodology

#### 1. Data Cleaning (Python)

* Handled ~400,000 transactions, removing cancellations (negative quantities) and invalid unit prices.
* Standardized date formats and handled missing `CustomerID` values to ensure data integrity.

#### 2. Feature Engineering (SQL)

* Used SQL to "flatten" transactional data into a **Customer Master Table**.
* Calculated **RFM Metrics**:
* **Recency:** Days since last purchase (Reference date: Dec 10, 2011).
* **Frequency:** Count of unique orders.
* **Monetary:** Total revenue per customer.


* Defined **Churn**: Formally labeled customers as "Churned" if they had not made a purchase in over **90 days**.

#### 3. Statistical Validation (Python)

* Performed an **Independent T-Test** to compare the spending habits of active vs. churned customers.
* **Result:** P-value < 0.05, confirming that the difference in monetary value is statistically significant, validating that our churned customers were indeed lower-value shoppers before leaving.

#### 4. RFM Segmentation

* Assigned scores (1-5) to each customer based on their RFM metrics.
* Segmented customers into categories: **Champions**, **At Risk**, **Loyalists**, and **Hibernating**.

---

### 📈 Key Insights & Dashboard

* **Overall Churn Rate:** [Insert your calculated churn rate, e.g., 35.2%].
* **Revenue at Risk:** Identified that [X]% of total revenue is currently tied to "At Risk" segments.
* **Geographic Trend:** The UK represents the highest volume, while [Country] shows a rising churn trend requiring immediate intervention.

---

### 💡 Business Recommendations

1. **Retention Campaign:** Target "At Risk" customers with personalized discount codes before they hit the 90-day churn threshold.
2. **VIP Program:** Launch a loyalty program for "Champions" to increase their average order value (AOV).
3. **Re-engagement:** Investigate the "Hibernating" segment to understand if they left due to product dissatisfaction or competitor pricing.

---

### 📂 Folder Structure

* `Data/`: Contains the cleaned CSV files.
* `Notebooks/`: Jupyter Notebook with Python cleaning and statistical tests.
* `Sql/`: SQL scripts used for RFM aggregation.
* `Dashboard/`: Power BI `.pbix` file.
* `README.md`: Project documentation.

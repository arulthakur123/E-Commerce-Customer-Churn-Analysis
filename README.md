# E-Commerce Customer Churn Analysis (India-Based)

This project focuses on understanding customer behavior in an Indian e-commerce environment by analyzing sales data from multiple sources such as Amazon, international platforms, and internal reports. The goal is to identify customer churn patterns, segment customers using RFM analysis, and derive actionable business insights.

## 📁 Project Structure

```
churn/
│
├── data_cleaned/                  # Cleaned CSV files
├── final_outputs/                # Final RFM and Churn CSVs
├── visualizations/               # Graphs and plots (optional)
├── EDA & RFM Analysis.ipynb      # Full working notebook
├── README.md                     # Project overview and insights (this file)
```

## 📊 Step-by-Step Workflow

### Step 1: 📦 Data Collection & Cleaning

**Files Used:**
- Amazon Sale Report
- International Sale Report
- Cloud Warehouse Comparison Chart
- Sale Report

**Actions:**
- Parsed dates (`pd.to_datetime`)
- Converted numeric fields (`pd.to_numeric`)
- Removed missing or corrupted data

---

### Step 2: 📈 Exploratory Data Analysis (EDA)

#### 1. **Amazon Sales Over Time**
- **Visualization:** Line plot of daily sales
- **Insight:** Identified peak revenue days and consistent growth patterns

#### 2. **Amazon Orders by Fulfilment Method**
- **Visualization:** Countplot using `sns.countplot`
- **Insight:** Fulfilment method impacts volume and possibly churn

#### 3. **Top 10 Most Sold SKUs**
- **Visualization:** Bar plot of SKUs
- **Insight:** Focused product sales contributing to majority revenue

#### 4. **International Sales Over Time**
- **Visualization:** Line plot
- **Insight:** Showed periodic spikes (seasonal demand patterns)

#### 5. **Cloud Warehouse Comparison**
- **Visualization:** Boxplot comparing Shiprocket vs INCREFF
- **Insight:** Shiprocket had higher variance; INCREFF more stable profitably

#### 6. **Stock Distribution by Category**
- **Visualization:** Bar plot
- **Insight:** Certain categories dominate inventory; potential risk of deadstock

---

### Step 3: 🔍 RFM Analysis

Used Amazon customer transactions to compute:

- **Recency:** Days since last purchase
- **Frequency:** Number of purchases
- **Monetary:** Total spend

Then calculated:

- RFM Score (R_F_M)
- Segmented users into: **Loyal**, **At Risk**, and **Others**

**Visualization:**
- **Boxplot:** Monetary by RFM segment
- **Insight:** Loyal customers have high spend, “At Risk” show potential churn

---

### Step 4: 🛑 Churn Prediction via RFM Segments

- Based on RFM scores, churn status was defined:
  - `Retained`: High frequency + low recency
  - `Churn Likely`: Low frequency + high recency
  - `Needs Nurturing`: Mid-range users who need reactivation

**Final Churn Distribution:**
```
Needs Nurturing    - 5147 users
Churn Likely       - 1708 users
Retained           - 302 users
```

---

## ✅ Business Value & Outcomes

- Identified 2,000+ high-risk users for churn campaigns.
- Highlighted best-selling SKUs and categories for stocking.
- Detected fulfilment channel trends for performance optimization.
- Created customer personas using RFM for targeted marketing.

---

## 🚀 Next Steps

- Build ML model on top of RFM segments (optional)
- Integrate user-level web tracking to enrich features
- Connect with CRM for automated churn retention campaigns

---

## 👨‍💻 Tools & Technologies

- Python (Pandas, Seaborn, Matplotlib)
- GitHub (Version control & project hosting)
- Jupyter Notebook

---

## 📌 Author

- **Name:** Arul Thakur
- **GitHub:** [arulthakur123](https://github.com/arulthakur123)

---

## 📎 License

This project is open-source and free to use.
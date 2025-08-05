# Customer Segmentation Using Clustering

Original Dataset from https://archive.ics.uci.edu/dataset/352/online+retail

To properly render Plotly (px) visualizations, please visit my Kaggle site project

https://www.kaggle.com/code/ariesuryow/eda-clustering-online-retail/notebook



## 📌 Project Overview
This project focuses on customer segmentation for an online retail business using unsupervised machine learning (clustering). By segmenting customers based on purchasing behavior, businesses can tailor marketing strategies and improve customer retention.

---

## 🎯 Problem Statement
The business has thousands of customers but lacks a structured way to group them based on behavior. The goal is to segment customers into distinct groups to:
- Identify loyal vs. at-risk customers
- Improve marketing targeting
- Enhance customer lifetime value

---

## 🧾 Dataset Overview
The dataset comes from a UK-based online retailer and contains transactions from 2010 to 2011. Key features include:

- **InvoiceNo**: Unique ID per transaction (prefix 'C' = cancellation)
- **StockCode**: Product/item ID
- **Description**: Item name
- **Quantity**: Number of items purchased
- **InvoiceDate**: Date of transaction
- **UnitPrice**: Price per item (£)
- **CustomerID**: Unique customer identifier
- **Country**: Customer location

---

## 🧹 Data Cleaning
Before clustering, the following steps were taken:
- Removed null/missing `CustomerID`
- Filtered out canceled orders (`InvoiceNo` starting with 'C')
- Handled duplicates and extreme outliers

---

## 📊 RFM Analysis
We created three metrics per customer:
- **Recency**: Days since last purchase
- **Frequency**: Total number of purchases
- **Monetary**: Total amount spent

These features were normalized and used for clustering.

---

## 🔍 Clustering Technique
- Applied **KMeans Clustering**
- Chose optimal number of clusters using the **Elbow Method**
- Segmented customers into meaningful clusters based on RFM scores

---

## 🎨 Customer Segments

### 1. Cluster 0 – **Bonus** (Cyan)
- High value, loyal customers who purchase frequently and recently
- 📌 **Strategy**: Loyalty programs, exclusive discounts, and personalized offers

### 2. Cluster 1 – **Reconnect** (Green)
- Infrequent buyers, low value, not recent
- 📌 **Strategy**: Reactivation campaigns, special promotions

### 3. Cluster 2 – **Growth** (Magenta)
- Recent, occasional buyers with growth potential
- 📌 **Strategy**: Relationship-building, exceptional customer service

### 4. Cluster 3 – **Preserve** (Blue)
- High value, frequent, and recent buyers
- 📌 **Strategy**: Maintain loyalty, offer personalized engagement

---

## 🚨 Outlier Clusters

### 5. Cluster 4 – **Casuals** (Salmon)
- Occasional low spenders who purchased recently
- 📌 **Strategy**: Retargeting ads to prompt more frequent purchases

### 6. Cluster 5 – **Quiet** (Red)
- Least engaged customers, no recent activity
- 📌 **Strategy**: Win-back campaigns with strong incentives

---

## 💡 Business Recommendations
- Personalize marketing based on segment
- Invest in loyalty rewards for high-value clusters
- Target reactivation efforts toward "Reconnect" and "Quiet" segments
- Run upsell campaigns for "Growth" and "Casual" clusters

---

## ✅ Conclusion
Using RFM-based clustering, we successfully identified key customer segments. These insights can help the business boost customer retention, improve marketing ROI, and grow revenue through targeted strategies.

---

## 📁 Tools & Technologies
- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- Jupyter Notebook
- KMeans Clustering
- RFM Analysis

---

## 📌 Next Steps
- Integrate time-series analysis to monitor cluster evolution
- Apply A/B testing on marketing strategies
- Build dashboards for real-time customer monitoring


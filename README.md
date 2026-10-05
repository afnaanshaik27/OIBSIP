# Customer Segmentation Analysis

## 📌 Project Overview

This project performs **Customer Segmentation Analysis** for an e-commerce business using **RFM (Recency, Frequency, Monetary) analysis** and the **K-Means clustering algorithm**.

The goal is to identify groups of customers with similar purchasing behaviour so that businesses can develop targeted marketing strategies for different customer segments.

This project was completed as part of the **Oasis Infobyte (OIBSIP) Data Analytics Internship – Level 1 Task 2**.

---

## 🎯 Objective

The main objectives of this project are:

* Analyze customer purchasing behaviour.
* Clean and prepare the e-commerce transaction data.
* Calculate Recency, Frequency, and Monetary (RFM) metrics.
* Standardize the RFM features.
* Determine the optimal number of clusters using the Elbow Method.
* Apply K-Means clustering.
* Profile and interpret each customer segment.
* Develop marketing recommendations for each segment.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

---

## 📂 Dataset

**Dataset:** Online Retail Dataset

The dataset contains transactional information from an online retail business, including:

* Invoice Number
* Stock Code
* Description
* Quantity
* Invoice Date
* Unit Price
* Customer ID
* Country

The dataset was cleaned before performing the customer segmentation analysis.

---

## 🧹 Data Cleaning

The following preprocessing steps were performed:

* Removed records with missing `CustomerID`.
* Removed cancelled invoices.
* Removed transactions with invalid or non-positive quantities.
* Removed transactions with invalid or non-positive unit prices.
* Converted `InvoiceDate` to datetime format.
* Created a `TotalPrice` feature using:

```text
TotalPrice = Quantity × UnitPrice
```

After cleaning, the data was used to calculate customer-level RFM metrics.

---

## 📊 RFM Analysis

Three behavioural features were selected for customer segmentation:

### Recency

Number of days since the customer's most recent purchase.

### Frequency

Number of unique purchases/orders made by the customer.

### Monetary

Total amount spent by the customer.

These three features provide a useful representation of customer purchasing behaviour.

---

## ⚙️ Data Standardization

Since Recency, Frequency, and Monetary have different scales, **StandardScaler** from Scikit-learn was used to standardize the features before applying K-Means clustering.

---

## 📈 Elbow Method

The Elbow Method was used to evaluate different values of K and identify a suitable number of clusters.

Based on the analysis, **K = 3** was selected for the final K-Means model.

---

## 🤖 K-Means Clustering

K-Means clustering was applied using:

* Number of clusters: **3**
* Random state: **42**
* `n_init`: **10**

The resulting clusters were interpreted based on their RFM characteristics.

---

## 👥 Customer Segments

| Customer Segment     | Customers | Percentage |
| -------------------- | --------: | ---------: |
| Regular Customers    |     3,230 |     74.46% |
| At Risk / Inactive   |     1,082 |     24.94% |
| High-Value Customers |        26 |      0.60% |
| **Total**            | **4,338** |   **100%** |

### Segment Characteristics

| Segment              | Avg. Recency | Avg. Frequency | Avg. Monetary |
| -------------------- | -----------: | -------------: | ------------: |
| High-Value Customers |         6.04 |          66.42 |     85,904.35 |
| Regular Customers    |        41.45 |           4.67 |      1,855.94 |
| At Risk / Inactive   |       247.11 |           1.58 |        631.42 |

---

## 🔍 Key Insights

### 1. Regular Customers

Regular Customers form the largest segment, representing **74.46%** of the customer base. They purchase relatively regularly and have an average recency of about 41 days.

### 2. At Risk / Inactive Customers

At Risk / Inactive Customers represent **24.94%** of customers. Their high average recency of approximately 247 days indicates that they have not purchased recently.

### 3. High-Value Customers

High-Value Customers represent only **0.60%** of the customer base but show exceptionally high purchasing activity and monetary value.

Their average frequency is **66.42 purchases**, with an average monetary value of **85,904.35**.

### 4. Customer Behaviour Differences

The RFM analysis clearly identifies different purchasing behaviours, allowing the business to create targeted strategies instead of treating all customers in the same way.

---

## 💡 Marketing Recommendations

### At Risk / Inactive Customers

* Send personalized re-engagement emails.
* Provide limited-time discounts or return incentives.
* Recommend products based on previous purchases.
* Create campaigns designed to bring inactive customers back.

### Regular Customers

* Encourage more frequent purchases through personalized offers.
* Use cross-selling and product recommendations.
* Introduce loyalty rewards.
* Provide targeted promotions based on purchasing history.

### High-Value Customers

* Provide VIP or premium loyalty benefits.
* Offer exclusive products and promotions.
* Provide personalized recommendations.
* Give early access to new products or special offers.
* Focus on maintaining long-term customer loyalty.

---

## 📊 Visualizations

The project includes visualizations for:

1. Elbow Method for selecting the number of clusters.
2. Frequency vs Monetary customer distribution.
3. Recency vs Monetary customer distribution.
4. Customer cluster profile.

All project screenshots are available in the `screenshots` folder.

---

## 📁 Project Structure

```text
DataAnalytics-L1-CustomerSegmentation/
│
├── OIBSIP_Task_2_Customer_Segmentation.ipynb
│
└── screenshots/
    ├── elbow-method.png
    ├── frequency-vs-monetary.png
    ├── recency-vs-monetary.png
    └── cluster-profile.png
```

---

## ▶️ How to Run the Project

1. Download or clone this repository.
2. Open `OIBSIP_Task_2_Customer_Segmentation.ipynb` using Jupyter Notebook or JupyterLab.
3. Ensure the required Python libraries are installed.
4. Place the `Online Retail.xlsx` dataset in the appropriate working directory.
5. Run the notebook cells sequentially to reproduce the analysis.

---

## 📌 Conclusion

The RFM-based K-Means clustering successfully segmented **4,338 customers into three distinct groups** based on purchasing behaviour.

The analysis shows that most customers are regular buyers, while a significant portion is at risk of becoming inactive. Although High-Value Customers represent a very small percentage of the customer base, they contribute exceptionally high purchasing activity and monetary value.

These segments can help businesses improve customer retention, personalize marketing campaigns, and focus resources on the customers with the greatest potential value.

---

## 🏷️ Internship

**Oasis Infobyte – OIBSIP Data Analytics Internship**

**Task:** Level 1 – Task 2
**Project:** Customer Segmentation Analysis

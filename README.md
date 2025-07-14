# customer-segmentation-ifood
# Customer Segmentation using KMeans Clustering

This project performs customer segmentation analysis for an e-commerce company using KMeans clustering on marketing and purchase behavior data. The segmentation helps identify different customer groups to improve targeted marketing, retention strategies, and overall business decisions.

---

## 📌 Project Goals

- Group customers into meaningful segments based on behavioral and demographic features.
- Discover customer personas such as high-spenders, deal-seekers, and inactive users.
- Enable data-driven marketing strategies using customer clusters.

---

## 📁 Dataset

- Source: `ifood_df.csv` (from Kaggle)
- Rows: ~2,200 customers
- Features: Demographics, product purchases, web/catalog/store interactions, campaign responses

---

## 🧪 Steps Performed

### ✅ 1. **Data Exploration & Cleaning**
- Removed unnecessary columns (`ID`, `Z_CostContact`, etc.)
- Handled missing values
- Parsed date fields
- One-hot encoded categorical variables (`Education`, `Marital_Status`)

### ✅ 2. **Feature Engineering**
- Created:
  - `Customer_Days`: Customer tenure
  - `MntTotal`: Total spend across all products
  - `MntRegularProds`: Non-luxury product spending
- Selected relevant features:
  - `Income`, `Recency`, `Customer_Days`, `NumDealsPurchases`, etc.

### ✅ 3. **Standardization**
- Scaled features using `StandardScaler` to prepare for clustering

### ✅ 4. **KMeans Clustering**
- Used **Elbow Method** to determine optimal number of clusters (K = 4)
- Applied KMeans and assigned each customer to a `Cluster`
- Calculated `Silhouette Score` to evaluate clustering performance

### ✅ 5. **Visualization**
- Boxplots for `Income`, `MntTotal`, `Recency`, etc. by cluster
- Scatter plots to show cluster separation
- Bar plots comparing average features across clusters

---

## 📊 Results & Insights

- **Cluster 0**: High-income, high-spending, frequent buyers → Premium segment
- **Cluster 1**: Low-income, inactive, low spend → Low-value segment
- **Cluster 2**: Young customers, web-savvy, moderate spend → Digital-focused segment
- **Cluster 3**: Deal seekers with high response to campaigns → Promotional segment

---

## 📈 Visuals

| Plot Type         | Description                        |
|------------------|------------------------------------|
| Elbow Curve       | To find optimal number of clusters |
| Boxplots          | Income / Spend distribution by cluster |
| Scatter Plot      | Recency vs Spend by cluster        |
| Bar Chart         | Avg. values of key features per cluster |

---

## ⚙️ Technologies Used

- **Python 3**
- **Pandas**, **NumPy** – Data handling
- **Matplotlib**, **Seaborn** – Visualization
- **Scikit-learn** – KMeans clustering, preprocessing
- **Google Colab** – Development environment
- **Git + GitHub** – Version control & collaboration

---

## 🚀 How to Run This Project

1. Clone the repository:
   ```bash
  git clone
     https://github.com/Vikram7447/customer-segmentation-ifood

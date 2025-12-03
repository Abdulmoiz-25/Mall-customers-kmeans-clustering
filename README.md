# Mall Customers K-Means Clustering
---

## Objective
This assignment demonstrates the application of **K-Means clustering** on the Mall Customers dataset for **market segmentation**. The goal is to identify distinct customer groups and provide actionable insights for marketing strategies.

---

## Dataset
- **Dataset Used:** `Mall_Customers.csv`
- **Number of Rows:** 200  
- **Number of Columns:** 5  

### Columns
| Column | Description |
|--------|-------------|
| CustomerID | Unique customer identifier |
| Gender | Male/Female |
| Age | Customer age |
| Annual Income (k$) | Annual income in thousand dollars |
| Spending Score (1-100) | Score assigned by the mall based on spending habits |

---

## Tasks & Implementation

### 1. Load and Explore Dataset
- Loaded dataset into a **pandas DataFrame**
- Displayed summary statistics, missing values check, and first 10 rows
- **Summary Stats** example:  
  - Mean Age: 38.85  
  - Mean Annual Income: 60.56 k$  
  - Mean Spending Score: 50.2  

---

### 2. Data Preprocessing
- Converted `Gender` to numeric: Male = 0, Female = 1
- Selected features for clustering:
  - **Option A:** Age vs Spending Score
  - **Option B:** Annual Income vs Spending Score
- Standardized features
- Plotted scatter plots to visualize distributions  

**Figures:**  
- Option A: `OptionA_Age_vs_Spending_scatter.png`  
- Option B: `OptionB_Income_vs_Spending_scatter.png`  

---

### 3. K-Means Clustering
- Set **K = 5** clusters for both options
- Generated cluster plots with centroids marked as `X`

**Cluster Plots:**  
- Option A: `OptionA_Age_vs_Spending_clusters.png`  
- Option B: `OptionB_Income_vs_Spending_clusters.png`  

---

### 4. Elbow Method
- Calculated **WCSS** for K = 1 to 12
- Plotted **elbow curves** to determine optimal K  
- Suggested K: **5 for both options**  

**Elbow Curves:**  
- Option A: `OptionA_Age_vs_Spending_elbow.png`  
- Option B: `OptionB_Income_vs_Spending_elbow.png`  

---

### 5. Evaluation Metrics
| Experiment | Silhouette Score | Davies-Bouldin Index |
|------------|-----------------|--------------------|
| Option A   | 0.55            | 0.68               |
| Option B   | 0.61            | 0.72               |

- Interpretation:
  - Silhouette scores indicate moderately well-separated clusters
  - Davies-Bouldin <1 suggests clusters are compact and distinct

---

### 6. Business Interpretation

**Option A – Age vs Spending Score**
| Cluster | Description | Marketing Insights |
|---------|-------------|------------------|
| 0       | Young, High Spend | Events & trendy promotions |
| 1       | Young, Low Spend  | Loyalty programs, discounts |
| 2       | Middle-aged, Medium Spend | Premium offerings |
| 3       | Older, Low Spend | Essential product promotions |
| 4       | Middle-aged, High Spend | VIP/exclusive services |

**Option B – Income vs Spending Score**
| Cluster | Description | Marketing Insights |
|---------|-------------|------------------|
| 0       | Low Income, High Spend | Discounts, installments |
| 1       | Mid Income, Medium Spend | Targeted campaigns |
| 2       | High Income, Low Spend | Loyalty/exclusive offers |
| 3       | Mid Income, High Spend | Premium promotions |
| 4       | Low Income, Low Spend | Basic promotions, awareness |

---

### 7. Cluster Centroids

**Option A – Age vs Spending Score**
| Cluster | Age | Spending Score | Description |
|---------|-----|----------------|------------|
| 0       | 23  | 80             | Young, High Spend |
| 1       | 25  | 40             | Young, Low Spend |
| 2       | 40  | 60             | Middle-aged, Medium Spend |
| 3       | 55  | 20             | Older, Low Spend |
| 4       | 45  | 75             | Middle-aged, High Spend |

**Option B – Income vs Spending Score**
| Cluster | Income (k$) | Spending Score | Description |
|---------|-------------|----------------|------------|
| 0       | 25          | 80             | Low Income, High Spend |
| 1       | 75          | 50             | Mid Income, Medium Spend |
| 2       | 120         | 20             | High Income, Low Spend |
| 3       | 60          | 70             | Mid Income, High Spend |
| 4       | 35          | 40             | Low Income, Low Spend |

---

### 8. Conclusion & Recommendations
- K-Means clustering successfully segmented customers into meaningful groups
- Highlights patterns based on age, income, and spending behavior
- Recommendations:
  1. Target High Spend, Young/Mid-Income segments with promotions, events, and loyalty programs
  2. Offer discounts/installments to Low Income, High Spend segments
  3. Allocate marketing budgets efficiently based on cluster-specific strategies
- Provides actionable insights for **customer-centric marketing strategies**

---
**Author:** Abdul Moiz Meer  


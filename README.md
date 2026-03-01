# 🧩 Week 11 – Customer Segmentation & Prediction  
## Advanced Machine Learning Models

---

## 📌 Project Overview

This project focuses on applying **advanced machine learning techniques** to perform:

1. Customer segmentation using clustering algorithms  
2. Segment-specific churn prediction models  
3. Hyperparameter tuning and model optimization  
4. Business-driven insights and recommendations  

Instead of building one global model, customers are first segmented into meaningful groups. Then, separate predictive models are trained for each segment to improve performance and interpretability.

This approach allows businesses to make **targeted and data-driven decisions**.

---

## 🎯 Project Objectives

- Segment customers using unsupervised learning techniques
- Compare multiple clustering algorithms
- Build separate Random Forest models for each segment
- Perform hyperparameter tuning using GridSearchCV
- Evaluate models using comprehensive metrics
- Generate business recommendations based on segment behavior

---

## 📂 Project Structure
Customer_Segmentation_Project/
│
├── customer_segmentation.ipynb
├── segmentation_data.csv
├── segment_profiles.md
├── model_evaluation_results.csv
├── business_recommendations.pdf
├── requirements.txt
└── README.md


---

## 📊 Dataset Description

The dataset contains customer behavioral and financial attributes such as:

- Tenure
- MonthlyCharges
- TotalCharges
- Contract type
- PaymentMethod
- Churn (Target Variable)

The dataset includes both numerical and categorical features suitable for clustering and classification.

---

## 🧠 Methodology

### 1️⃣ Feature Preparation
- Selected relevant numerical features
- Applied StandardScaler for clustering

---

### 2️⃣ Clustering Algorithms Implemented

✔ K-Means Clustering  
✔ Hierarchical Clustering  
✔ DBSCAN (Exploratory comparison)

**Elbow Method** was used to determine the optimal number of clusters.

Final segmentation used **3 customer segments**.

---

### 3️⃣ Identified Customer Segments

- 🟦 Premium Spenders  
- 🟩 Budget Conscious Customers  
- 🟨 Young Professionals  

Detailed profiles are available in `segment_profiles.md`.

---

### 4️⃣ Segment-Specific Prediction Models

For each segment:
- A separate **Random Forest Classifier** was trained
- Data split into training and testing sets
- Model evaluated independently

---

## 📈 Model Evaluation Metrics

Each segment model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Example Output:


Premium Spenders: Accuracy = 92%, F1 = 0.89
Budget Conscious: Accuracy = 88%, F1 = 0.85
Young Professionals: Accuracy = 90%, F1 = 0.87


Evaluation results are saved in:

model_evaluation_results.csv


---

## ⚙️ Hyperparameter Tuning

Hyperparameter optimization was performed using:

- `GridSearchCV`
- Cross-validation (CV = 3)

Parameters tuned:
- Number of estimators
- Maximum tree depth
- Minimum samples split

This improved model generalization and reduced overfitting.

---

## 📊 Feature Importance Analysis

Random Forest feature importance was analyzed to understand:

- Which customer attributes influence churn
- Differences in feature importance across segments

---

## 💼 Business Recommendations

Segment-specific strategies were created and documented in:


business_recommendations.pdf


Examples:
- Premium Spenders → Loyalty programs & upselling
- Budget Customers → Competitive pricing
- Young Professionals → Engagement & referral incentives

---

## 🧪 Testing & Validation

- Clusters validated using inertia reduction (Elbow Method)
- Models evaluated on unseen test data
- Cross-validation used in hyperparameter tuning
- Segment balance verified before modeling

---

## ▶️ Setup Instructions

### 1️⃣ Install Dependencies

```bash
pip install -r requirements.txt
2️⃣ Run the Notebook

Open:

customer_segmentation.ipynb

Run cells sequentially.

📦 requirements.txt
pandas
numpy
matplotlib
seaborn
scikit-learn
scipy
🚀 Key Learnings

Combining clustering with classification improves prediction quality

Segment-specific models outperform a single global model

Hyperparameter tuning enhances performance stability

Data-driven segmentation supports targeted business decisions

# Amazon "Truth-O-Meter": Predictive Value Analysis

## 📌 Executive Summary

This project investigates the common consumer belief that **"higher price equals higher quality."** By analyzing over 1,400 electronics products from Amazon, I built a data pipeline to see if a product's price can actually predict its user rating.

**The Verdict:** Price is a poor predictor of satisfaction. The analysis revealed a **"Value Plateau,"** where paying more does not result in a better-rated product. This insight helps consumers and businesses focus on "Value Heroes" rather than just premium branding.

---

## 🛠️ The Data Pipeline

### 1. Data Cleaning (Pre-processing)

Raw retail data is often messy. I used **Python (Pandas)** to transform the dataset into a machine-readable format:

- **Currency Normalization:** Stripped currency symbols (₹) and commas from `actual_price` and `discounted_price`.
- **Data Type Conversion:** Converted text-based prices and ratings into **numerical floats** to allow for mathematical modeling.
- **Handling Missing Values:** Cleaned the dataset by removing incomplete entries to ensure the model's integrity.

---

### 2. Exploratory Data Analysis (EDA)

Before modeling, I visualized the relationship between cost and quality:

- **Correlation Check:** Used the **Pearson Correlation Coefficient** to measure the strength of the link between price and rating.
- **Trend Visualization:** Created scatter plots with regression lines using **Seaborn** to identify where price and quality diverge.

---

### 3. Machine Learning (Linear Regression)

I developed a **Multiple Linear Regression** model using **Scikit-Learn**:

- **Features:** Used `actual_price` and `discount_percentage` as predictors.
- **Validation:** Implemented an **80/20 train-test split** to verify the model’s accuracy on unseen data.

---

## 📈 Key Findings

- **The 5% Rule:** Price and discounts explain less than **5% of the variance** in user ratings. 95% of a product's success comes from factors other than its price tag.
- **The Value Plateau:** User satisfaction stays consistent (between 4.0 and 4.2 stars) across almost all price points above ₹1,000.
- **The Discount Paradox:** A slight negative correlation suggests that extreme discounts sometimes signal lower consumer satisfaction.

---

## 📂 Dataset Source

The data used for this analysis was sourced from Kaggle:

- **Dataset:** [Amazon Sales Dataset](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset)

---

## 🚀 How to Run

1. Clone this repository.
2. Install dependencies:
   ```bash
   pip install pandas seaborn scikit-learn matplotlib
3. Run the analysis script or Jupyter Notebook.
# 🏘️ California Housing: Exploratory Data Analysis (EDA) - 1990 Census

## 📖 Project Overview
A comprehensive Exploratory Data Analysis (EDA) of the California Housing dataset (1990 Census). This project investigates the impact of income, location, and population density on real estate values through statistical analysis, feature engineering, and geographic visualization.

**Key Goal:** Understand the drivers of the `median_house_value` to prepare the data for predictive Machine Learning models.

---

## 📌 Problem Statement
**The Challenge:** Predicting house values is complex because prices are influenced by inter-related factors like proximity to the ocean, house age, and local demographics.

**The Objective:** We need to perform deep statistical analysis to identify which features (e.g., `median_income`) have the strongest correlation with price and to discover data quality issues before modeling.

---

## 🏛️ Analytical Structure
This project is organized into four professional phases:

1. **Data Setup & Quality Check:**
   - Loaded the 1990 Census data.
   - Checked for data integrity and initial structural problems.

2. **Cleaning & Feature Engineering:**
   - **Missing Values:** Identified missing entries in `total_bedrooms` and imputed them using the **Median** (robust to outliers).
   - **Feature Creation:** Generated new metrics like `rooms_per_household` to compare relative density rather than raw totals.

3. **Statistical & Distribution Analysis:**
   - Analyzed the shape of features (skewness).
   - **Capping Discovery:** Discovered a critical issue where `median_house_value` is capped at **$500,001**, which acts as an artificial ceiling for predictions.

4. **Deep Relationship & Geographic Viz:**
   - **Correlation Matrix:** Confirmed that `median_income` is the strongest positive predictor of house value.
   - **Geospatial Analysis:** Visualized data on a map of California, revealing that coastal proximity significantly drives up prices.

---

## 💡 Key Insights & Results
* **Income Factor:** Median Income is the single most important predictor of housing prices.
* **Location:** Coastal districts ("Ocean Proximity") show distinct price clusters compared to inland areas.
* **Data Limitations:** The dataset contains "capped" values for both housing price and house age, which may bias linear regression models if not handled correctly.

---

## 🛠️ Technologies Used
* **Python 3.x**
* **Pandas:** For data manipulation and cleaning.
* **Seaborn & Matplotlib:** For statistical data visualization and heatmaps.
* **Scikit-Learn:** For data imputation (handling missing values).

---

## 🚀 How to Run This Notebook
1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
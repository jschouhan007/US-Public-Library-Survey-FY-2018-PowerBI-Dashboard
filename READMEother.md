# Public-Library-Survey-FY-2018-US-Data-Science
🚀 End-to-end data science project analyzing the US Public Library Survey. Features Exploratory Data Analysis (EDA), Random Forest ML models (Regression &amp; Classification), and Power BI dashboarding.
--------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------
# 📚 US Public Library Infrastructure Analysis & Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Random%20Forest-success.svg)
![Data Visualization](https://img.shields.io/badge/Data%20Visualization-Seaborn%20%7C%20PowerBI-yellow.svg)

## 📌 Project Overview
This project presents a comprehensive, data-driven analysis of the United States public library infrastructure using the FY2018 Public Library Survey (PLS) dataset. By examining over 17,000 library outlets, this study investigates the structural, geographic, and demographic factors that influence library operations. 

The project encompasses Data Cleaning, Exploratory Data Analysis (EDA), Statistical Hypothesis Testing, and Advanced Machine Learning to uncover actionable insights for urban planners and policymakers.

## 📊 Dataset
* **Source:** US Institute of Museum and Library Services (IMLS)
* **Records:** 17,478 Library Outlets
* **Key Variables:** Square Footage, Annual Operating Hours, Locale (Urban/Rural), Outlet Type (Central/Branch), and County Population.

## 🚀 Key Findings
1. **Infrastructure Strategy by Geography:** Urban communities heavily rely on decentralized Branch networks, whereas Rural populations depend almost exclusively on single Central hubs.
2. **Predicting Operations:** A facility's square footage and the surrounding county's population act as the strongest predictors of its operating hours.
3. **Core Access:** Branch and Central libraries combined make up **96%** of all physical library access in the US.

## 🧠 Machine Learning Models Built
* **Random Forest Regressor:** Predicts the *weekly operating hours* of a library based on its physical size and location demographics ($R^2 = 0.61$).
* **Random Forest Classifier:** Successfully categorizes the architectural role of a library (Central Hub vs. Branch) based on surrounding community features (Accuracy: 72%).
* **K-Means Clustering:** Unsupervised learning used to group libraries into distinct "Facility Tiers" for infrastructure planning.

## 🛠️ Technologies Used
* **Languages:** Python (Pandas, NumPy)
* **Data Visualization:** Matplotlib, Seaborn, Power BI
* **Machine Learning:** Scikit-Learn
* **Statistical Testing:** SciPy (ANOVA, Chi-Square)

## 💻 How to Run the Project
1. Clone this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<jschouhan007>/Public-Library-Survey-FY-2018-US-Data-Science.git
   

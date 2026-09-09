# 📚 US Public Library Infrastructure Analysis & Prediction
### End-to-End Data Science & Machine Learning Pipeline — FY2018 Public Library Survey (IMLS)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Random%20Forest%20%7C%20K--Means-success.svg)
![Visualization](https://img.shields.io/badge/Visualization-Seaborn%20%7C%20Power%20BI-yellow.svg)
![Statistics](https://img.shields.io/badge/Statistics-SciPy%20ANOVA%20%7C%20Chi--Square-red.svg)

---

## 🎯 CSAR Framework Overview

| | |
|---|---|
| **Challenge** | 17,478 US public library outlets operate with vastly different resources, but policymakers had no data-driven model to predict operational capacity or guide infrastructure investment. |
| **Situation** | The FY2018 Public Library Survey (PLS) — the US federal government's most comprehensive library census — contained 37 raw variables per outlet, with inconsistencies, missing values, and no ready-made analytical structure. |
| **Action** | Built a full data-science pipeline: data cleaning → feature engineering → EDA → statistical hypothesis testing (ANOVA, Chi-Square) → 3 ML models (Random Forest Regression, Random Forest Classification, K-Means Clustering) → Power BI executive dashboard. |
| **Result** | Regression model predicts weekly operating hours with **R² = 0.61**; classifier identifies library architectural role with **72% accuracy**; clustering segmented all 17,478 outlets into strategic "Facility Tiers"; findings deliver actionable intelligence for urban planners and policymakers. |

---

## 🔴 The Challenge

Public libraries are America's most accessible public infrastructure — yet decisions about funding, staffing, and facility expansion are frequently made without quantitative evidence. The core problems this project addresses:

1. **No predictive framework existed** to estimate a library's operating capacity from its physical and demographic characteristics.
2. **Urban vs. Rural infrastructure strategies were anecdotal**, not statistically validated.
3. **17,478 outlets with 37 attributes each** — a volume of federal survey data too large and too messy for manual analysis.
4. **Stakeholders (urban planners, policymakers, library boards)** needed insights translated into an interactive, non-technical format.

---

## 🟠 The Situation

**Dataset: FY2018 Public Library Survey (PLS) — US Institute of Museum and Library Services (IMLS)**

| Attribute | Detail |
|---|---|
| Records | **17,478 library outlets** (all 50 states) |
| Features | **37 raw variables** |
| Key Variables | Square Footage, Annual Operating Hours, Weeks Open, Locale (City/Suburban/Town/Rural), Outlet Type (Central/Branch/Bookmobile), County Population, State |
| Data Quality Issues | Missing values, negative/invalid entries, coded categorical variables requiring domain mapping |

The raw federal data required substantial wrangling before any statistical or ML work was possible — including encoding categorical survey codes (`OUTLET_TYPE`, `LOCALE_CAT`) into human-readable categories and engineering derived metrics.

---

## 🟡 The Action

### 1️⃣ Data Cleaning & Feature Engineering
- Removed duplicates and filtered invalid records (negative square footage / hours).
- Engineered new features, including **HOURS_PER_WEEK**, to normalize operational capacity.
- Mapped IMLS survey codes into readable locale and outlet-type categories for analysis.

### 2️⃣ Exploratory Data Analysis (EDA)
- Analyzed library density per state, outlet-type composition, and size distributions.
- Surfaced national benchmarks: **median library size = 6,550 sq ft**; **average operation = 2,174 hours/year across 51.4 weeks**.

### 3️⃣ Statistical Hypothesis Testing (SciPy)
- **ANOVA** to test whether operating hours differ significantly across locale categories (City/Suburban/Town/Rural).
- **Chi-Square** tests to validate associations between geography and infrastructure strategy.
- Confirmed a **statistically significant correlation between facility size and operating hours**.

### 4️⃣ Machine Learning (Scikit-Learn)
| Model | Task | Performance |
|---|---|---|
| **Random Forest Regressor** | Predicts weekly operating hours from facility size + location demographics | **R² = 0.61** |
| **Random Forest Classifier** | Classifies library architectural role (Central Hub vs. Branch) from community features | **72% accuracy** |
| **K-Means Clustering** | Unsupervised segmentation of outlets into distinct "Facility Tiers" for infrastructure planning | Actionable tier profiles |

### 5️⃣ Executive Visualization
- Statistical plots with **Matplotlib & Seaborn**.
- Interactive **Power BI dashboard** translating findings for non-technical policymakers and urban planners.

---

## 🟢 The Results

### Quantified Outcomes
- 📈 **R² = 0.61** regression model — square footage + county population proven as the strongest predictors of operating hours.
- 🎯 **72% classification accuracy** predicting whether a facility serves as a Central Hub or Branch from community demographics alone.
- 🗂️ **17,478 outlets segmented** into strategic Facility Tiers via unsupervised clustering — a reusable framework for infrastructure planning.
- 📊 Analyzed **100% of US public library outlets** (17,478 records × 37 features) — a complete national census, not a sample.

### Key Findings
1. **Infrastructure Strategy by Geography** — Urban communities rely on decentralized **Branch networks**; Rural populations depend almost exclusively on single **Central hubs**.
2. **Core Access** — Branch + Central libraries together make up **~96% of all physical library access** in the US.
3. **Scale Advantage** — City libraries are physically larger **and** open more hours than rural counterparts.
4. **Year-Round Access** — **82%+ of libraries operate all 52 weeks per year**.
5. **Predictive Drivers** — Facility square footage and county population are the dominant predictors of operational capacity.

### Business/Policy Impact
The models and Facility Tiers give urban planners and policymakers a **data-driven basis for funding allocation, facility sizing, and branch-vs-hub placement decisions** — replacing anecdote with evidence.

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.8+ |
| Data Wrangling | Pandas, NumPy |
| Machine Learning | Scikit-Learn (Random Forest, K-Means) |
| Statistical Testing | SciPy (ANOVA, Chi-Square) |
| Visualization | Matplotlib, Seaborn, Power BI |
| Environment | Jupyter Notebook |

---

## 🚀 How to Run

```bash
git clone https://github.com/jschouhan007/Public-Library-Survey-FY-2018-US-Data-Science.git
cd Public-Library-Survey-FY-2018-US-Data-Science
pip install pandas numpy scikit-learn scipy matplotlib seaborn
jupyter notebook
```

---

## 📝 ATS Keywords
`Data Science` `Machine Learning` `Random Forest` `K-Means Clustering` `Supervised Learning` `Unsupervised Learning` `Regression` `Classification` `Feature Engineering` `Exploratory Data Analysis` `EDA` `Hypothesis Testing` `ANOVA` `Chi-Square` `Python` `Pandas` `NumPy` `Scikit-Learn` `SciPy` `Matplotlib` `Seaborn` `Power BI` `Data Cleaning` `Statistical Analysis` `Predictive Modeling` `Public Policy Analytics`

## 💼 CV-Ready Bullets
- Engineered an end-to-end data science pipeline on the federal FY2018 Public Library Survey (**17,478 outlets × 37 features**), delivering Random Forest regression (**R² = 0.61**) and classification (**72% accuracy**) models to predict library operational capacity.
- Applied ANOVA and Chi-Square hypothesis testing to statistically validate urban-vs-rural infrastructure strategies, and segmented all outlets into strategic **Facility Tiers** via K-Means clustering.
- Built an interactive **Power BI dashboard** translating model outputs into actionable policy intelligence for urban planners and decision-makers.

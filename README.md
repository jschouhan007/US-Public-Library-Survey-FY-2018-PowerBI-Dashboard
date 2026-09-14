# 📚 U.S. Public Library Survey FY2018 — Power BI Dashboard

> **Interactive Power BI dashboard built from the FY2018 U.S. Public Library Survey (PLS) to explore public-library infrastructure, outlet characteristics, geography, and operating patterns across the United States.**

[![Power BI](https://img.shields.io/badge/Microsoft%20Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiYWJmMmRkNGMtYjdiMi00NWU3LWEwMjgtYTMyYmFmMTA0OTQ2IiwidCI6ImUxNGU3M2ViLTUyNTEtNDM4OC04ZDY3LThmOWYyZTJkNWE0NiIsImMiOjEwfQ%3D%3D&embedImagePlaceholder=true)
[![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Preparation-217346)](https://learn.microsoft.com/power-query/)
[![DAX](https://img.shields.io/badge/DAX-Analysis-0078D4)](https://learn.microsoft.com/dax/)
[![IMLS](https://img.shields.io/badge/Data-IMLS%20PLS-blue)](https://www.imls.gov/research-evaluation/surveys/public-libraries-survey-pls)

## 🔗 Live Interactive Dashboard

### **[▶ Open the Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYWJmMmRkNGMtYjdiMi00NWU3LWEwMjgtYTMyYmFmMTA0OTQ2IiwidCI6ImUxNGU3M2ViLTUyNTEtNDM4OC04ZDY3LThmOWYyZTJkNWE0NiIsImMiOjEwfQ%3D%3D&embedImagePlaceholder=true)**

The report is published through **Power BI's web publishing/sharing experience**, allowing the finished dashboard to be opened interactively in a browser without requiring the raw dataset to be manually explored.

---

## 🎯 Project Overview

This repository contains the **Power BI implementation** of an analysis based on the **FY2018 Public Libraries Survey (PLS)** published by the **Institute of Museum and Library Services (IMLS)**.

The dashboard converts public-library survey data into an interactive business-intelligence report. The work covers the full Power BI workflow:

```text
Raw PLS Data
     ↓
Power BI Data Import
     ↓
Power Query
     ↓
Cleaning & Transformation
     ↓
Data Modeling
     ↓
DAX / Measures
     ↓
Interactive Visualizations
     ↓
Dashboard & Exploration
     ↓
Published Power BI Report
```

A key characteristic of this project is that the **data cleaning, preparation, transformation, analytical shaping, calculations, and dashboard development were performed within Power BI itself**, primarily through **Power Query, the Power BI data model, and DAX**.

This repository should therefore be read as a **Power BI / Business Intelligence project**, rather than as a Python machine-learning implementation.

---

## 📊 Dataset

### Source

**U.S. Public Libraries Survey (PLS), Fiscal Year 2018**  
**Publisher:** Institute of Museum and Library Services (IMLS)

IMLS describes the PLS as an annual survey covering approximately 9,000 public library systems and approximately 17,000 individual public library outlets, including main libraries, branches, and bookmobiles. The FY2018 public-use data include a dedicated **Public Library Outlet Data File** containing **17,478 outlet records**.

### Official Sources

- **[IMLS — Public Libraries Survey (PLS)](https://www.imls.gov/research-evaluation/surveys/public-libraries-survey-pls)**
- **[IMLS — FY2018 PLS Data & Documentation](https://www.imls.gov/sites/default/files/2018_pls_data_file_documentation.pdf)**
- **[IMLS — FY2018 PLS Data Collection](https://www.imls.gov/research-evaluation/surveys-data/public-libraries-survey/report-your-pls-data/fy-2018-pls-data)**

### Dataset Scope Used for the Dashboard

| Item | Description |
|---|---|
| Survey | U.S. Public Libraries Survey (PLS) |
| Fiscal year | FY2018 |
| Primary outlet dataset | Public Library Outlet Data File |
| Outlet records | 17,478 |
| Geographic coverage | United States public library outlets in the FY2018 PLS |
| Data provider | Institute of Museum and Library Services (IMLS) |

The source documentation identifies outlet-level information including outlet type and operational/geographic characteristics. The dashboard transforms relevant fields into an analysis-ready Power BI model.

---

## 🧹 Data Cleaning & Transformation in Power Query

The raw survey data was not treated as dashboard-ready data. It was prepared directly inside Power BI before visualization.

The Power Query stage is used to turn raw source fields into consistent, analysis-ready data.

### Main preparation tasks

- Importing the source dataset into Power BI
- Inspecting the raw schema and field types
- Cleaning inconsistent or unusable values
- Handling missing / unavailable values where appropriate
- Correcting and standardizing data types
- Filtering records or values that should not participate in a particular analysis
- Transforming source columns for reporting
- Preparing categorical fields for readable dashboard labels
- Creating analysis-ready fields derived from the source columns
- Structuring the final dataset for the Power BI model

### Why Power Query was used

Keeping the preparation process inside Power BI makes the report easier to reproduce and maintain: the transformation logic sits between the source data and the report model rather than depending on an external Python preprocessing script.

---

## 🏗️ Data Modeling

After transformation, the prepared data is loaded into the **Power BI data model** for reporting and interactive analysis.

The modeling stage focuses on making the data usable by report visuals and filters rather than simply displaying the raw table.

Key modeling activities include:

- Organizing analytical fields
- Defining the fields used as dimensions and reporting attributes
- Building calculated measures where required
- Supporting slicers and report filters
- Enabling visual-level and cross-visual analysis
- Structuring data so aggregated metrics respond dynamically to user selections

The result is a report model designed for **interactive exploration**, not a static exported chart set.

---

## 🧮 DAX & Analytical Calculations

**DAX (Data Analysis Expressions)** is used within Power BI for report-level analytical calculations and measures.

These calculations support metrics and comparisons such as:

- Library / outlet counts
- Aggregated operating measures
- Geographic comparisons
- Outlet-type comparisons
- Facility characteristics
- Summary KPIs
- Filter-responsive metrics

Because these are model/report calculations, users can change selections in the report and see the relevant metrics update dynamically.

> **Important:** The dashboard is a Power BI analytical report. It does not represent the Python Random Forest, K-Means, or SciPy pipeline documented in `README_PLS_DataScience_ML.md`.

---

## 📈 Dashboard Analysis

The report is designed to turn a large public-sector survey dataset into an interactive visual analysis layer.

The dashboard supports exploration of themes including:

### 🇺🇸 Geographic Analysis

Compare library and outlet characteristics across U.S. geographic areas and states represented in the dataset.

### 🏛️ Outlet Structure

Explore the composition and characteristics of library outlets, including outlet-type distinctions available in the source data.

### 🌎 Locale / Community Context

Analyze differences across geographic or community classifications represented in the PLS data, including city, suburban, town, and rural categories where used in the report.

### 📐 Facility Characteristics

Examine physical / infrastructure-related measures available at outlet level, including facility-size information used in the underlying analysis.

### ⏱️ Operating Patterns

Explore operating measures such as annual service hours and related operational fields available in the FY2018 data.

### 🔎 Interactive Comparisons

Use the report's interactive controls to move from national-level summaries to more focused subsets of the data and compare categories without manually rebuilding the analysis.

---

## 🎛️ Interactive Power BI Features

The published report is intended to be explored interactively.

Typical interaction patterns in the report include:

- Slicers and filters
- Dynamic KPI / measure updates
- Cross-filtering between visuals
- Category-based comparisons
- Geographic filtering / comparison where applicable
- Interactive chart exploration
- Tooltips and contextual visual details where configured

The goal is to make the dataset usable by someone who does **not** need to open the original raw data and manually perform the analysis.

---

## 💡 Analytical Questions the Dashboard Helps Explore

The report can be used to investigate questions such as:

- How are public library outlets distributed across the United States?
- How does outlet composition vary by geography?
- How do Central, Branch, Bookmobile, and other source-defined outlet categories compare where represented?
- How do library characteristics differ between urban and rural settings?
- How does facility size vary across different locations or outlet categories?
- How do operating hours differ across geographic and community classifications?
- Which states or areas show notable differences in library infrastructure and operations?
- How do multiple library characteristics change together when the report is filtered to a specific segment?

These are **descriptive and comparative BI questions**; the dashboard is intended to surface patterns in the FY2018 data rather than establish causal relationships.

---

## 🔍 From Raw Data to Decision-Friendly Reporting

A major purpose of the project is the translation of a large government survey into an interface that is easier to understand and investigate.

```text
             RAW SURVEY DATA
                    │
                    ▼
          ┌───────────────────┐
          │    Power Query    │
          │ Clean + Transform │
          └─────────┬─────────┘
                    │
                    ▼
          ┌───────────────────┐
          │   Data Model      │
          │ Fields + Measures │
          └─────────┬─────────┘
                    │
                    ▼
          ┌───────────────────┐
          │       DAX         │
          │ Analytical Metrics│
          └─────────┬─────────┘
                    │
                    ▼
          ┌───────────────────┐
          │ Power BI Report   │
          │ Visuals + Filters │
          └─────────┬─────────┘
                    │
                    ▼
             INTERACTIVE BI
               DASHBOARD
```

This workflow demonstrates the practical use of Power BI beyond basic chart creation: **data preparation → modeling → analytical measures → visualization → interactive reporting**.

---

## 🛠️ Technology Stack

| Area | Technology |
|---|---|
| Business Intelligence | **Microsoft Power BI** |
| Data Preparation | **Power Query** |
| Analytical Calculations | **DAX** |
| Data Modeling | **Power BI Data Model** |
| Visualization | **Power BI Visuals** |
| Source Data | **FY2018 U.S. Public Libraries Survey (IMLS)** |
| Delivery | **Published Power BI Web Report** |

### Not the implementation stack for this repository

This repository's dashboard implementation should **not** be described as a Python/Scikit-Learn/ML project. The separate `README_PLS_DataScience_ML.md` documents a different analytical workflow involving Python, EDA, statistical testing, and machine learning.

---

## 📂 Repository Structure

```text
Public-Library-Survey-FY-2018-US-Data-Science-Dashboard/
│
├── PowerBI Dashboard & Datasets/
│   └── Power BI dashboard and associated project data/assets
│
├── README.md
│   └── Documentation for the Power BI dashboard
│
└── README_PLS_DataScience_ML.md
    └── Separate Data Science / Machine Learning documentation
```

The repository is intentionally separated so that the **Power BI dashboard documentation** and the **broader Data Science / ML documentation** do not get mixed together.

---

## 🚀 How to Explore the Project

### 1. View the published dashboard

Open the live report:

**[▶ Launch Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYWJmMmRkNGMtYjdiMi00NWU3LWEwMjgtYTMyYmFmMTA0OTQ2IiwidCI6ImUxNGU3M2ViLTUyNTEtNDM4OC04ZDY3LThmOWYyZTJkNWE0NiIsImMiOjEwfQ%3D%3D&embedImagePlaceholder=true)**

### 2. Explore the repository assets

Open the `PowerBI Dashboard & Datasets` directory to inspect the Power BI project files and associated dataset assets committed to the repository.

### 3. Review the methodology

For the separate Python / statistical / ML work associated with the broader PLS analysis, see:

[`README_PLS_DataScience_ML.md`](./README_PLS_DataScience_ML.md)

---

## 📌 Important Scope & Interpretation Notes

### FY2018 snapshot

The dashboard is based on **Fiscal Year 2018** PLS data. It should therefore be interpreted as an analysis of that survey year rather than a live, continuously updated representation of U.S. public libraries.

### Descriptive BI analysis

The Power BI report is primarily a **descriptive and exploratory business-intelligence dashboard**. Relationships visible in charts should not automatically be interpreted as causal relationships.

### Source data definitions

Variable meanings, coding, scope, exclusions, and other methodological details should be interpreted according to the official IMLS FY2018 PLS documentation.

---

## 🎓 Skills Demonstrated

This project demonstrates practical ability in:

- **Power BI Desktop**
- **Power Query / M-based data transformation**
- **Data cleaning and preparation**
- **Data modeling**
- **DAX measures and analytical calculations**
- **KPI design**
- **Interactive dashboard development**
- **Data visualization**
- **Geographic and categorical analysis**
- **Public-sector / government dataset analysis**
- **Business intelligence reporting**
- **Interactive analytical storytelling**
- **Publishing and sharing a live Power BI report**

---

## 🧠 Why This Project Is Portfolio-Relevant

This project demonstrates a complete Power BI workflow rather than only the final charts.

It shows that the work involved:

> **Understanding raw data → cleaning it → transforming it → modeling it → creating analytical measures → designing an interactive report → publishing the result for real users.**

That makes the project relevant to roles involving:

- Business Intelligence
- Data Analysis
- Power BI Development
- Reporting & Analytics
- Data Visualization
- Junior Data Engineering / BI Engineering
- Public-sector / operational analytics

---

## 📚 Data Source & Attribution

The underlying data are provided by the **Institute of Museum and Library Services (IMLS)** through the U.S. Public Libraries Survey.

Official source:

**[Institute of Museum and Library Services — Public Libraries Survey (PLS)](https://www.imls.gov/research-evaluation/surveys/public-libraries-survey-pls)**

The official FY2018 documentation identifies the **Public Library Outlet Data File (`pls_outlet_pud18i`)** as containing **17,478 records** for public library outlets in FY2018.

---

## 👤 Author

**Jaideep Singh Chouhan**  
B.Tech CSE — Data Science / Machine Learning  
Lovely Professional University, Punjab, India

---

## ⭐ Project Links

| Resource | Link |
|---|---|
| **Live Power BI Dashboard** | [Open Dashboard ↗](https://app.powerbi.com/view?r=eyJrIjoiYWJmMmRkNGMtYjdiMi00NWU3LWEwMjgtYTMyYmFmMTA0OTQ2IiwidCI6ImUxNGU3M2ViLTUyNTEtNDM4OC04ZDY3LThmOWYyZTJkNWE0NiIsImMiOjEwfQ%3D%3D&embedImagePlaceholder=true) |
| **GitHub Repository** | [Open Repository ↗](https://github.com/jschouhan007/Public-Library-Survey-FY-2018-US-Data-Science-Dashboard) |
| **Official IMLS PLS Data** | [Open IMLS ↗](https://www.imls.gov/research-evaluation/surveys/public-libraries-survey-pls) |
| **FY2018 PLS Documentation** | [Open Documentation ↗](https://www.imls.gov/sites/default/files/2018_pls_data_file_documentation.pdf) |

---

## 📎 Final Takeaway

> **A Power BI Business Intelligence project that transforms the FY2018 U.S. Public Libraries Survey into an interactive analytical dashboard for exploring library infrastructure, outlet characteristics, geography, and operating patterns.**

---

### Keywords

`Power BI` `Power Query` `DAX` `Business Intelligence` `BI Dashboard` `Data Cleaning` `Data Transformation` `Data Modeling` `Data Visualization` `Interactive Dashboard` `KPI` `Public Library Survey` `IMLS` `Government Data` `Public Sector Analytics` `Data Analysis` `FY2018 PLS`

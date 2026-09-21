Heart Disease Risk & Patient Health Analytics Platform


Cardiovascular disease is a major health concern, and the increasing availability of patient-level data provides an opportunity to better understand and manage heart disease risk.
However, healthcare data is often spread across demographic, clinical, and lifestyle factors such as age, BMI, cholesterol, blood pressure, heart rate, smoking status, family history,
exercise, stress, sleep, and chest pain type,making it difficult to identify how these factors interact and contribute to heart disease. The core objective is to analyze these attributes 
together to identify patterns and determine which factors and patient groups are most strongly associated with heart disease. Without a consolidated view, healthcare teams may overlook 
high-risk populations, allocate preventive-care resources inefficiently, and miss opportunities for early screening, counselling, and intervention. The proposed solution is an interactive
analytical dashboard that combines clinical, demographic, and lifestyle information into a single view, enabling healthcare stakeholders to compare heart disease patterns across smoking status,
chest pain type, BMI, family history, age, and other key indicators, identify high-risk segments, and gain clear, actionable insights to support preventive healthcare, patient counselling, and more informed resource allocation. 

An end-to-end data analytics and business intelligence pipeline designed to transform clinical patient records into interactive, high-performance diagnostic screening tools. This platform processes complex cardiovascular telemetry to isolate high-risk patient segments, evaluate systemic comorbidities, and provide healthcare coordinators with real-time, data-backed preventive decision frameworks.



## 📌 1. Project Architecture & Framework

This system leverages a decoupled data architecture to handle clinical patient telemetry efficiently from ingestion through deployment:

Use code with caution.[ Raw CSV Datasets ]│▼ (Python / Pandas Engine)[ Robust Median Ingestion & ETL Filtering ] ───► Standard Casing & Binary Mapping│▼ (Clean Data Models)[ Power BI Data Engine / DAX Calculation Architecture ]│▼[ Interactive UI Layout Canvas ] ◄─── (Dynamic Sub-150ms Slicer Pipeline)


## 🎯 2. Strategic Project Objectives

* **Demographic Segmentation:** Isolate high-risk patient profiles across localized age brackets (<45, 45-60, >60) and biological sexes.
* **Comorbidity Impact Quantification:** Quantify the statistical compounding effect of secondary conditions (Smoking, Diabetes, High Blood Pressure) on baseline diagnostic outcomes.
* **Clinical BI System Delivery:** Design a high-performance visual screening dashboard featuring dynamic data cross-filtering capabilities under 150ms.



## 🛠️ 3. Technical Toolstack & Engineering Assets

* **Data Engineering & ETL Pipelines:** Python 3.x (Pandas, NumPy)
* **Analytics & Dashboard Architecture:** Power BI Desktop / Tableau Prep
* **Statistical Data Foundations:** UCI Machine Learning Repository & Kaggle Clinical Heart Disease Datasets



## 📊 4. Ingestion Pipeline & Data Preprocessing

### 🔹 Data Quality Management
* **Null-Value Handling:** Evaluated structural diagnostic columns; 0 missing values detected post-validation.
* **Standardization Filters:** Mapped structural strings to proper casing formats. Transformed raw numerical flags to logical labels (e.g., mapping numerical `1` to `Male` and `0` to `Female`).
* **Robust Outlier Normalization:** Identified extreme physiological anomalies (Serum Cholesterol >400 mg/dl, Resting Blood Pressure >180 mm Hg) and applied target robust median substitution filters to protect model variance against heavy skewing.

### 🔹 Structural Data Engineering (DAX & Engine Metrics)
* **2 Level Calculated Engine Columns:**
  * `Age Group` (Segmented categories: `<45`, `45-60`, `>60`)
  * `Gender Label`
* **4 Core Complex Analytical Measures:**
  * `Total Patients` (Baseline metric aggregation)
  * `Heart Disease Rate %` (Proportional risk calculations)
  * `Average Ejection Fraction` (Continuous physiological averages)
  * `Survival Count` (Outcome-driven clinical evaluation metrics)



## 📈 5. Interface Engineering & Reporting Setup

The operational production visual engine contains exactly **8 integrated functional interface elements**: 1 Main Banner Header, 3 Summary KPI Cards, and 4 Advanced Visual Charts.

| Reporting Section Focus | Targeted Primary Metrics | Visual Components Utilized |
| :--- | :--- | :--- |
| **Demographics Pipeline** | Total Patient Volume, Clean Biological Sex Splits | Core Donut Charts + Responsive KPI Cards |
| **Physiological Analysis** | Ejection Fraction Trends vs. Ultimate Patient Survival | Overlapping Continuous Line & Box Plots |
| **Systemic Comorbidities** | Compound Impact Profiles (Smoking Status & Blood Pressure) | High-Density Matrix Heatmap Canvas |



## 💡 6. Evaluated Project Insights

* **Insight 1 (Age Progression):** Target heart disease prevalence escalates significantly beyond the 45-year age boundary universally across both biological categories.
* **Insight 2 (Demographic Baseline):** Male cohorts exhibit a higher underlying baseline diagnosis profile within this consolidated repository schema.
* **Insight 3 (Compound Indicators):** Paired degradation in Ejection Fraction paired with lower Maximum Heart Rate tracking forms a significantly sharper indicator of prospective danger than tracking isolated high cholesterol spikes.



## 📂 7. Repository Directory Structure

```text
├── data/
│   ├── raw/               # Original clinical data from Kaggle/UCI
│   └── processed/         # Cleaned, median-substituted CSV payloads
├── notebooks/
│   └── data_preprocessing.ipynb  # Python Jupyter notebook detailing Pandas ETL scripts
├── reports/
│   ├── Heart_Disease_Dashboard.pbix # Finished Power BI visual report canvas
│   └── Final_Project_Report.pdf     # Documented performance metrics and writeup
├── requirements.txt       # Python environment dependencies
└── README.md              # Project documentation file
```



## 🚀 8. Setup & Installation Run Guide

### Step 1: Clone the Target Repository
```bash
git clone https://github.com
cd Heart-Disease-Risk-and-Patient-Health-Analysis


### Step 2: Establish Python Dependencies
```bash
pip install -r requirements.txt


### Step 3: Run the ETL Pipeline Notebook
Open the notebook repository via your IDE or terminal to inspect the outlier normalization algorithms:
```bash
jupyter notebook notebooks/data_preprocessing.ipynb


### Step 4: Access the BI Canvas
1. Open **Power BI Desktop**.
2. Click `File -> Open Report` and navigate to `reports/Heart_Disease_Dashboard.pbix`.
3. Use the contextual slicers for **Age Group, Biological Sex, or Chest Pain Type** to test cross-filtering response times.


## 🔮 9. Future System Upgrades
Future analytical roadmap expansions focus on training predictive Machine Learning


# Data Engineering Project

## Overview
This project addresses multiple challenges in hospital data engineering, including data integration, analytics, and clinical prediction. It combines data warehouse design, ETL processes, interactive dashboards built on the data warehouse, and advanced machine learning workflows for comprehensive clinical and operational insights.

## Project Tasks

1. **Data Warehouse & ETL Process**
	- Designed a clinical data warehouse to centralize hospital information.
	- Implemented ETL (Extract, Transform, Load) workflows to collect, prepare, and transform data from multiple CSV sources (+20 csv file) (e.g., admissions, patients, services) for analytics and BI dashboards, following the data warehouse schema.
	- Enabled efficient storage and querying for downstream analytics.

2. **Interactive Dashboards with Power BI**
	- Built interactive dashboards on top of the data warehouse design to visualize key hospital metrics: patient demographics, diagnoses, drug usage, admissions, transfers, and ICU workload.
	- Provided actionable insights for executive, medical, and unit chiefs.
	- Example screenshots are included below to illustrate dashboard features.

3. **Data Preparation & Dimensionality Reduction**
	- Cleaned, merged, imputed missing values, encoded categorical variables, scaled features, engineered new features, and handled outliers using dedicated notebooks.
	- Scaled features to standardize ranges.
	- Used Principal Component Analysis (PCA) to reduce dimensionality and improve clustering/classification performance.

4. **Clustering & Classification Models**
	- Implemented clustering algorithms (KMeans, DBSCAN, Agglomerative, GMM) to group patients based on clinical profiles.
	- Developed classification models (SVM, Logistic Regression, Random Forest, XGBoost) to predict ICU need.
	- Selected SVM as the best classifier and performed hyperparameter tuning via grid search, but this did not improve accuracy compared to the default settings.

## Folder Structure
- 'notebooks/': All Jupyter notebooks for data merging, cleaning, PCA, clustering, and classification.
- 'data/': Processed datasets (e.g., afterPCA.csv, merged-data.csv, etc.).
	-'nanim.csv' is the raw data after we merged patients,admissions,transfers,etc in merging_data.ipynb and used it in data_preparation.ipynb
	-'supervised.csv'  is the cleaned, imputed, encoded, and scaled dataset (without PCA)
	-'res.csv' is the output after the PCA used in clustering
- 'screenshots/': Dashboard screenshots for README or documentation.

## Key Notebooks
- **Data Merging**: Collects and merges data from multiple CSVs (admissions, patients, services, etc.) into a single dataset.
- **Data Preparation & PCA**: Cleans data, handles outliers, and applies PCA for dimensionality reduction.
- **Clustering**: Groups patients using unsupervised learning algorithms and interprets cluster profiles.
- **Classification**: Predicts ICU need using supervised models, with detailed evaluation and optimization.

## Data Warehouse & BI Dashboards
- The project includes the design and partial implementation of a clinical data warehouse.
- ETL processes automate data integration for analytics.
- Power BI dashboards provide interactive views for hospital management and clinical staff.
- Example dashboard screenshots are shown below. Additional dashboard images can be found in the `screenshots/` folder.

---

![Dashboard Screenshot 1](project\screenshots\units_transfers.png)
![Dashboard Screenshot 2](project\screenshots\patients_demographics.png)


---
## Data Source:
The main dataset used is the publicly available "mimic-iii-clinical-database-demo-1.4". Due to its large size and licensing, it is not included in this repository. Please download it from the official source if needed.



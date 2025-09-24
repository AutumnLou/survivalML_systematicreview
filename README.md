# survivalML_systematicreview
Database of machine learning methods used in cancer survival analysis, compiled from systematic review (196 studies)

## Available Datasets

This repository contains two main datasets compiled from our systematic review.

---

### 1. `database_overview.csv`

This file provides an **overview of the 196 studies** included in the systematic review.  
It includes metadata and study-level characteristics with the following columns:

- **link** — Hyperlink to full-text article  
- **title** — Title of the article  
- **author** — First author (surname, first name)  
- **year** — Year of publication  
- **cancer_type** — Cancer/carcinoma type (e.g., Pan-cancer, Breast, Cervical, Colon & Rectal, Kidney, Leukemia, Prostate, etc.)  
- **criteria** — Inclusion/exclusion criteria; Patient-level, Cohort-level, or None  
- **study_type** — Study type (retrospective, prospective, clinical trial, reanalysis, other)  
- **data_type** — Data type (Clinicopathologic, Raw imaging data, Radiomics, Genomics, Epigenomics, Proteomics, Transcriptomics, Metabolomics, Other)  
- **size** — Cohort/sample size  
- **timepoint** — Timepoint of evaluation (e.g., pre-operative, post-operative, diagnosis, etc.)  
- **publicly_available_data** — Availability of data (Yes, No, Available on request, Not stated, Other)  
- **source** — Data source (CT = clinical trial, DB = database, H = hospital, GEO = Gene Expression Omnibus, SEER = Surveillance, Epidemiology, and End Results, TCGA = The Cancer Genome Atlas, TCIA = The Cancer Imaging Archive, Other)  
- **outcome** — Survival outcome(s) (e.g., Overall Survival (OS), Progression-Free Survival (PFS), Cancer-Specific Survival, Metastasis-Free Survival, etc.)  
- **software** — Software used (R, Python, SAS, Stata, Other)  
- **code** — Is code available (e.g., GitHub, supplemental material)?  
- **ML** — General ML method(s) implemented (Regularisation, Tree-based methods, Deep Neural Networks, SVM, Boosting, etc.)  
- **ML_detail** — Exact ML model(s) implemented  
- **trad** — Traditional/classical method(s) implemented (e.g., Cox proportional hazards, Fine-Gray, Parametric, State-of-the-art, Other)  
- **prefilter** — Prefiltering method(s) applied (e.g., Correlation, Differentially Expressed Genes, Clustering, Pre-specified/hand-selected variables)  
- **fs** — Feature selection method(s) used (e.g., Univariate analysis, Stepwise selection, Variable importance)  
- **framework** — Sampling framework (e.g., Bootstrapping, Cross-validation, Train/test split)  
- **dis** — Metrics for discrimination (e.g., C-index, Integrated Brier Score (IBS), Other, None)  
- **cal** — Calibration methods (e.g., Calibration curves, Brier score, Other, None)  
- **pred** — Predictive performance evaluation beyond discrimination (e.g., Decision Curve Analysis, Net Benefit, Time-dependent AUC/ROC)  

---

### 2. `database_prediction.csv`

This file contains the **results of the performance analysis**, focusing on comparisons of ML and traditional methods for overall survival prediction. 39 studies were analyzed to evaluate performance. 


**Columns include:**  
- **cancer** — Cancer type  
- **detail** — Subtype/detail of cancer  
- **sample_size** — Cohort/sample size  
- **framework** — Sampling framework (e.g., CV, bootstrapping, train/test split)  
- **reference** — Author surname + year  
- **full_reference** — Full citation of the study  
- **title** — Title of the article  
- **link** — Hyperlink to the article  
- **C-index values** (where available):  
  - `CPH` — Cox proportional hazards  
  - `RSF` — Random Survival Forest  
  - `Deep Learning`  
  - `Regularisation`  
  - `Boosting`  
  - `Shallow Neural Network`  
  - `SVM` — Support Vector Machine  
  - `Other`  

---

👉 Both datasets are provided in **CSV format** for transparency and easy reuse. An `.xlsx` version is also available for convenience.

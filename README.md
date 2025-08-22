
# Rainfall-Runoff Prediction using ML (SVR, RF, XGBoost)

###  Objective

To simulate and predict **runoff** from **rainfall data** using supervised ML techniques such as:
- **Support Vector Regression (SVR)**
- **Random Forest Regression**
- **XGBoost Regression**
- (Optional: Multiple Linear Regression & LSTM if time permits)

---

### Folder Structure

- **data/**: Raw & processed datasets (mainly IMD rainfall & river basin runoff)
- **notebooks/**: Jupyter/Colab EDA, modeling, visualizations
- **src/**: All major code modules for data processing & ML pipelines
- **pyspark/**: Optional PySpark-based large-scale data processing
- **references/**: All research papers and literature used for modeling strategy
- **reports/**: Model evaluation results, graphs, and final conclusion



### Data Collection

- **Source**: IMD (Indian Meteorological Department) Rainfall data, CWC for Runoff
- **Format**: Mostly `.csv`, `.xlsx` after extraction
- **Tools for Extraction**:
  - Web scraping scripts for IMD (in `src/data_acquisition`)
  - Manual download + formatting



 ### Preprocessing & Featur engg.

- Handling missing/null values
- Normalizing rainfall values
- Aggregating at daily/monthly level
- Creating lag features (e.g., 3-day rainfall sum)
- Creating labels for runoff prediction



###  Modeling Pipeline

- **Problem Type**: Supervised Regression (and Classification where applicable)
- **Features Used**: Rainfall lag values, temperature (optional), soil moisture (if available)
- **Models Implemented**:
  - `SVR` with RBF and polynomial kernels
  - `Random Forest Regressor`
  - `XGBoost Regressor`
  - `Multiple Linear Regression`
  - (Optional) `LSTM` if time permits



### Evaluation Metrics

- RMSE
- MAE
- R² Score
- Visual comparisons (scatter plots, residual plots)





### In case of scaling up:
-  `pyspark.sql` and `pyspark.ml` for model pipelines
-  distributed model training and large-scale data handling
- Integration script available in `/pyspark/pyspark_pipeline.py`





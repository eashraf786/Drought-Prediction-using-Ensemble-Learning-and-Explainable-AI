## 🌾 Drought Prediction Using Ensemble Machine Learning and Explainable AI
Accurate forecasting for climate-resilient agriculture and proactive water management

### 📌 Overview
This project presents a robust time-series drought prediction system using ensemble learning and Explainable AI (XAI). It analyzes 51 years (1972–2022) of high-resolution MERRA satellite data across five drought-prone Indian states, modeling complex meteorological patterns to forecast drought occurrence with high accuracy and interpretability.

Key technologies include XGBoost, Random Forest, SVM, KNN, SHAP, and LIME — all integrated to support transparent, actionable early-warning systems for policymakers and farmers.

### 🎯 Objectives
Predict short-term drought conditions using weather and climate features.

Ensure model interpretability with SHAP & LIME for stakeholder trust.

Visualize predictions with interactive district-wise drought risk maps.

Empower data-driven resource allocation and sustainable agriculture planning.

### 🗂️ Dataset
Source: NASA’s MERRA satellite reanalysis data (1972–2022)

Coverage: 5 states → Maharashtra, Gujarat, Andhra Pradesh, Bihar, Karnataka

Features:

Avg. Temperature, SPI, Precipitation, Potential Evapotranspiration, Vapor Pressure, Wet Day Frequency

Lagged features (up to 6 months)

Categorical: State, District

Temporal: Month, Year (with cyclic encoding)

Size: 29,988 monthly records, balanced across 49 districts

### ⚙️ Project Pipeline
#### 1️⃣ Data Cleaning & Preprocessing:

Remove missing/duplicate values.

Time-series exploratory plots for trend analysis.

Label & ordinal encoding for categorical/time variables.

Cyclic transformations for month/year to preserve seasonality.

#### 2️⃣ Feature Engineering:

Generate lagged features (t-1 to t-6) for each weather metric.

Final feature space: 42 columns (36 lagged + cyclic + categorical).

#### 3️⃣ Modeling:

Train & evaluate: Random Forest, XGBoost, SVM, KNN.

Best performing: XGBoost, fine-tuned with RandomizedSearchCV.

Accuracy: 97.1%

F1-Score: 80.0%

Recall: 90.1%

#### 4️⃣ Explainability:

SHAP: Global feature importance → SPI & precipitation lags = top drivers.

LIME: Local interpretability → shows feature impacts for specific district predictions.

#### 5️⃣ Visualization:

Folium + Geoapify: Generate an interactive map showing districts at drought risk for Jan 2023.

### 🧩 Tools & Libraries
Python, Pandas, NumPy, Scikit-learn, XGBoost, SHAP, LIME

Folium, Geoapify API, Matplotlib, Seaborn

Jupyter Notebook, Google Colab

### 🏆 Impact
Supports early intervention in drought-prone regions.

Enables evidence-based water resource planning.

Increases trust in AI systems via transparent explanations.

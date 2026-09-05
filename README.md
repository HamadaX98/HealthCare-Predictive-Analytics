# HealthCare Predictive Analytics

A end-to-end data science and machine learning pipeline that explores patient healthcare records, cleans and visualizes demographic and clinical features, and trains classification models to predict patient **Test Results** using MLflow for experiment tracking.

---

## Project Structure & Team

* **Track:** AI & Data Science


* **Group Code:** `SHR1_AIS3_M1e`


### Team Members & Contributions

* **Ahmed Magdy Ahmed (Leader):** Data Collection & MLflow Integration


* **Khaled Tarek Mohamed:** Data Exploration, Analysis & Visualization


* **Modather Abdelmohsen Abdelmawgood:** Predictive Modeling & Evaluation



---

## Tech Stack & Libraries

* **Data Manipulation & Analysis:** `pandas`, `numpy`, `scipy`

* **Data Visualization:** `plotly.express`, `seaborn`, `matplotlib`

* **Machine Learning:** `scikit-learn` (`DecisionTreeClassifier`, `RandomForestClassifier`, `LabelEncoder`)


* **Experiment Tracking:** `mlflow`, `pyngrok`

* **Data Source:** Kaggle (`prasad22/healthcare-dataset`) downloaded via `kagglehub`


---

## Key Workflow & Pipeline

```
┌─────────────────┐     ┌──────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│ Data Collection │ ──► │ Data Cleaning &  │ ──► │ Machine Learning │ ──► │ MLflow Tracking │
│  (Kagglehub)    │     │   EDA (Plotly)   │     │    (DTC & RFC)   │     │   & Logging     │
└─────────────────┘     └──────────────────┘     └──────────────────┘     └─────────────────┘

```

1. **Data Ingestion & Cleaning:**
* Downloads dataset using `kagglehub`.


* Removes duplicate records and verifies null values.


* Inspects distributions across demographics, medications, insurance providers, and admission types.




2. **Exploratory Data Analysis:**
* Box plots for outlier detection on **Billing Amount**.


* Interactive sunburst charts analyzing relationships between categories (e.g., *Test Results by Medication*, *Patient Status*).


* Histogram with mean indicator for **Age Distribution**.




3. **Preprocessing & Modeling:**
* Encodes categorical columns using `LabelEncoder`.


* Configures **Test Results** as the target variable ($y$) and remaining features as inputs ($X$).


* Splits data into training and test sets ($N=2000$ test samples).


* Trains and evaluates both **Decision Tree Classifier** and **Random Forest Classifier** models.




4. **Experiment Tracking:**
* Runs an SQLite-backed MLflow UI server locally.


* Uses `ngrok` to expose the tracking UI via public URL.


* Logs Accuracy, Precision, Recall, F1 score, model artifacts, and signatures.





---

## Execution Guide

### 1. Requirements

Install all dependencies using `pip`:

```bash
pip install numpy pandas seaborn scipy plotly matplotlib scikit-learn kagglehub pyngrok mlflow

```

### 2. Running the Pipeline

Run the main script:

```bash
https://github.com/HamadaX98/HealthCare-Predictive-Analytics.git

```

### 3. Accessing the MLflow UI

* During execution, `ngrok` will ask for an authentication token from [ngrok Dashboard](https://www.google.com/search?q=https://dashboard.ngrok.com/signup).


* Paste the token into the prompt to generate a public ngrok tunnel pointing to your local MLflow tracking server (`[http://127.0.0.1:5000](http://127.0.0.1:5000)`).

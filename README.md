# Task 1: Automated Data Pipeline Development (ETL)

## 📌 Project Overview
This project establishes an automated **Extract, Transform, Load (ETL)** data processing pipeline built using Python, Pandas, and Scikit-Learn. The pipeline ingests raw, uncleaned passenger data from the Titanic dataset, handles missing values, standardizes numerical features, encodes categorical variables, and exports a cleaned, ML-ready dataset.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Libraries:** `pandas`, `numpy`, `scikit-learn`
* **Environment:** Google Colab / Jupyter Notebook

---

## 🔄 ETL Pipeline Steps

1. **Extract (Data Ingestion):**
   * Automatically downloads the raw Titanic CSV dataset from a public source.
   
2. **Transform (Data Preprocessing & Feature Engineering):**
   * **Missing Value Imputation:** 
     * Imputed missing `Age` values using **Median Strategy**.
     * Imputed missing `Embarked` values using **Most Frequent (Mode) Strategy**.
   * **Feature Scaling:** Applied `StandardScaler` to numerical columns (`Age`, `Fare`, `SibSp`, `Parch`) to convert values into Z-scores with mean 0 and variance 1.
   * **Categorical Encoding:** Applied `OneHotEncoder` to convert categorical variables (`Sex`, `Embarked`, `Pclass`) into binary sparse vectors.
   * Combined all transformations seamlessly using Scikit-Learn's `Pipeline` and `ColumnTransformer`.

3. **Load (Data Export):**
   * Outputted the fully preprocessed dataset into `cleaned_titanic_data.csv` ready for model training.

---

## 📁 Repository Structure
```text
├── Task1_Data_Pipeline.ipynb    # Main Google Colab Notebook
├── cleaned_titanic_data.csv     # Exported cleaned dataset
└── README.md                    # Project documentation

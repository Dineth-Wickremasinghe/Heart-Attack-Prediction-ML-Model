

# ❤️ Heart Attack Prediction Using Machine Learning

A machine learning project to predict heart attack risk using clinical and biometric patient data.
This project includes full preprocessing, model comparison, Random Forest optimization, and ethical considerations.

---

## 📘 **Project Overview**

Heart disease is one of the world's leading causes of death, making early prediction critical for preventive care.
This project builds a **machine learning-based heart attack prediction model** using a structured medical dataset containing patient clinical features.

The final model helps identify individuals at high risk, supporting healthcare professionals with faster and more accurate assessments.

---

## 📊 **Dataset**

* **Source:** Mendeley Data Repository
* **Total Records:** 1,319 patient entries
* **Type:** Structured clinical data (CSV)
* **Features:**

  * Age
  * Gender
  * Heart Rate
  * Systolic BP
  * Diastolic BP
  * Blood Sugar
  * CK-MB
  * Troponin
  * Risk Output (Target)

### ✔ Benefits

* Balanced class distribution
* Clean, structured medical attributes
* Suitable for ML integration

### ⚠ Limitations

* Missing lifestyle factors
* No comorbidity history
* Limited diagnostic richness
* Static values without temporal context

---

## 🧹 **Preprocessing Pipeline**

### 1️⃣ Data Cleaning

* Removed nulls and duplicates
* Outliers capped using **IQR method**
* Verified using boxplots & histograms

### 2️⃣ Feature Scaling

* **MinMaxScaler** applied to numerical features
* All values scaled to 0–1 range

### 3️⃣ Dimensionality Reduction

* PCA applied on Systolic & Diastolic BP
* Created: `BP_PC1`, `BP_PC2`
* Reduces multicollinearity

### 4️⃣ Feature Selection

* Based on Random Forest feature importance
* Removed **Gender** due to low contribution and potential bias

---

## 🤖 **Modeling & Algorithms**

The following algorithms were evaluated:

| Model               | Accuracy   | Precision  | Recall     | F1 Score   | ROC AUC    |
| ------------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Logistic Regression | 0.9132     | 0.9605     | 0.8957     | 0.9269     | 0.9184     |
| KNN                 | 0.8905     | 0.9652     | 0.8527     | 0.9055     | 0.9018     |
| SVM (Linear)        | 0.9169     | 0.9731     | 0.8895     | 0.9294     | 0.9251     |
| Decision Tree       | 0.9735     | 0.9698     | 0.9877     | 0.9787     | 0.9693     |
| **Random Forest**   | **0.9811** | **0.9876** | **0.9815** | **0.9846** | **0.9809** |
| ANN                 | 0.9358     | 0.9679     | 0.9263     | 0.9467     | 0.9386     |

### 🏆 **Selected Model: Random Forest**

Random Forest achieved the highest accuracy and best recall, making it most suitable for medical applications where false negatives are critical.

### Model Configuration

* 100 decision trees
* Bootstrap aggregation
* No maximum depth
* Scale-invariant
* Random state = 42

---

## 🛠 **Technology Stack**

* **Python 3**
* **Libraries:**

  * pandas
  * NumPy
  * scikit-learn
  * Matplotlib
  * Seaborn
* **Environment:** Google Colab

---

## 🔐 Ethical Considerations

### Fairness & Bias

* Tested across demographics
* Gender feature removed to avoid bias
* Balanced dataset prevents class skew

### Explainability

* SHAP & LIME recommended for clinical interpretability
* Feature importance visualized

### Accountability

* Model is a **decision support tool**, not a diagnostic system
* Human oversight required
* Documented with model cards & evaluation notes

---

## 🚀 Future Improvements

* Integrate **XGBoost / LightGBM** for better performance
* Deploy as a **web application** (Flask / FastAPI)
* Automate tuning using **GridSearchCV / Optuna**
* Add more clinical & lifestyle features

---

## 👥 Team Notes

* Effective task division based on skill sets
* Regular collaboration and revision
* Improved technical and project execution skills

---




